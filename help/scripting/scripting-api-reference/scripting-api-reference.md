---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/scripting-api-reference.html"
breadcrumb-title: ''
description: プラグイン開発用の完全なSubstance 3D Designer PythonスクリプティングAPIリファレンスにアクセスします。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Scripting API reference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スクリプトAPIリファレンス
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1251'
ht-degree: 0%

---


# スクリプトAPIリファレンス

このページでは、APIの主な概念について説明します。

詳細については、<b>ヘルプ/Python APIドキュメント…</b>でアクセスできるアプリケーションに付属のドキュメントを参照してください。このドキュメントでは、モジュール名（以下の括弧内に記載）を<b>クイック検索</b>して、定義を簡単に見つけることができます。

## コンテキスト

コンテキスト(*Context*)オブジェクトは、API</b>への<b>メインエントリポイントです。 これは、ユーザーが&#39;*sd*&#39;モジュールのメソッド&#39;<b>*getContext()*</b>&#39;を使用して最初に取得するときに作成されます。

このオブジェクトを使用すると、アプリケーション</b> (*SDApplication*)オブジェクトを<b>取得できます。

## アプリケーション(SDApplication)

アプリケーション(*SDApplication*)は、<b>次のようなメインAPIマネージャーへのアクセス</b>を許可するオブジェクトです。

* アプリケーションのすべての<b>パッケージ</b>を管理する<b>パッケージ</b>マネージャー(*SDPackageMgr*);
* アプリケーションのすべての<b>モジュール</b>を管理する<b>モジュール</b>マネージャー(*SDModuleMgr*)。
* アプリケーションのウィンドウに<b>メニューとドック</b>を作成できる<b>UI </b>マネージャー(*SDUIMgr*)。

特定のイベントが発生したときに呼び出されるアプリケーションに<b>コールバック</b>を登録できます。

## パッケージマネージャー(SDPackageMgr)

このオブジェクトは、すべてのアプリケーションの<b>パッケージ</b>を管理します。 パッケージは&#39;<b>*エクスプローラー*</b>&#39;コンポーネントに表示されます。

これにより、次のことが可能になります。

* 新しいパッケージを<b>作成</b>します。
* パッケージの<b>読み込み/アンロード</b>;
* パッケージを<b>保存</b>;
* パッケージを<b>検索</b>します。

## パッケージ(SDPackage)

パッケージ(*SDPackage*)は、<b>リソースのコレクション</b> (*SDResource*)です。

パッケージのコンテンツは、&#39;*SDPackageMgr*&#39;オブジェクトを介して、<b>.sbs</b>拡張子を持つファイルに<b>格納</b>できます。 このオブジェクトを使用すると、<b>特定の</b>リソースを取得できます。

