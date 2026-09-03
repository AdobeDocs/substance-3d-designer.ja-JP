---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: 焼き込みカラーのブレンドノードを使用すると、シャドウと焼き込み効果を作成するためのコントラストが強くなり、テクスチャが暗くなります。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焼き込みカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 9%

---


# 焼き込みカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-burn.resources/color-burn-01.png){width="128px"}

<b>イン:</b>フィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

前景と背景の間で焼き込みカラーのブレンドを実行します。 数式の形式は1 - (1-Background) / Foregroundです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>前景</b> <i>カラー入力</i> |  |
| <b>背景</b> <i>カラー入力</i> |  |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景の間のブレンド不透明度。 |
| <b>アルファブレンディング</b> <i>False/True</i> | 前景および背景のアルファチャンネルのブレンドを切り替えます。 Falseに設定した場合、フォアグラウンドのアルファチャンネルは無視されます。 |
