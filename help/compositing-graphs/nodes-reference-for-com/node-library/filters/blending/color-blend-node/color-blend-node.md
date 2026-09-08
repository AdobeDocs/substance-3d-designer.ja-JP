---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/color-blend-node.html"
breadcrumb-title: ''
description: 「カラー」描画ノードを使用すると、色相や彩度を変更しても輝度が維持されるように、カラーモードを使用してテクスチャを描画できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Color (Blend Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラー（ブレンドノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '108'
ht-degree: 4%

---


# カラー（ブレンドノード）

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/difference.png){width="128px"}

## カラー

**イン：** *フィルター/描画*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

前景の色相とクロミナンスを適用しながら、背景の輝度を維持するカラー描画モードを実行します。

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
