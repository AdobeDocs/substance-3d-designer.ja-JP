---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: 差描画ノードを使用すると、差描画モードを使用して反転およびコントラスト効果を作成し、テクスチャを描画できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 差
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '99'
ht-degree: 7%

---


# 差

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](difference.resources/difference-01.png){width="128px"}

<b>イン:</b>フィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

前景と背景の入力の間に差描画モードを生成します。 前景から背景を減算し、絶対値を返します（負の値は返しません）。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>背景</b> <i>カラー入力</i> |  |
| <b>前景</b> <i>カラー入力</i> |  |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景の間のブレンド不透明度。 |
| <b>アルファブレンディング</b> <i>False/True</i> | 前景および背景のアルファチャンネルのブレンドを切り替えます。 Falseに設定した場合、フォアグラウンドのアルファチャンネルは無視されます。 |
