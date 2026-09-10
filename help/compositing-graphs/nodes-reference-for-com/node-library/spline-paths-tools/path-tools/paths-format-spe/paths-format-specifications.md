---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-format-specifications.html"
breadcrumb-title: ''
description: パス形式の仕様と、パスノードとスプラインノードで使用されるデータ構造について学習します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Format Specifications
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パス形式の仕様
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '2491'
ht-degree: 0%

---


# パス形式の仕様

このページでは、パス形式について説明し、パスツールに含まれる関数を使用してその形式のデータを操作するためのガイダンスを提供します。

## 形式の仕様

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

このセクションでは、<b>パスドキュメント</b> （または画像）をエンコードする方法について説明します：

Pathsドキュメントはパスのリストです。各パスは、<b>32ビット浮動小数点カラーテクスチャ</b>でエンコードされたセグメントのリストを記述します。

テクスチャは、「上」(*$pos.y &lt; 0.5*)と「下」(*$pos.y > 0.5*)の部分に分割されます。

「上」の部分のピクセルのデータは、「下」の部分の一致するピクセルと意味的に密接に関連し、逆も同様です。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![パスポリゴン符号化データ](paths-format-specifications.resources/PathsPolygon_Data.jpg "パスポリゴン符号化データ")

</td>
</tr>
</table>

>[!NOTE]
>
> パスデータは32ビットの精度を必要とし、低いビット深度を使用すると不正確な結果が生成されます。
> 
> したがって、パスデータを生成するノードの「出力フォーマット」パラメーターを「HDR高精度(32F)」に設定してください。

`*uv\_pos*`を&#39;top&#39;パーツのピクセルの2Dアドレス（*$pos*&#x200B;など）にします。

この文書の残りの部分：

* <b>top[uv\_pos].XYZW</b>は、上部のピクセルに格納されている4つのフロートを参照します。\
  top[uv\_pos] == sample\_color(paths, uv\_pos)
* <b>bottom[uv\_pos].XYZW</b>は、最下部の一致するピクセルに格納されている4つのフロートを参照します。\
  bottom[uv\_pos] == sample\_color(paths, uv\_pos + Float2(0, 0.5))

top[uv\_pos]とbottom[uv\_pos]を組み合わせると、ドキュメントの意味単位U[uv\_pos]が形成され、8つのフロートで構成されます。

### 文書ヘッダー

すべてのパス文書は、文書ヘッダーで始まります。 これは最初の意味単位U[(0,0)]:

+++上
<b>X</b>

パスの数（[0; 16777216]の正の整数でなければなりません）。

空のパスがある場合は、ここで数えられます。 ですから、「デコードするパスヘッダーの数」と考えることができます。

<b>YZ</b>

このドキュメントのピクセルサイズ（正確には`Float2(1,1) / $size`）。

これは、出力サイズが異なる[ピクセルプロセッサー](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)または[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)からパスを読み取る場合などに便利です。

<b>幅</b>

1/16 = 0.0625（ヘッダーフラグ）

+++

+++下
<b>XY</b>

このドキュメントで定義された最後の頂点のアドレス。 これは、新しいデータを追加する場合に便利です。

したがって、実際には、最後の頂点のアドレスよりも（スキャンライン順に）大きいアドレスであればどれでもかまいません。 範囲は、 &rbrack;0, 1[×]0,.5&lbrack;

<b>ZW</b>

未使用。Float2(0, 1)である必要があります。

+++

### パスヘッダー

ドキュメントのヘッダの直後にnumber-of-paths = top[(0,0)].X path-headersが続き、1つ一つが意味単位です。\
E.g. ドキュメント内に3つのパスがある場合、それらはU[(0,1)\*pixel\_size], U[(0,2)\*pixel\_size]およびU[(0,3)\*pixel\_size] (pixel\_size = top[(0,0)].YZ)に保存されます。

1行のピクセルに収まらないパスがある場合、残りのパスヘッダーはスキャンライン順に次の行に書き込まれます。\
NULLのパスヘッダー(`top[...].XYZW = Float4(0,0,0,0)`)を使用できます。このようなパスは空のパスとして使用できます。

N番目のパスのパスヘッダーは、アドレス`path\_addr`で次のように定義されます：

+++上
<b>X</b>

このパス内の頂点の数。 [0, 16777216]の範囲内である必要があります。

クローズパスの始点と終点が同じ位置にある場合は、2つの頂点がカウントされます。\
頂点が0個のパスは有効なパスです。

<b>年</b>

*Is\_closed*&#x200B;フラグ：パスが閉じている場合（例：円）は1、それ以外の場合（例：直線）。

<b>Z</b>

