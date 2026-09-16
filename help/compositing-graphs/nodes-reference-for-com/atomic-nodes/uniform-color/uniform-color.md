---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ""
description: '[色を統一]ノードを使用して、単色の塗り潰しとベースレイヤを作成するための均一な色のテクスチャを生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 均一カラー
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 7%
---

# 均一カラー

<table>
<tr style="border: 0;">
<td style="border: 0; width: 30%; vertical-align: top">

![原子ノード：均一な色](uniform-color.resources/comp_uniform_1.png "原子ノード：均一な色")

</td>
<td style="border: 0; vertical-align: top">

フラットなグレースケールまたはカラー値を生成します。

これは、カラーを追加したり、特定の値を作成したりするための出発点として頻繁に使用される単純なノードです。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="uniform-color.resources/uniform-color-tooltip.gif" alt="均一カラーツールヒント" /></div>


>[!TIP]
>
> パフォーマンスの最適化
> 
> どちらの調整も、ノードの計算時間とメモリのフットプリントを削減します。
> 
> * グレースケール値が必要な場合は、ノードの[カラーモード](#parameters)を&#39;グレースケール&#39;に切り替えてください。
> * ノードの出力は単色なので、できるだけ低い解像度を使用します。 ノードの&#39;[出力サイズ](../../../../compositing-graphs/output-size/output-size.md)&#39;パラメーターを&#39;絶対&#39; [継承メソッド](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)、解像度16 x 16ピクセルを使用するように設定します。


## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | グレースケールとカラー出力画像を切り替えます。 |
| <b>出力色</b> *フロート/フロート4* | 出力画像に使用する単色を選択します。   「カラー」カラーモードを使用する場合、Alphaチャンネルは不透明度に使用されます。0は完全に透明で、1は完全に不透明です。 |


## 例

*近日公開。*
