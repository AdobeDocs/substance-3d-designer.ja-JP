---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/value-processor.html"
breadcrumb-title: ""
description: 値プロセッサノードを使用すると、カスタム調整の数学的な演算を使用してテクスチャ値を処理および操作できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Value processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: バリュープロセッサー
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '156'
ht-degree: 3%
---

# バリュープロセッサー

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![Atomicノード：値プロセッサ](value-processor.resources/comp_valueprocessor_1.png "Atomicノード：値プロセッサ"){width="100%"}

<b>In:</b>個のアトミックノード

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

[Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)を計算し、その結果を出力します。

[ピクセルプロセッサ](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)に相当しますが、ピクセルごとに関数を計算するのではなく、1つの値を計算し、[Substanceグラフで使用できるようにする](../../../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)点が異なります。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="value-processor.resources/value-processor-tooltip.gif" alt="value-processor tooltip" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>


>[!TIP]
>
> このノードは、[Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)について学習するための開始点として適しています。
> 
> また、このタイプのグラフを使用して数学的な演算を実行することは、このノードから何かを得るために必須です。


## パラメーター

|  |  |
| --- | --- |
| <b>値プロセッサ関数</b> *任意の使用可能な値の種類* | [Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)は、出力値を計算するために評価されました。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力画像#</b> *グレースケール/カラー* | [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)または[Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)ノードを使用して、指定されたインデックスの入力の値にアクセスします。 |


## 例

*近日公開。*
