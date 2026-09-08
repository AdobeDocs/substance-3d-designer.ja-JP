---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/hald-clut.html"
breadcrumb-title: ''
description: 「Hald CLUT」ノードを使用すると、カラーグレーディングと補正にHald CLUT形式を使用してカラールックアップテーブルを適用できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Hald CLUT
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ハルト・クラット
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '91'
ht-degree: 4%

---


# ハルト・クラット

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hald-clut.png){width="128px"}

## ハルト・クラット

**イン：** *フィルター/調整*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

入力画像にLUTを適用します。 LUTは4096\*4096の解像度でHald形式である必要があります。 詳細については、<http://www.quelsolaar.com/technology/clut.html>を参照してください。

### 入力

* **入力**: *カラー入力*\
  LUTを適用する画像。
* **lut**: *色入力* Lut入力スロット。 4096 x 4096でなければなりません。

## パラメーター

* **Alpha別のLUT強度**: *False/True* LUT効果をアルファチャンネルで重み付けするかどうかを定義します。

例

![](../../../../../../assets/content-hald-clut.jpg)

</td>
</tr>
</table>