特定のリソースを<b>作成</b>するには、関連するオブジェクトの静的メソッド(例： &#39;*SDSBSCompGraph.sNew()*&#39;)を参照してください。

パッケージには、メタデータ辞書(SDMetadataDict)も含まれます。 メタデータ[の詳細については、](../../package-metadata/package-metadata.md)を参照してください。

## リソース(SDResource)

リソース(*SDResource*)は、別のリソースから<b>参照</b>できるオブジェクトです。

複数のリソース<b>型</b>があります：

* フォルダー(*SDResourceFolder*);
* グラフ(*SDGraph*);
* ビットマップ(*SDResourceBitmap*);
* SVG画像(*SDResourceSVG*);
* フォント(*SDResourceFont*);
* シーン(*SDResourceScene*);
* BSDF測定(*SDResourceBSDFMeasurement*);
* ライトプロファイル(*SDResourceLightProfile*)。

リソースは、次の下の静的メソッド&#39;*sNew()*&#39;から<b>作成</b>できます：

* 包み。
* フォルダー。

1つのリソースに複数の<b>プロパティ</b> (*SDProperty*)を設定できます。

## UIマネージャー(SDUIMgr)

UIマネージャーを使用すると、Substance Designerのメインウィンドウ（<b>メニュー</b>、<b>ドック</b>など）に<b>ユーザーインターフェイス要素を作成</b>でき、ユーザーインターフェイス関連のイベントが発生したときに<b>コールバック</b>を呼び出すことができます。

さらに、UIマネージャーは、アクティブなグラフの<b>現在のアクティブなグラフ</b>と<b>選択範囲</b>にアクセスできます。

## グラフ(SDGraph)

グラフ(*SDGraph*)は、次を含むオブジェクトです。

* <b>ノード</b>(*SDNode*);
* <b>グラフオブジェクト</b> (*SDGraphObjects*);
* <b>プロパティ</b>(*SDProperty*)。

グラフには4つの種類があります。

* Substanceグラフ(*SDSBSCompGraph*)
* Substance関数グラフ(*SDSBSFunctionGraph*)
* SubstanceFXMapグラフ(*SDSBSFxMapGraph*)

グラフには1つまたは複数の<b>出力</b>ノードを含めることができます。 出力ノードは、グラフの<b>結果</b>を表します。

メソッド&#39;*getNodeDefinitions()*&#39;を使用すると、グラフで使用可能なすべてのノードを<b>取得</b>できます。

メソッド&#39;*newNode()*&#39;を使用して、新しいノードを<b>作成</b>できます。

メソッド&#39;*newInstanceNode()*&#39;を使用して、リソース(*SDResource*)から新しい<b>インスタンス</b>ノードを作成できます。

## ノード(SDNode)

ノード(*SDNode*)は、オブジェクトに対して実行された<b>操作</b>を表します。

以下から作成できます。

* <b>定義</b> (*SDDefinition*) (&#39;*SDGraph.newNode()&#39;*&#x200B;を参照);
* <b>リソース</b> (*SDResource*) (&#39;*SDGraph.newInstanceNode()&#39;*&#x200B;を参照)。

1つのノードに複数の<b>プロパティ</b>を設定できます。

ノードに複数の<b>型</b>があります：

* *<b>SDSBSCompNode</b>*: Substance グラフのノード(*SDSBSCompGraph*);
* *<b>SDSBSFunctionNode</b>*: Substance 関数グラフのノード(*SDSBSFunctionGraph*);
* *<b>SDSBSFxMapNode</b>*: Substance FXMap Graph (*SDSBSFxMapGraph*)のノード。

## グラフオブジェクト(SDGraphObjects)

グラフオブジェクト(*SDGraphObject*)は、<b>追加情報</b>をグラフに追加するオブジェクトですが、グラフの評価処理中に&#x200B;<b>*考慮されない*&#x200B;オブジェクトです。</b>

グラフオブジェクトには<b>3種類</b>があります：

* <b>Pin</b> (*SDGraphObjectPin*)
* <b>コメント</b> (*SDGraphObjectComment*)
* <b>フレーム</b> (*SDGraphObjectFrame*)

これらのオブジェクトを<b>作成</b>する方法の詳細については、これらのオブジェクトの静的メソッド&#39;*sNew()*&#39;を参照してください。

## プロパティ(SDProperty)

プロパティ(*SDProperty*)は、<b>別のオブジェクト</b> （グラフ、ノード、リソースなど）のプロパティを<b>説明</b>するオブジェクトです。

特定の<b>カテゴリ</b> (*SDPropertyCategory*)に属しています：

* <b>入力</b>:オブジェクトの入力プロパティを分類します。これは通常<b>現在のオブジェクトによって実行される操作</b>に影響を与えます。
  * 例：Substanceグラフの均一な色ノードのプロパティ&#39;*color*&#39;は入力プロパティです。
* <b>出力</b>:オブジェクトの出力プロパティを分類します。 オブジェクトの<b>result</b>を識別するために使用されます。
* <b>注釈</b>:オブジェクトによって実行された操作</b>に影響を与えない&#x200B;<b>*プロパティを分類します*。
  * 例：グラフの&#39;*label*&#39;は、グラフの計算に影響を与えないため、注釈プロパティです。

次の<b>メンバー</b>が含まれています：

* <b>Id</b>：このカテゴリのコンテキスト内のプロパティの識別子；
* <b>型</b>：現在のプロパティでサポートされている型です。 一部のプロパティは&#x200B;*複数*&#x200B;の型をサポートできます： &#39;*int*&#39;、&#39;*float*&#39;など。
  * 例： &#39;*sbs::function::add*&#39;ノードの入力プロパティは、さまざまな型をサポートできます： &#39;*int&#39;*、&#39;*int2&#39;*、&#39;*int3&#39;*、&#39;*int4&#39;*、&#39;*float&#39;*、&#39;*float2&#39;*、&#39;*float3&#39;*、&#39;*float4&#39;など；*
* <b>カテゴリ</b>:プロパティが属するカテゴリ（入力、出力、注釈）;
* <b>ラベル</b>:プロパティのラベルです。表示&#x200B;*のみ*&#x200B;に使用されます。
* <b>説明</b>:プロパティの説明；
* <b>DefaultValue</b>:デフォルト値；
* <b>IsConnectable</b>：このプロパティで接続(*SDConnection*) *を実行できるかどうかを*&#x200B;示します。
* <b>isReadyOnly</b>:プロパティが読み取り専用かどうかを示します。 trueの場合、関連付けられた値は&#x200B;*変更不可*&#x200B;になります。
* <b>isVariadic</b>: trueの場合、このプロパティはオブジェクト上で&#x200B;*multiple*&#x200B;プロパティとして表されます。
* <b>isPrimary</b>：指定されたプロパティが、他のプロパティを制御する&#x200B;*プリンシパル*&#x200B;プロパティであるかどうかを示します。 *注意：*&#x200B;これは、Substance *合成*&#x200B;ノード(*SDSBSCompNode*)に固有です。

例：

* &#39;*sbs::compositing::input*&#39;ノードのプロパティ：

<table data-preserve-html="true"><colgroup><col style="width: 276.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing:：入力</th></tr><tr><td style="text-align: left;"><strong>入力</strong></td><td style="text-align: left;"><strong>注釈</strong></td><td style="text-align: left;"><strong>出力</strong></td></tr><tr><td>$outputsize</td><td>ラベル</td><td><p>unique_filter_output (CONNECTABLE)</p></td></tr><tr><td>$format</td><td>description</td><td><br/></td></tr><tr><td>$pixelsize</td><td>identifier</td><td><br/></td></tr><tr><td>$pixelratio</td><td>userdata</td><td><br/></td></tr><tr><td>$tiling</td><td>グループ</td><td><br/></td></tr><tr><td>$randomseed</td><td>visibleif</td><td><br/></td></tr><tr><td><p>bitmapresourcepath</p></td><td>用途</td><td><br/></td></tr></tbody></table>

* &#39;*sbs::compositing::blend*&#39;ノードのプロパティ：

<table data-preserve-html="true"><colgroup><col style="width: 278.0px;"/><col style="width: 129.0px;"/><col style="width: 283.0px;"/></colgroup><tbody><tr><th colspan="3" style="text-align: center;">sbs::compositing:：ブレンド</th></tr><tr><td style="text-align: left;"><strong>入力</strong></td><td style="text-align: left;"><strong>注釈</strong></td><td style="text-align: left;"><strong>出力</strong></td></tr><tr><td>$outputsize</td><td><br/></td><td>unique_filter_output (CONNECTABLE)</td></tr><tr><td>$format</td><td><br/></td><td><br/></td></tr><tr><td>$pixelsize</td><td><br/></td><td><br/></td></tr><tr><td>$pixelratio</td><td><br/></td><td><br/></td></tr><tr><td>$tiling</td><td><br/></td><td><br/></td></tr><tr><td>$randomseed</td><td><br/></td><td><br/></td></tr><tr><td>source.connector （接続可能）</td><td><br/></td><td><br/></td></tr><tr><td><p>destination.connector （接続可能）</p></td><td><br/></td><td><br/></td></tr><tr><td>opacity.connector （接続可能）</td><td><br/></td><td><br/></td></tr><tr><td>opacitymult</td><td><br/></td><td><br/></td></tr><tr><td colspan="1">blendingmode</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">colorblending</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr><tr><td colspan="1">maskrectangle</td><td colspan="1"><br/></td><td colspan="1"><br/></td></tr></tbody></table>

## 型(SDType)

型(*SDType*)には、次のような値<b>型</b>の情報が含まれています：

* <b>Id</b>：型の識別子；
* <b>修飾子</b>: &#39;*SDTypeModifier&#39;* <b>enum</b>値の1つである型修飾子：
  * *自動*;
  * *均一*：値は操作ごとに&#x200B;*一度*&#x200B;評価されます。
  * *変化*：値は操作ごとに&#x200B;*複数回*&#x200B;評価されます（例：各テクセル）。

次のように複数のタイプが定義されています。

* <b>列挙</b> (*SDTypeEnum*): <b>列挙</b>型とそのすべてのプロパティを説明します。
* <b>構造体</b> (*SDTypeStruct*): <b>構造体</b>型がすべてのプロパティと共に記述されています。
* <b>配列</b> (*SDTypeArray*): <b>配列</b>を記述します。
* など

詳細については、Substance Designerの&#x200B;*Python APIドキュメント*&#x200B;を参照してください。

## 値(SDValue)

値(*SDValue*)は、*基本型*&#x200B;の値を<b>カプセル化</b>するオブジェクトです。

例：

* &#39;<b>*SDValueInt*</b>&#39;オブジェクトは、&#39;*int*&#39;値をカプセル化します。
* &#39;<b>*SDValueFloat4*</b>&#39;オブジェクトは、&#39;*float4*&#39;値をカプセル化します。
* など

通常、&#39;<b>get()</b>&#39;メソッドを使用して基本型の値を<b>取得</b>できますが、返された&#39;*SDValue&#39;*&#x200B;の&#x200B;*型*&#x200B;に依存する場合もあります。

## 接続(SDConnection)

接続(*SDConnection*)は、2つの異なる<b>ノード</b>の2つの異なる<b>プロパティ</b>間の<b>リンク</b>を表します。

次の情報が含まれます。

* <b>ターゲットノード</b>;
* ターゲットノードの<b>ターゲットプロパティ</b>;

すべての<b>接続操作</b>は、ノードで実行されます：

* <b>新しい接続を作成しています</b>。&#39;*SDNode.newPropertyConnection()*&#39;を参照してください。
* <b>既存の接続を削除しています</b>。&#39;*SDNode.deletePropertyConnection()*&#39;を参照してください。
* <b>プロパティの接続を取得</b>しています。&#39;*SDNode.getPropertyConnections()*&#39;を参照してください。

## モジュール(SDModule)

モジュールは<b>定義と型のコレクション</b>です。

これにより、作成可能なノード上の情報だけでなく、列挙や構造に関するすべての情報を簡単に取得できます。

次の情報が含まれます。

* モジュールマネージャー(*SDModuleMgr*)のコンテキストで一意の<b>ID</b> (*Id*);
* <b>定義</b>の一覧(*SDDefinition*);
* <b>型</b>の一覧(*SDType*)。

## 定義(SDDefinition)

定義(*SDDefinition*)オブジェクトには、<b>プロパティ</b> （&#39;*SDNode&#39;*&#x200B;など）に基づく特定の<b>オブジェクト</b>の定義に関する情報が含まれています。

次の情報が含まれます。

* <b>Id</b>：定義の識別子；
* <b>ラベル</b>：定義のラベル；
* <b>説明</b>：定義の説明；
* <b>プロパティ</b>：使用可能なすべてのプロパティ&#x200B;*カテゴリ* (*SDPropertyCategory*)のプロパティ。
