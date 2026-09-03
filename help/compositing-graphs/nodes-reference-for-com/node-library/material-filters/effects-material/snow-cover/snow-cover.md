---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
breadcrumb-title: ''
description: Snowカバーノードを使用して、サーフェスの角度と位置に基づいてマテリアルに雪の積み重ね効果を加えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Snow Cover
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Snowカバー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 8%

---


# Snowカバー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](snow-cover.resources/snow-cover-01.png){width="128px"}

<b>内：</b> マテリアルフィルター >エフェクト

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

オールインワン効果で、マテリアル全体に雪が積もります。 フォトスキャンなどの高画質のHeightmapを使用することを強く想定しています。 結果はPBRで正しいことを意図しています。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>新しいSnow</b> <i>0.0 - 1.0</i> | 起立した領域の雪の量を設定します。 結果は溶融Snowパラメータに関連付けられます。 |
| <b>溶けたSnow</b> <i>0.0 - 1.0</i> | 下げたコーナーの雪解け量を設定します。 |
| <b>ビルドアップ</b> <i>0.0 - 1.0</i> | 主にHeight出力に影響し、Heightの重ね合わせ効果を決定します。 |
| <b>Smoothness</b> <i>0.0 - 1.0</i> | 積雪によるHeightのディテールを滑らかにします。 |
| <b>フレークの適用度</b> <i>0.0 - 1.0</i> | 主にノーマルマップ、フレークのディテールの強度に影響します。 |
