---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/vector-and-swizzle-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designerの関数グラフでベクトルノードとスウィズルノードを使用すると、ベクトルデータとコンポーネントを操作できます。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Vector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベクトル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 5%

---


# ベクトルノードとスウィズルノード

[ベクトルノード]と[スウィズルノード]では、それぞれ個別のコンポーネントからベクトルノードを構築したり、個別のコンポーネントに分解することができます。これらは、[RGBAマージ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)および[RGBA分割](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md)に似ていますが、関数グラフの場合は似ています。 また、[キャスティング](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)は多くの場合オプションではないため、ベクトルデータ型間の変換の主要な方法でもあります。

## ベクトルノード

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

ベクトルノードを使用すると、コンポーネントの少ない1つまたは複数のベクトル要素を、コンポーネントの多いベクトル要素に結合できます。 ベクターノードには、いくつかの特定のルールや制限があります。

* ベクトルノードには、**2つの入力**&#x200B;しかありません。結果のベクトルに2つ以上のコンポーネントがある場合でも同様です。
* ベクトル入力は&#x200B;**1つの型に限定されません**：入力として小さいコンポーネントを受け取ることができます。
* 結果の出力の順序は、**入力の順序**&#x200B;によって決定されます。

つまり、次の方法が最適に使用されます。

* 2つの2成分ベクトルを接続するか、1成分ベクトルと3成分ベクトルを接続して、ベクトル4を2つの方法で作成します。
* 単一の整数または実数から3または4個の成分を持つベクトルを作成する場合、3成分を持つベクトルに組み合わせる前に、少なくとも1つのベクトル2を組み合わせる必要があります。

コネの順番をよく考えろ。 入力の接続順序を次に示します。

![](../../../../assets/vector-int1.png){width="200px"}

左の例は、最初にInteger(1)を接続し、次にInteger 3を接続します。 結果は以下のとおりです

| 出力 | X | Y | Z | 幅 |
| --- | --- | --- | --- | --- |
| 入力 1 | 0 |  |  |  |
| 入力 2 |  | 1 | 2 | 4 |

![](../../../../assets/vector-int2.png){width="200px"}

「左の例」は、最初の例の入力を入れ替え、最初の例の最初のInteger 3、次にInteger(1)を入れ替えます。

| 出力 | X | Y | Z | 幅 |
| --- | --- | --- | --- | --- |
| 入力 1 | 1 | 2 | 4 |  |
| 入力 2 |  |  |  | 0 |

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-vectorint4.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-vectorint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-vectorint3.png"/></div> |
| --- | --- | --- |
| **ベクトル整数2** | **ベクトル整数3** | **ベクトル整数4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-vectofloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-vectofloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-vectofloat4.png"/></div> |
| **ベクトル浮動小数点2** | **ベクトル浮動小数点3** | **ベクトル浮動小数点4** |

</td>
</tr>
</table>

## Swizzleノード

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

スウィズルノードは、マルチコンポーネントベクトルからコンポーネントを分解または分割し、X、Y、Z、Wのコンポーネントを個別に利用したり、入れ替えることができます。 次のルールと制限が適用されます。

* Swizzleノードの出力は&#x200B;**1つだけです**。
* Swizzleノード&#x200B;**は、正しい型（Intまたは浮動小数）の任意の入力**&#x200B;を受け取ります。

### コンポーネントを分割

Swizzleの最も一般的な使い方は、整数4を4つの個別の整数にブレーキングするなど、コンポーネントを分割するために使用することです。 この場合、制限があるため、4つの個別のスウィズル整数ノードが必要になります。

また、2つのノード2や整数と整数3など、他の種類の分割も可能です。これも、すべての結果には独自の整数が必要であることを念頭に置いています。

### コンポーネントの入れ替え

名前が示すように、Swizzleは、値の順序を変更したり、値を上書きしたりするために使用できます。 X、Y、Z、WからW、Y、X、Zに順序を変更できます。また、X、Y、Z、WからX、X、X、Wなどに値を変更できます。

</td>
<td style="border: 0;" valign="top">

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/fn-vector-swizzleint1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c1_image" src="../../../../assets/fn-vector-swizzleint2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c2_image" src="../../../../assets/fn-vector-swizzleint3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r0-column-c3_image" src="../../../../assets/fn-vector-swizzleint4.png"/></div> |
| --- | --- | --- | --- |
| **スウィズル整数** | **Swizzle** **整数2** | **Swizzle** **整数3** | **Swizzle** **整数4** |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c0_image" src="../../../../assets/fn-vector-swizzlefloat1.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c1_image" src="../../../../assets/fn-vector-swizzlefloat2.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c2_image" src="../../../../assets/fn-vector-swizzlefloat3.png"/></div> | <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid1_items_grid-cell1_position-par_dx_table_row-r2-column-c3_image" src="../../../../assets/fn-vector-swizzlefloat4.png"/></div> |
| **Swizzle** **浮動小数** | **Swizzle** **浮動小数2** | **Swizzle** **浮動小数3** | **Swizzle** **浮動小数4** |

</td>
</tr>
</table>
