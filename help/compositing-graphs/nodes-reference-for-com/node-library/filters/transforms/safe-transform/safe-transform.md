---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: '[セーフトランスフォーム]ノードを使用すると、テクスチャの境界を維持し、アーティファクトを回避しながら変換を適用できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: セーフ変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 5%

---


# セーフ変換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](safe-transform.resources/safe-transform-01.png)

![](safe-transform.resources/safe-transform-02.png)

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

タイリングセーフバージョンの[Transform 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)。 タイリングを壊すことなく、またオフセットと回転が小さいためにピクセルのディテールを失うことなく（鮮明さやシャープネスの損失）、拡大・縮小、回転、オフセットすることができます。

最大限のコントロールや完全なシャープが必要な場合に、ノイズを変形するのに便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>タイル</b> <i>1 - 16</i> | タイリング単位で入力を縮小します。 |
| <b>オフセットモード</b> <i>手動、ランダム</i> | 手動で定義したオフセットではなく、ランダムなオフセットに切り替えます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 結果を移動または変換します。 ピクセルがスナップされ、補間されていないことを確認します。 |
| <b>回転</b> <i>0.0 - 1.0</i> | 角度に沿って入力を回転します。 |
| <b>タイルセーフ回転</b> <i>False/True</i> | ピクセルをぼかさない安全な値に回転をスナップするかどうかを指定します。 |
| <b>対称</b> <i>なし、X、Y、X+Y</i> |  |
| <b>背景色</b> <i>（カラー値） （カラーバージョンのみ）</i> |  |
| <b>ミップマップモード</b> <i>自動、手動</i> | マッピングモードを決定します。 これを「手動」に設定すると、よりシャープな結果になります。 |
| <b>ミップマップレベル</b> <i>0 - 10</i> | ミップマップモードが「手動」に設定されている場合、別のミップマップを選択できます。 |