パスのインデックス&#x200B;*N.*&#x200B;は*path\_addr*と完全に一致する必要があります（以下の注を参照）。

<b>幅</b>

ヘッダーフラグ： 1/16 = 0.0625。

+++

+++下
<b>XY</b>

開始（または最初の）頂点アドレス。

<b>ZW</b>

終了（または最後）の頂点のアドレス。

+++

>[!NOTE]
>
> paths\_tools.sbsの関数`Utils/pixel\_index\_to\_position`を使用して、Nから`path\_addr`を計算できます： `path\_addr = pixel\_index\_to\_position(N+1)`

### 頂点情報

頂点は、ヘッダー（文書ヘッダーまたはパスヘッダー）の後の画像内の任意の場所に表示されます。 頂点は様々な「種類」（開始、中間、終了）にすることができ、2つのアドレスポインター（「リンク」）を使用して明示的にリンクされています。

<b>Start</b>および<b>End</b> 頂点は、この点で特別です。閉じた頂点または任意のリンクされたパスのネットワークを表現できるようにするには、一方のリンクを実際に使用して、同じパスを表す他のすべてのStartまたはEnd 頂点を循環リンクしたリストを作成します。 このように互いに一致する頂点を「同胞」と呼ぶ。 [歓迎されるイラスト]

正式には、アドレス`*vert\_addr*`の各頂点は次のように定義されています：

+++上
<b>XY</b>

頂点の位置。 座標には、NaNまたは±inf以外の任意の浮動小数点値を使用できます。 このレベルでのタイリングの概念は存在しないので（各フィルタの実装によって扱えるかどうかは関係ありません）、パスはユークリッド平面上で定義されているはずです。

<b>Z</b>

頂点パスのインデックス。 1つの頂点は1つのパスにのみ属することができます。 （既に説明したように、開始および終了頂点には兄弟を設定できます）。 パスインデックスはパスヘッダの取得に使用できるので（上のパスヘッダの節を参照）、必ず同期しておいてください。

<b>幅</b>

頂点のタイプ： 値の符号とその絶対値の間で分割されます。

符号パーツでは、値0は実際には頂点がないことを意味します（他のすべてのコンポーネントも0である必要があります）。 負の値を指定すると、頂点は「コーナー」としてマークされます。正の値を指定すると、頂点は「スムーズ」になります。 頂点のコーナーとスムーズは純粋な分離アトリビュートで、他のパスのエンコーディングに影響を与えたり意味を持ったりすることはありません。

絶対値の部分では、ピクセルの種類(Start, Mid, End)と別のフラグ(trivial\_link)が符号化される。

* *0.125*：終了頂点（図形の最後の頂点。常に非簡易リンクです。以下を参照してください）

* *0.25*：開始頂点（図形の最初の頂点。常に非簡易リンクです。以下を参照してください）

* *0.5*：中間の頂点に非簡易リンクがあります

* *1*：頂点の中央に些細なリンクがあります

「簡易リンク」とは（現在のパスの頂点のリストの）前の頂点と次の頂点が左のピクセル(vert\_addr-(0,pixel\_size))に保存され、右のピクセル(vert\_addr+(0,pixel\_size))に保存されることを意味し、「非簡易リンク」とは、これらの頂点の少なくとも1つが他の場所に保存されることを意味します。

+++

+++下
リンクの「三元性」に関係なく、リンクの信頼できる値は下部に保存されます。

<b>XY</b>

このパスの前の頂点のアドレス。 開始頂点の場合は、次の兄弟の頂点を指します。\
if |top[vert\_addr].W| = 1, then bottom[vert\_addr].XY = vert\_addr - (0,pixel\_size)

<b>ZW</b>

このパスの次の頂点のアドレス。 終了頂点の場合は、次の兄弟の頂点を指します。\
if |top[vert\_addr].W| = 1, then bottom[vert\_addr].ZW = vert\_addr + (0,pixel\_size)

+++

## パス情報の読み書き

独自のパス処理ノードを作成する場合は、いくつかのツールがあります。

基本は、[パス頂点プロセッサ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)および[パス頂点プロセッサシンプル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)のノードによって提供されます。このノードは基本的に[ピクセルプロセッサ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)と同じ方法で使用できます。

頂点プロセッサノードが提供するパス（より多くの入力テクスチャ、またはより多くの前後の頂点）以上の機能が必要な場合は、このグラフの実装をコピーすることをお勧めします(<b>Get(&quot;%perVertex&quot;)</b>ノードをカスタム処理で置き換えると仮定します)。

