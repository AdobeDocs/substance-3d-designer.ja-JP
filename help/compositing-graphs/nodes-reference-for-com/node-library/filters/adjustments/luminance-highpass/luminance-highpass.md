---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/luminance-highpass.html"
breadcrumb-title: ''
description: 輝度ハイパスノードを使用して、テクスチャから高周波数の輝度ディテールを抽出し、表面のディテールを強調します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Luminance Highpass
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 輝度ハイパス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '105'
ht-degree: 6%

---


# 輝度ハイパス

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/luminance-highpass.png){width="128px"}

## 輝度ハイパス

**イン：** *フィルター/調整*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

入力の輝度値に[ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)を実行して、照明情報をキャンセルします。 撮影したテクスチャを照明情報で修正する場合に便利です。 [Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)で複数のパスを組み合わせて、様々な周波数の光のディテールを取り除くことができます。

[低周波数の照明をキャンセル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/lighting-cancel-low-fre/lighting-cancel-low-frequencies.md)よりも、色の保持に関して少し優れています。

## パラメーター

* **半径**: *0.0 ～ 64.0*&#x200B;ハイパス効果の半径。 半径を小さくすると、小さな照明がキャンセルされ、入力画像に合わせて調整されます。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/luminance-highpass-example.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
