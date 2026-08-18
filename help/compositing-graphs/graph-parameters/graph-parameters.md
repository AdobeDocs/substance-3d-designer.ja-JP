---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/graph-parameters.html"
breadcrumb-title: ''
description: Substance 3D Designerでグラフパラメーターを作成および管理し、マテリアルのプロパティやビヘイビアーを制御する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Graph parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラフパラメーター
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1503'
ht-degree: 0%

---


# グラフパラメーター

<b>Substanceグラフ</b>の標準パラメーターについて説明します。

グラフには、変更可能なパラメータがいくつかあります。 グラフの&#x200B;*空きスペース*&#x200B;をクリックするか、<b>エクスプローラー</b>パネルの&#x200B;*グラフ項目*&#x200B;を選択して見つけることができます。 その後、パラメーターがパラメータービューに表示されます。

<a name="base-parameters"></a>

## ベースパラメーター

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

このセクションには、*含まれているすべてのノード*&#x200B;に影響するパラメーターが含まれています。

実際、&#39;親に対する相対&#39; [継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定された基本パラメーターを持つこのグラフのすべてのノードは、*グラフの*&#x200B;基本パラメーターから値を取得します。

一方、グラフのベースパラメータの値は、そのグラフが使用されているコンテキストによって異なります。

</td>
<td style="border: 0;" valign="top">

![基本パラメーター](../../assets/doc-graph-props-base-params.png "基本パラメーター"){width="512px" zoomable="yes"}

</td>
</tr>
</table>