しかし、頂点単位の機能を適用するよりもエイリアンな作業を行いたい場合は、以下の説明で使用できるツールを詳しく説明します。 これらは通常、他のパスノード(*paths\_tools.sbs)*&#x200B;と同じパッケージに含まれる小さなヘルパー関数です。 （これらの関数は、[<b>ライブラリ</b>](../../../../../../interface/the-library/the-library.md)および<b>ノードメニュー</b>には表示されません）。

### &#39;読み取り&#39;関数

`Read`フォルダーには、パスに関する情報を収集するのに便利ないくつかの情報があります。

特定のピクセルに関する情報を提供する場合もあります。 これらはすべて\*top\*部分のサンプルされたFloat4値を入力として受け取ります。 これらの実装を見ると、非常にシンプルです。 そのポイントは、単なる原子ノードよりも多くの意味を伝えることにある。

+++is_header
現在のサンプル値がパスヘッダーまたはドキュメントヘッダーであることを確認します。

+++

+++path_is_closed
パスヘッダーのIs\_Closedフラグ(.Y)をチェックします。 \*既に`is\_header`を含むパスであることを確認し、`current\_pixel\_is\_document\_header`がfalseを返したことを前提としています。

+++

+++is_vertex
現在のサンプリング値が頂点（ヘッダーや空のピクセルではない）であることを確認します。

+++

+++is_start_vertex
\*トップパーツのサンプリングされた\*値が開始頂点かどうかをチェックします（最初に`is\_vertex`をチェックする必要はありません）。

+++

+++is_mid_vertex
\*トップパーツのサンプリングされた\*値が開始頂点でも終了頂点でもない頂点であるかどうかをチェックします（最初に`is\_vertex`をチェックする必要はありません）。

+++

+++is_end_vertex
\*最上位のサンプリングされた\*値が終了頂点かどうかをチェックします（最初に`is\_vertex`をチェックする必要はありません）。

+++

+++is_segment_start
`is\_start\_vertex || is\_mid\_vertex`のショートハンドです。 [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)ベースの処理で、各セグメントを一度に処理する場合に便利です。

+++

+++is_corner
頂点のコーナーフラグを確認してください（最初に`is\_vertex`を確認する必要はありません。回答がtrueの場合は、確実に頂点を確認してください）。 このフラグはまだ公式ノードではサポートされていないことに注意してください。

+++

+++has_trivial_links
頂点の場合は、底部をサンプリングしなくても、前後の頂点の位置を簡単に推定できるかどうかを示します。 （注：頂点以外の場合は、常にfalseが返されます）。

これを直接使用するのではなく、`sample\_next\*`または`sample\_prev\*`のいずれかの関数を使用して処理を行うことをお勧めします。

+++

+++sample_next, sample_prev
トップパーツのサンプリング値`*sampled*`とその位置`*sampled\_position*`を指定して、次の（それぞれ前の）頂点のトップパーツのサンプリング値を返し、この近隣の（トップパーツの）位置にFloat2変数`*next\_sampled\_pos*`を設定します(&lt;戻り値> = SampleColor(next\_sampled\_pos, image0))。 `*input0PixSize*`は、パスのピクセルサイズ(top[(0,0)].YZ)と等しくなければなりません。

現在のピクセル(`*sampled*`)が<b>開始</b>頂点の場合、*sample\_prev*&#x200B;によってこの頂点の次の兄弟が返されます。同様に、それが<b>終了</b>頂点の場合、*sample\_next*&#x200B;によってこの頂点の次の兄弟が返されます（つまり、望むものではない可能性があります）。 この問題を解決するには、以下の`*sample\_next\_advanced*`と`*sample\_prev\_advanced*`を参照してください。

簡単にするために、<b>パス情報はinput0!</b>に格納されていると見なされます。 また、関数のドキュメントの状態とは異なり、`*next\_sampled\_pos*`を事前に宣言する必要はありません。 `*[out]next\_sampled\_pos*`は、この2番目の「戻り値」が存在することを通知するダミーパラメーターです。

`*paths\_trace*` [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)は、3番目のIterateノードのIterationsパラメーターで使用方法の例を確認できます。

![sample_nextの最小限の使用例](paths-format-specifications.resources/paths-spec_fxmap-sample-next_02.png "sample_nextの最小限の使用例")



![プレビューパス(path_trace)でのsample_nextの使用例](paths-format-specifications.resources/paths-spec_fxmap-sample-next_01.png "プレビューパス(path_trace)でのsample_nextの使用例")



+++

+++sample_next_advanced, sample_prev_advanced
これは、閉じたパスでの作業を目的としています。 オープンパスの場合、開始または終了の頂点には兄弟がありません。この場合、両方の関数は同じ隣接する唯一の関数を返します。 複数の兄弟（ネットワークとして接続されたパス）を持つ開始または終了の頂点の場合は、リンクリスト内の次の兄弟の隣接する頂点を返します。

