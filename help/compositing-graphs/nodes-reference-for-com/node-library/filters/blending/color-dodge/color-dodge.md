---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-dodge.html"
breadcrumb-title: ''
description: 覆い焼きカラーのブレンドノードを使用して、ハイライトと光彩のエフェクトを作成するためのコントラストを下げ、テクスチャを明るくします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Dodge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 覆い焼きカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 9%

---


# 覆い焼きカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-dodge.resources/color-dodge.png){width="128px"}

<b>イン:</b>フィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

覆い焼きカラーブレンドを実行します。 数式はBackground / (1-Foreground)です。

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
