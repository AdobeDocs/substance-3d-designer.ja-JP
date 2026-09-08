---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-burn.html"
breadcrumb-title: ''
description: 焼き込みカラーのブレンドノードを使用すると、シャドウと焼き込み効果を作成する際のコントラストが強くなり、テクスチャが暗くなります。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焼き込みカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 9%

---


# 焼き込みカラー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-burn.png){width="128px"}

## 焼き込みカラー

**イン：** *フィルター/描画*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

前景と背景の間で焼き込みカラーのブレンドを実行します。 数式の形式は1 - (1-Background) / Foregroundです。

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