例えば、グラフが別のグラフでインスタンスノードとして使用されている場合、そのベースパラメーターはデフォルトで「入力に対して相対的」継承方法を使用します。 つまり、プライマリ入力に接続されているノードから値を取得します。 （[オーバーライド](#input-parameters)されていない場合）

ほとんどの場合、継承は、これらの値を定義し、グラフ全体でこれらの値がどのように変化するかを決定する上で重要な役割を果たします。 そのため、これらのパラメーターを使用する前に、[Substanceグラフの継承](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)について十分に理解しておくことを強くお勧めします。

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|:---------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>出力サイズ</b> | このパラメーターを使用すると、グラフ内の画像の&#x200B;*基本解像度*&#x200B;を選択できます。  次を使用します <div><img data-preserve-html="true" height="22" src="../../assets/props-output-size-lock.jpg"/></div> サイズを調整するときに、高さの値と幅の値が一致して画像の正方形を維持するためのロックボタン。<br><br>*デフォルト: (0,0) – 親を基準にする* [詳細](../../compositing-graphs/output-size/output-size.md) |
| <b>出力形式</b> | グラフの&#x200B;*基本ビット深度*&#x200B;を次のオプションから選択できます：<ul data-preserve-html="true"><li data-preserve-html="true">8ビット</li><li data-preserve-html="true">16ビット</li><li data-preserve-html="true">HDR低精度16F（16ビット浮動小数点）</li><li data-preserve-html="true">HDR高精度32F（32ビット浮動小数点）</li></ul>*既定： 8 Bit/チャンネル – 親に対する相対* |
| <b>ピクセルサイズ</b> | ピクセルサイズを定義します。 **幅**&#x200B;と&#x200B;**Height**&#x200B;の両方の値を&#x200B;**1**&#x200B;に設定しておくことをお勧めします。*既定： (1,1) – 親に相対的* |
| <b>タイルモード</b> | グラフの基本&#x200B;*タイルモード*&#x200B;を次のオプションから定義します：<ul data-preserve-html="true"> <li data-preserve-html="true">タイリングなし</li> <li data-preserve-html="true">水平方向タイリング</li> <li data-preserve-html="true">垂直方向タイリング</li> <li data-preserve-html="true">水平および垂直(H+V)タイリング</li> </ul>*既定： HとVの分割 – 親を基準とする* |
| <b>ランダムシード</b> | グラフのベース&#x200B;*ランダムシード*&#x200B;を定義します。  次を使用します <div><img data-preserve-html="true" height="22" src="../../assets/prop-randomise.jpg"/></div> 新しいランダム値をランダムシードに割り当てるボタン。<br><br>*既定： 0 – 親に対する相対* |

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<a name="attributes"></a>

## 属性

<b>属性</b>セクションには、グラフの&#x200B;*メタデータ*&#x200B;が含まれています。このメタデータは、作成者のデザインに従ってグラフを&#x200B;*識別*、*分類*&#x200B;および&#x200B;*適用*&#x200B;するための情報を提供します。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![グラフの属性](../../assets/doc-graph-props-attributes.png "グラフの属性"){zoomable="yes"}

</td>
</tr>
</table>

+++属性のリスト

|                      |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
|:---------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **識別子** | これはグラフの名前であり、*一意*&#x200B;である必要があります。同じパッケージ内に同じ<b>識別子</b>を持つ複数のグラフを含めることはできません。 [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルでグラフの&#x200B;*名前*&#x200B;として使用されています。<br><br>*注意：*&#x200B;識別子&#x200B;*を空の文字列*&#x200B;にすることはできません。 空の文字列は自動的に`_`または`Substance_graph`に置き換えられます。 この値には次の文字を&#x200B;*のみ*&#x200B;使用できます： *`A-Z, 1-9, @$%[{]}_-`.* 承認されていない文字は自動的に`_`で置き換えられます。<br><br>*既定： New\_Graph、またはグラフ作成時にユーザーが設定します* |
| **ラベル** | *ユーザー向け*&#x200B;のシナリオ（例： [ライブラリ](../../interface/the-library/the-library.md)エントリまたは[インスタンスノード](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ラベル）で読みやすさを向上させるために、<b>ID</b>の代わりに<b>Label</b>を使用して&#x200B;*名前*&#x200B;のグラフを表示します。  ラベルは&#x200B;*一意ではない*&#x200B;ことができ、特殊文字を含めることができます。<br><br>*ヒント：*&#x200B;グラフの名前を変更する場合（例： [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)）、そのラベルも変更できます！<br><br>*既定：空* |
| **型** | <b>型</b>は、[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)の目的を定義するために使用されます。 主に、[&#39;送信&#39;相互運用性の機能](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md) [.](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/send-to-215286290.html)を対象としています |
| **マテリアルモデル** | グラフのマテリアルモデルを設定すると、モデルに一致するシェーダ&#x200B;*が利用可能な場合、3Dビューで適切なシェーダが使用されるようになります。<br>例：* 3Dビューで`OpenPBR v1.1`マテリアルモードでグラフを表示すると、ターゲットマテリアルの`OpenPBR Surface`シェーダが選択されます。<br><br>一致するシェーダが見つからない場合、またはグラフのモデルが`Undefined`に設定されている場合、3Dビューのターゲットマテリアルに使用されるシェーダは&#x200B;*変更されていません*&#x200B;です。 |
| **物理サイズ** | この値は、*物理ワールド*&#x200B;のテクスチャの次元をX （長さ）、Y （幅）、Z (Height)で指定します。 したがって、グラフで生成されるマテリアルと本質的に関連しています。 例えば、物理サイズを使用して、<b>2Dビュー</b>と<b>3Dビュー</b>でテクスチャを正しい比率で表示できます。<br><br>*ヒント：* Substanceグラフの物理サイズは、$physicalsize [組み込み変数](../../function-graphs/variables/system-variables/system-variables.md)を使用して、グラフ内の任意のSubstanceに適用されたノード関数グラフでFloat3値として取得できます。<br><br>*注意：* **Z**&#x200B;の値2&rbrace;は、現在、*には0 **3Dビュー**。*&#x200B;したがって、マテリアルの&#x200B;**Heightスケール**&#x200B;の値は、**heightscale**&#x200B;の使用量に設定された&#x200B;**Output**&#x200B;ノードを使用するか、直接&#x200B;**マテリアルのプロパティ**&#x200B;で設定する必要があります。<br><br>*既定： (0,0,0)* |
| **アイコン** | この領域では、*アイコン*&#x200B;を定義できます。このアイコンは、<b>ライブラリ</b>でこのグラフのエントリを<b>SBS</b>および<b>SBSAR</b>として表示するために使用されます。 このアイコンは、[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)の<b>棚</b>など、他の状況でも使用されます。 この領域には次のオプションがあります。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>参照</b>:アイコンとして使用する<i>既存のイメージ</i>のシステムファイルを参照できます</li> <li data-preserve-html="true"><b>生成</b>: <b>PBR レンダリング</b>ノードの<i>組み込みプリセット</i>を使用してアイコンを生成します</li> <li data-preserve-html="true"><b>貼り付け</b>：現在<i>クリップボード</i>にある画像データをアイコンとして貼り付けることができます</li> <li data-preserve-html="true"><b>削除</b>：このオプション<i>既存のアイコンを削除</i>し、アイコンスロット<i>を空のままにします</i></li> </ul>*注意：* **生成**&#x200B;オプションでは、**物理サイズ**&#x200B;を使用して、ディスプレイスメント効果の&#x200B;**PBR レンダリング**&#x200B;の&#x200B;**Heightスケール**&#x200B;を特定します。 **physicalsize**&#x200B;の使用量に設定された&#x200B;**Output**&#x200B;ノードがグラフに存在する場合、この出力が使用されます。 このような出力が存在しない場合、グラフの&#x200B;**Attributes**&#x200B;の値が&#x200B;*代わりに*&#x200B;使用されます。 属性の値が(0,0,0)の場合は、0.1の&#x200B;*プリセット値*&#x200B;が使用されます。<br><br>*注意：* *アイコン*&#x200B;が定義されていない場合は、代わりにグラフの&#x200B;*最初の画像出力*&#x200B;が使用されます。<br><br>*既定値：空* |
| **パッケージ** | このグラフが属する&#x200B;**パッケージ**&#x200B;の&#x200B;*絶対*&#x200B;ファイル名。**フォルダー**&#x200B;ボタンを使用すると、この場所で新しいシステム&#x200B;*ファイルブラウザーウィンドウ*&#x200B;を開くことができます。*既定：パッケージのファイル名/パッケージが保存されていない場合は空になります* |
| **SBSARで公開されました** | これは、グラフとその出力を、グラフの&#x200B;**パッケージ**&#x200B;から公開された&#x200B;**SBSAR**&#x200B;ファイルで&#x200B;*表示*&#x200B;できるかどうかを制御します。これは、パッケージ内の一部のグラフがパッケージのメイングラフに&#x200B;*サブグラフ*&#x200B;としてのみ使用され、**SBSAR**&#x200B;に&#x200B;*が表示されない*&#x200B;場合に便利です。*既定：はい* |
| **ライブラリに表示** | パッケージが&#x200B;**ライブラリ**&#x200B;によって&#x200B;*監視*&#x200B;されている場所に保存されている場合に、**ライブラリ**&#x200B;でグラフを&#x200B;*表示*&#x200B;するかどうかを制御します。*既定：プロジェクト設定の[ライブラリ]タブで設定します* |
| **説明** | グラフの&#x200B;*説明テキスト*&#x200B;です。このグラフは、**Library**&#x200B;のグラフエントリの&#x200B;*tooltip*、このグラフの&#x200B;**Instance**&#x200B;ノード、および既存の&#x200B;**Software Integration**&#x200B;を持つSubstanceに表示されます。*既定：空* |
| **カテゴリ** | このフィールドでは、**ライブラリ**&#x200B;でこのグラフアイテムの&#x200B;*カテゴリ*&#x200B;を設定できます。*既定：空* |
| **作成者** | このフィールドを使用して、作成者の&#x200B;*名前*&#x200B;を入力できます。*既定：空* |
| **作成者URL** | このフィールドでは、*URL*&#x200B;を入力できます（例：作成者のWebサイト）。*既定：空* |
| **タグ** | このフィールドを使用して独自の&#x200B;*タグ*&#x200B;を追加し、グラフの&#x200B;*検索性*&#x200B;と&#x200B;*検出可能性*&#x200B;を向上させることができます。*既定：空* |
| **グループ** | ノードメニューの項目のグループ化を有効にします。 共通の「グループ」値を共有するグラフやビットマップなどのリソースは、グループの名前が付けられたセクションにグループ化されます。 *既定：空* |
| **ユーザーデータ** | このフィールドを使用して、独自の追加データを追加できます。 これは、サードパーティソフトウェアでのカスタム統合に便利です。 Substance 3D PainterおよびSamplerでは、このuserdataを使用して特定のビヘイビアーを設定します。*デフォルト：空* |
| **テンプレートデータ** | Substanceグラフをテンプレートとして使用する場合、この属性は[テンプレートのcategoryとsubtitle](../../compositing-graphs/creating-compositing-gra/creating-a-substance-compositing-graph.md)を設定します。 2つのサブタイトルは完全に区切られています： &lt;category>;&lt;subtitle> <br><br>*Default: Empty* |

+++
<a name="input-parameters"></a>

## 入力パラメーター

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[公開されたパラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)を含む、グラフに固有のすべてのパラメーターは[管理](../../compositing-graphs/manage-parameters/manage-parameters.md)されており、ここで編集およびプレビューできます。

[パラメータープリセット](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)は、一部またはすべてのパラメーターに対して作成することもできます。

</td>
<td style="border: 0;" valign="top">

![入力パラメーター](../../assets/doc-graph-props-input-parameters.png "入力パラメーター"){zoomable="yes"}

</td>
</tr>
</table>

+++基本パラメータをオーバーライドする
別のグラフのグラフを[インスタンスノード](../creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)として使用する場合、その新しいインスタンスノードの基本パラメーターの既定値を制御できます。

「入力パラメーター」セクションの上部にあるハンバーガーメニューを開き、「ベースパラメーターのオーバーライド」サブメニューに移動して、任意のデフォルト値を設定するベースパラメーターを選択します。

選択したパラメーターのエディターが、グラフ入力パラメーターのリストの上に表示されます。 その後、必要に応じてそれらの値と[継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)を調整できます。

+++

>[!IMPORTANT]
>
> [コンテキスト内の編集](../../interface/preferences-window/preferences-window.md)を使用している場合、<b>プレビュー</b>および<b>プリセット</b>タブが無効になります。

<a name="inputs"></a>

## 入力

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

この部分には、グラフのすべての[Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)ノードが一覧表示されます。

各項目の一番左にあるハンドルをドラッグ&amp;ドロップして、項目を並べ替えることができます。

</td>
<td style="border: 0;" valign="top">

![入力](../../assets/doc-graph-props-inputs.png "入力"){zoomable="yes"}

</td>
</tr>
</table>

<a name="outputs"></a>

## 出力

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

この部分では、すべてのグラフの[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードです。

各項目の一番左にあるハンドルをドラッグ&amp;ドロップして、項目を並べ替えることができます。

</td>
<td style="border: 0;" valign="top">

![出力](../../assets/doc-graph-props-outputs.png "出力"){zoomable="yes"}

</td>
</tr>
</table>
