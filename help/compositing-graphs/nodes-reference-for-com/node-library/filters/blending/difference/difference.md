---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/difference.html"
breadcrumb-title: ''
description: 差分ブレンドノードを使用すると、反転およびコントラスト効果を作成するための差分モードを使用してテクスチャをブレンドできます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Difference
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 差
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# 差

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

## 差

**イン：** *フィルター/描画*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

前景と背景の入力の間に差描画モードを生成します。 前景から背景を減算し、絶対値を返します（負の値は返しません）。

## パラメーター

### 入力

* **背景**: *カラー入力*
* **前景**: *カラー入力*
* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **不透明度**: *0.0 ～ 1.0*\
  前景と背景の間のブレンド不透明度。
* **Alphaのブレンド**: *False/True*\
  前景および背景のアルファチャンネルのブレンドを切り替えます。 Falseに設定した場合、フォアグラウンドのアルファチャンネルは無視されます。

## サンプル画像

</td>
</tr>
</table>