+++

### &#39;書き込み&#39;関数

`Write`フォルダーには、[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)</b>で<b>書き込み可能なFloat4を構築する小さなヘルパーがあります。

実際、[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)は描画する前にRGBとAlphaを掛け合わせるので、実際の値は掛け合わされずに補正されます。 例えば[ピクセルプロセッサー](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)でこれらの関数を使用する場合は、前乗算を自分で再適用するか、カスタムバージョン（ユースケースに合わせて最適化され、使用が簡単なバージョン）を作成することをお勧めします。

+++document_header
指定したパスの数を宣言して、文書ヘッダーの最上部を構築します。

+++

+++document_last_vertex_spec
最後の頂点アドレスを指定する文書ヘッダの\*bottom\*部分を構築する（A.1を参照）。

+++

+++path_header
パス`*nbVertices*`の頂点の数、`*isClosed*`フラグ、および`*pathIndex*`に基づいて、パスヘッダーの上部を構築します。

+++

+++start_vertex、mid_vertex、end_vertex
頂点の最上部を構築し、位置、種類、その他のオプションを適宜設定します。

*mid\_vertex*&#x200B;および&#x200B;*hasTrivialLinks*&#x200B;パラメーターのバージョン情報：適切な値を設定することをお勧めします。ただし、リンクが重要な値であるかどうかを判断できない場合は、安全にfalseに設定できます（生成されたパスの処理に時間がかかります）。

+++

パスのヘッダと頂点に対するボトムパートビルダはありません。どちらもトップ部分への2つのリンクをエンコードするので、この関数は本質的に2つのFloat2からのベクトルFloat4コンストラクタになります。 [Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)を使用して書く場合は、XYZをWで除算することを忘れないでください（WはアドレスのYです。Wをnullにすることはできません）。

[Paths Polygon](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)ノードをホストする&#x200B;<b>*paths\_polygon.sbs* </b>パッケージで、これらの関数の適切な使用例を確認できます。

### パスを処理するメソッド

通常は、ピクセルプロセッサーまたはFx-Mapを使用して、次のような長所と短所のあるカスタム処理を実装します。

+++FX-Map
[Fx-Map](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)ベースのソリューションは通常、パス全体（またはパス）または累積パス（たとえば、デシメーションまたはテッセレーション後に頂点を再パックするなど）のグローバルな知識を必要とする高レベルの操作を実行する場合に推奨されます。 また、この方法は最も簡単です。初めてカスタム処理を行う場合は、Fx-Mapを使用することをお勧めします。ただし、*速度が遅くなる可能性があります*。

そもそもFx-Mapに精通している必要があります。 これに該当しない場合は、[固有のドキュメント](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)を確認してください。

Fx-Mapを使用したパスの読み取りと書き込みの方法について理解するには、<b>*paths\_trace.sbs*</b>&#x200B;の[Preview Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)の実装と、<b>*paths\_polygon.sbs*</b>&#x200B;の[Paths Polygon](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-polygon/paths-polygon.md)を参照することをお勧めします。

+++

+++ピクセルプロセッサー
[ピクセルプロセッサ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)ソリューションは、「ローカル」情報のみが必要な場合に適しています。 ここでは、空間的（要素間の距離）ではなく、位相的（頂点が互いにリンクしている）に「ローカル」を意味します。 これが頂点プロセッサの実装方法です。 通常、ピクセルプロセッサはFx-Mapよりも高速です。これは、各ピクセルの機能が並列に評価され、アクセスされるデータの量が限られているためです。 現在のピクセルしか変更できないため、実装作業の方がはるかに重要な場合があります。

具体的なユースケースに応じて言うべきことはたくさんありますが、最初にすべきことは、自分がどこにいるか確認することです。

上位($pos.y &lt; 0.5)または下位($pos.y > 0.5)のパーツにいますか？ 専用の変数（例： `*isTop*`）で、`*vert.addr*`浮動小数点2を作成して、その値を上部の`*$pos*`、下部の`$pos - (0,0.5)`にすることを推奨します。

*vert.addr*&#x200B;とは何ですか？ これをサンプリングして、何かあるかどうか(W != 0)をチェックし、あるとしたらどうなるかを正確にチェックします。 ヘッダー(W = 0.0625) （`*Read/is\_header*`でチェック）または頂点（`Read/is\_vertex`でチェック） ヘッダーの場合は、ドキュメントヘッダーですか、パスヘッダーですか？ （`*Read/current\_pixel\_is\_document\_header*`を使用して確認できます）。 ヘルパー関数の1つまたは複数を使用して、興味を引くものと一致させます。

+++
