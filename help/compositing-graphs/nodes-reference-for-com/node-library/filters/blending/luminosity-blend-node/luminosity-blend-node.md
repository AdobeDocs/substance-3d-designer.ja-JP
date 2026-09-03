---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/luminosity-blend-node.html"
breadcrumb-title: ''
description: 輝度の描画ノードを使用すると、輝度の値に基づいてテクスチャを描画し、明るさをベースにした合成効果を作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Luminosity (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 輝度（ブレンドノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6507710c6005db383ba88ce9e5c6ad9c34d87c9f
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# 輝度（ブレンドノード）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<b>イン:</b>フィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

前景の輝度を取り入れながら、背景の色相とクロミナンスを維持する輝度の描画モードを実行します。

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
