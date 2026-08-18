---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/linear-burn.html"
breadcrumb-title: ''
description: 焼き込み（リニア）ノードを使用すると、焼き込み（リニア）モードを使用してテクスチャをブレンドし、減光効果やコントラスト効果を作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Linear Burn
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 焼き込み (リニア)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
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

焼き込み（リニア）ブレンドを実行します。 数式は、前景+背景 – 1です。

## パラメーター

### 入力

* **前景**: *カラー入力*
* **背景**: *カラー入力*
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
