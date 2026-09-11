---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/values-in-substance-compositing-graphs.html"
breadcrumb-title: ''
description: 効率的なマテリアル作成のためのSubstance合成グラフにおける値の種類とデータ処理について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Values in Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance グラフの値
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 2%

---


# Substance グラフの値

バージョン2019.1.0で[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html) エンジン v7が導入されて以来、関数だけでなく、Substanceグラフで値を処理できるようになりました。[](../../function-graphs/function-graphs.md) 値データは、関数（整数、浮動小数、ブール値など）で使用されるデータと同じであり、イメージ全体のピクセル値を表すカラーデータやグレースケールイメージデータとは明確に異なります。 具体的には、値データに言及する場合、*整数 1、整数 2、整数 3と整数 4、浮動小数 1、浮動小数 2、浮動小数 3、浮動小数 4とブーリアン*&#x200B;を意味します。 それぞれが個別のカラーコードを持ち、ほとんど互いに入れ替わりません。

これには、次のような使用例があります。

* 単一値マテリアルプロパティまたは追加のメタデータなどの非画像データを返して処理します。 例えば、マテリアルのIOR値などです。
* ピクセルごとに計算する必要のないグラフの計算を最適化しています（[ピクセルプロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)の代わりに使用できます）。 例えば、ランダムなベタ塗り。
* 画像データを値に処理することによって、1つのノードのプロパティを別のノードにリンクする。 例えば、レベルを調整する画像の最小値と最大値などです。

## 新しい値ノードと入力

次の2つの新しいアトミックノードが値を操作します。

|  |  |
| --- | --- |
| <div><img alt="バリュープロセッサーノードアイコン" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../assets/valueprocessor.png" title="バリュープロセッサーノードアイコン" width="100px"/></div>  <b>[バリュープロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)</b> | [バリュープロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)には、任意の数のグレースケール入力またはカラー入力を指定でき、これらの入力に基づく計算から1つの値を返すことができます。 |
| <div><img alt="値入力ノードアイコン" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../assets/inputnumeric.png" title="値入力ノードアイコン" width="100px"/></div>  **[値の入力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)** | [値入力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)を使用すると、値として明示的に定義されたサブグラフに入力スロットを作成できます。 |

さらに、他のノードでは特定の方法で処理されます。

[出力ノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)は、グレースケールとカラーで行ったように、値の接続を接続すると、値の出力になるように自動的に調整されます。

![出力値ノード](../../assets/values-output.gif "出力値ノード"){width="512px"}

各ノード（[Atomic](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)および[Library](../../compositing-graphs/nodes-reference-for-com/node-library/node-library.md)/Instance）に新しいタブがあり、値の入力を定義できます。

![ノードに入力値を追加しています](../../assets/values-inputs.gif "ノードに入力値を追加しています")

## 値の操作

値の使用は、通常のSubstanceグラフの作業とは少し異なります。

値の接続は、[値プロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)、[値の入力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)、または[サブグラフ](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)からのみ実行できます。 つまり、最初から値の接続を作成する唯一の方法はバリュープロセッサであり、「静的な値」ノードなどはありません。 代わりに、バリュープロセッサを作成し、静的な値を配置して出力として設定することで、同じ結果が得られます。

複数の値、または複数の値のセットやグループを返す場合は、[サブグラフ](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)を作成する必要があります。値プロセッサは単一の値のみを返すことができます。

値が表示される場所または使用中の場所を強調表示するには、値入力（値出力）を持つノードを黄色の太い枠線で強調表示します。

![値の操作](../../assets/yellowhighlight.png "値の操作")
