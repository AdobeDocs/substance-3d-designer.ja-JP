---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/warnings-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: Substance合成グラフの警告について理解し、一般的な問題やエラーを解決する方法を学びます。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Warnings in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance グラフの警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 1%

---


# Substance グラフの警告

Substance 3D Designerの[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)によって発生する可能性のある警告メッセージとエラーメッセージの一覧を表示し、それぞれの一般的なトラブルシューティング手順を示します。

警告は、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルのグラフリソースに対する警告アイコンのツールヒントと、グラフが読み込まれている場合は、[グラフビュー](../../interface/the-graph-view/the-graph-view.md)の左下隅に表示されます。

## ![（エラー）](../../assets/error.svg)出力ノードが定義されていません

グラフに[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードがありません。

**![(tick)](../../assets/check.svg)ソリューション**

1つ以上の[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードをグラフに追加し、ストリームの最後のノードの出力をそのノードに接続します。

>[!NOTE]
>
> [新しいグラフ](../creating-compositing-gra/creating-a-substance-compositing-graph.md)ダイアログで使用できるグラフテンプレートには、プリセットの出力ノードが用意されており、使用できます。

![&#39;出力ノードが定義されていません&#39;という警告を修正する](../../assets/warnings-comp-output.gif "&#39;出力ノードが定義されていません&#39;という警告を修正する"){width="512px"}

### ![（エラー）](../../assets/error.svg) *[x]*&#x200B;パラメーターの関数に警告があります

指定されたノードの指定されたパラメーターに適用された[関数グラフ](../../function-graphs/function-graphs.md)に、少なくとも1つの警告があります。\
nodeパラメーターは、テンプレートNode[Parameter]に続くノードラベルの後の角かっこ内に指定します。

E.g. 均一カラー[出力カラー]、ピクセルプロセッサー[ピクセル関数単位]

**![(tick)](../../assets/check.svg)ソリューション**

[グラフビュー](../../interface/the-graph-view/the-graph-view.md)でラベルと警告バッジの警告を発しているノードを見つけて選択し、[プロパティ](../../interface/properties/properties.md)パネルでプロパティを表示します。 警告を出しているパラメーターを見つけ、**[関数の編集]**&#x200B;ボタンをクリックして、その関数を開きます。

次に、グラフビューの左下隅に表示されている警告を評価して、問題を解決します。 関数グラフで報告された警告のトラブルシューティングについては、[関数グラフの警告](../../function-graphs/warnings-function-graphs/warnings-in-function-graphs.md)ページを参照してください。

![&#39;パラメーター関数に警告があります&#39;警告を修正](../../assets/warnings-comp-param-function.gif "&#39;パラメーター関数に警告があります&#39;警告を修正")

### ![（エラー）](../../assets/error.svg)参照されたデータに警告があります

ノードが参照するリソースに1つ以上の警告があります。 リソースを参照するノードを次に示します。

* [グラフインスタンス](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ノードはグラフを参照しています
* [ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードは[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)を参照しています
* [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)ノードが[SVGリソース](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)を参照しています
* [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)ノードが[フォントリソース](../../resources/font-resource/font-resource.md)を参照しています

**![(tick)](../../assets/check.svg)ソリューション**

[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルで、参照されているリソースを探し、リソースによって発生したすべての警告のトラブルシューティングを行います。

* グラフについては、このページの他の項目を参照してください
* 他の種類のリソースについては、[依存関係からの警告](../../resources/warnings-from-dep/warnings-from-dependencies.md)ページを参照してください

![&#39;参照されたデータに警告があります&#39;の警告を修正する](../../assets/warnings-comp-referenced-data.gif "&#39;参照されたデータに警告があります&#39;の警告を修正する")

### ![（エラー）](../../assets/error.svg)参照リソースが見つかりません

[Substance 3D](https://www.adobe.com/jp/products/substance3d/3d-augmented-reality.html)ファイル(SBS)に保存されたパスに、ノードが参照するリソースが見つかりませんでした。 リソースを参照するノードを次に示します。

* [グラフインスタンス](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ノードはグラフを参照しています
* [ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードは[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)を参照しています
* [SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)ノードが[SVGリソース](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)を参照しています
* [Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)ノードが[フォントリソース](../../resources/font-resource/font-resource.md)を参照しています

**![(tick)](../../assets/check.svg)ソリューション**

[グラフインスタンス](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ノードの場合

ソースグラフが、**Package**&#x200B;属性に保存されたパスにあるパッケージに存在することを確認してください。\
存在しない場合は、インスタンスノードを削除し、有効なパッケージを参照しているインスタンスノードに置き換えます。 または、インスタンスノードが参照するパッケージとグラフを再作成し、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルでホストパッケージにRMBをクリックして、コンテキストメニューの&#x200B;**再読み込み**&#x200B;オプションを選択することで、ホストパッケージを再読み込みすることもできます。

[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)、[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)または[テキスト](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)ノードの場合

エクスプローラーパネルで参照されているリソースを検索し、**ファイルパス**&#x200B;属性に保存されている場所にリソースが存在することを確認してください。\
表示されない場合は、エクスプローラーのリソース項目で「 RMB 」をクリックし、コンテキストメニューの&#x200B;**再配置…**&#x200B;オプションを選択して、そのリソースの新しい有効なターゲットファイルを設定します。

![&#39;参照リソースが見つかりません&#39;という警告を修正する](../../assets/warnings-comp-referenced-resource.gif "&#39;参照リソースが見つかりません&#39;という警告を修正する")

### ![（エラー）](../../assets/error.svg)テキストノードは無効なフォントを使用しています

[Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)ノードは、正しく読み込みまたは解析できないフォントを参照しています。

<b>![(tick)](../../assets/check.svg)ソリューション</b>

[Text](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)ノードを選択し、<b>Font</b>プロパティの値をメモします。 システムでそのフォントのソースファイルを探し、それが&#x200B;*正常*&#x200B;であることを確認します（例：テキストエディターなどの別のアプリケーションで使用する）。 必要に応じて、正常なフォントファイルでフォントを置き換えるか、テキストノードを別のフォントに切り替えます。
