---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/pixel-processor.html"
breadcrumb-title: ""
description: ピクセルプロセッサーノードを使用すると、高度なテクスチャ処理用のカスタム式を使用して個々のピクセルを処理できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Pixel processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ピクセルプロセッサー
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 1%
---

# ピクセルプロセッサー

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![アトミックノード: ピクセルプロセッサー](pixel-processor.resources/comp_pixelprocessor_1.png "アトミックノード: ピクセルプロセッサー")

</td>
<td style="border: 0;" valign="top">

指定した[Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)の結果を各ピクセルの値とするイメージを生成します。

このピクセルプロセッサーを使用すると、オプションの入力で、出力として返される各ピクセルに対してカスタム関数を実行できます。

このノードは、数学演算を実行してグラフ内の結果を返すことができるため、これまでで最も汎用性の高いノードです。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="pixel-processor.resources/pixel-processor-tooltip.gif" alt="ピクセルプロセッサツールチップ" /></div>

[FX-Map](../../../../function-graphs/fxmaps/fxmaps.md)と同様に、操作を実行するには内部機能を設定する必要があります。 ピクセルプロセッサーがFX-Mapと異なる点は、パターンの配置には重点を置かず、パターンの形状と配置を制御する複数の機能がある点です。 代わりに、各ピクセルに対して並列に1つの関数が実行され、各ピクセルは隣接するピクセルの計算結果を認識しません。

このピクセルプロセッサーは、[バリュープロセッサー](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)に似ています。これは1つの値でのみ実行され、ピクセルプロセッサーと比較して適切な最適化を行うことができます。

ノードベースのエディターで[シェーダー](../../../../glossary/glossary.md)関数を作成する場合は、ピクセルプロセッサーを使用すると使い慣れた環境を実現できます。


>[!TIP]
>
> ピクセルプロセッサーノードの簡単な使用方法を示す注釈付きのプロジェクトファイルは、このドキュメントの[サンプルSubstance グラフ](../../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)のセクションにあります。
> 
> [バリュープロセッサー](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)ノードは、[Substance関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)について理解するための良い出発点となります。
> 
> また、この種のノードを使用して数学的な演算を実行することは、このグラフから何かを得るために必須です。
> 
> また、[UV](../../../../glossary/glossary.md)、[テクスチャサンプリング](../../../../glossary/glossary.md)、およびベクターの概念を理解しておくことをお勧めします。


## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブーリアン* | グレースケールとカラー出力画像を切り替えます。 |
| <b>ピクセル関数あたり</b> *浮動小数/浮動小数4* | [Substance関数のグラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)が出力イメージのピクセルごとに評価されました。   現在のピクセルの[正規化](../../../../glossary/glossary.md)位置にアクセスするには、<b>$pos</b>変数に設定された[Get 浮動小数 2](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)ノードを使用します。 |

## 入力コネクター

|  |  |
| --- | --- |
| <b>入力画像 #</b> *グレースケール/カラー* | [Sample color](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)または[Sample grayscale](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)ノードを使用して、指定されたインデックスの入力の値にアクセスします。 |


## 例

*近日公開。*
