---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/hsl.html"
breadcrumb-title: ""
description: HSLノードを使用して、色相、彩度、色明度のテクスチャを調整し、カラーを操作および補正します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > HSL
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HSL
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0cb0df528e7f0eb6f3c2d51e35302744952718d5
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 9%
---

# HSL

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![アトミックノード: HSL](hsl.resources/comp_hsl_1.png "アトミックノード: HSL")

</td>
<td style="border: 0;" valign="top">

カラー画像の色相、彩度、明度を調整します。

これは基本的で使いやすいノードで、カラーデータを操作する場合に非常に便利です。

画像のトーンを他の方法で編集する場合は、[曲線](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)、[レベル](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)および[コントラスト/輝度](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)を確認してください。

</td>
</tr>
</table>

<div data-preserve-html="true" style="text-align: center;"><img src="hsl.resources/hsl-tooltip.gif" alt="hslツールチップ" /></div>



## パラメーター

|  |  |
| --- | --- |
| <b>色相</b> *浮動小数* | 入力画像のカラーを指定します。   0.5より小さい値を指定すると色相が負にシフトし、0.5より大きい値を指定するとプラスにシフトします。 |
| <b>彩度</b> *浮動小数* | 入力画像のカラーの彩度を指定します。   0.5より小さい値を指定すると彩度が下がり、0.5より大きい値を指定すると彩度が上がります。 |
| <b>明度</b> *浮動小数* | 入力画像の明度を指定します。0.5より小さい値にすると明度が下がり、0.5より大きい値にすると上がります。 |

## 入力コネクター

|  |  |
| --- | --- |
| <b>入力</b> *色*&#x200B;プライマリ | 処理する画像。 |


## 例

*近日公開。*
