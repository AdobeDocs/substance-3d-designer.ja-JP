---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/snow-cover.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%

---


# Snowカバー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/snow-cover.png){width="128px"}

## Snowカバー

**内：** *マテリアルフィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

オールインワン効果で、マテリアル全体に雪が積もります。 フォトスキャンなどの高画質のHeightmapを使用することを強く想定しています。 結果はPBRで正しいことを意図しています。

## パラメーター

### 入力

* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **チャネル**\
  この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。
* **新しいSnow**: *0.0 ～ 1.0*&#x200B;起伏のある領域の積雪量を設定します。 結果は溶融Snowパラメータに関連付けられます。
* **溶けたSnow**: *0.0 ～ 1.0*&#x200B;下がったコーナーで溶けた雪の量を設定します。
* **ビルドアップ**: *0.0 ～ 1.0* Height出力に主に影響を与え、Heightの重ね合わせ効果を決定します。
* **Smoothness**: *0.0 ～ 1.0*&#x200B;積雪によるHeightの細部の滑らかさを設定します。
* **フレークの適用度**: *0.0 ～ 1.0*&#x200B;主にノーマルマップ、フレークのディテールの適用度に影響します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
