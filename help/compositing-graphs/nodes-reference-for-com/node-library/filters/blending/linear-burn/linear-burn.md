---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: 焼き込みノードを使用して、焼き込みリニアモードでテクスチャをブレンドし、減光効果とコントラスト効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焼き込み (リニア)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '96'
ht-degree: 10%

---


# 焼き込み (リニア)

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/linear-burn.png){width="128px"}

## 焼き込み (リニア)

**イン：** *フィルター/描画*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

焼き込みブレンドを実行します。 数式は、前景+背景 – 1です。

## パラメーター

### 入力

* **前景**: *カラー入力*
* **背景**: *カラー入力*
* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **不透明度**: *0.0 ～ 1.0*\
  前景と背景の間のブレンド不透明度。
* **アルファブレンディング**: *False/True*\
  描画領域と背景アルファチャンネルのブレンドを切り替えます。 Falseに設定した場合、前景のアルファチャンネルは無視されます。

## サンプル画像

</td>
</tr>
</table>
