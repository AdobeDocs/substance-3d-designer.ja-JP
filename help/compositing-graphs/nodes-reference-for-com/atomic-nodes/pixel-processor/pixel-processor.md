---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ''
description: ピクセルプロセッサノードを使用すると、高度なテクスチャ操作を行うカスタム式を使用して個々のピクセルを処理できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ピクセルプロセッサー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 1%

---


# ピクセルプロセッサー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomicノード：ピクセルプロセッサ](../../../../assets/comp_pixelprocessor_1.png "Atomicノード：ピクセルプロセッサ"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

指定した[Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)の結果を各ピクセルの値とするイメージを生成します。

ピクセルプロセッサーを使用すると、オプションの入力で、出力として返される各ピクセルに対してカスタム関数を実行できます。

このノードは、数学的な操作を実行してグラフ内の結果を返すことができるため、これまでで最も汎用性の高いノードです。

</td>
</tr>
</table>

[FX-Map](../../../../function-graphs/fxmaps/fxmaps.md)と同様に、何かを実行するには内部機能を設定する必要があります。 ピクセルプロセッサーがFX-Mapと異なる点は、パターンの配置に焦点を合わせず、パターンの形状と配置を制御する複数の機能を備えていることです。 代わりに、各ピクセルに対して並列に1つの関数が実行され、各ピクセルは隣接するピクセルの計算結果を認識しません。

ピクセルプロセッサは、[値プロセッサ](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)に似ています。このプロセッサは1つの値でのみ動作し、ピクセルプロセッサと比較して適切な最適化を提供できます。

ノードベースのエディターで[シェーダ](../../../../glossary/glossary.md)関数を作成するために使用するユーザーは、ピクセルプロセッサーを使用すると、使い慣れた環境を実現できます。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> ピクセルプロセッサノードの簡単な使用方法を示す注釈付きのプロジェクトファイルは、このドキュメントの[Substanceグラフのサンプル](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)セクションにあります。
> 
> [Value processor](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)ノードは、[Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)について理解するための開始点として適しています。
> 
> また、このタイプのグラフを使用して数学的な演算を実行することは、このノードから何かを得るために必須です。
> 
> また、[UV](../../../../glossary/glossary.md)、[テクスチャサンプリング](../../../../glossary/glossary.md)、およびベクターの概念を理解しておくことをお勧めします。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | グレースケールとカラー出力画像を切り替えます。 |
| <b>ピクセル関数あたり</b> *フロート/フロート4* | [Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)が出力画像のピクセルごとに評価されました。   現在のピクセルの[正規化](../../../../glossary/glossary.md)位置にアクセスするには、<b>$pos</b>変数に設定された[Get Float2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)ノードを使用します。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力画像#</b> *グレースケール/カラー* | [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)または[Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)ノードを使用して、指定されたインデックスの入力の値にアクセスします。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
