---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/height-normal-blender.html"
breadcrumb-title: ''
description: Height法線ブレンダーノードを使用して、サーフェスのディテール情報を組み合わせるHeightと法線マップをブレンドします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Height Normal Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Heightノーマルブレンダー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# Heightノーマルブレンダー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

## Heightノーマルブレンダー

**場所：** *フィルター/法線マップ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

グレースケールの高さマップをノーマルマップにブレンドするショートカットノード。 Height入力は内部でノーマルマップに変換され、ノーマル入力と正しく合成されます。

これは、個別のノードを使用して手動でディテールをブレンドするよりも迅速にディテールをブレンドする方法ですが、特定のニーズに対するコントロールと調整が欠けている場合があります。

## パラメーター

### 入力

* **Height**: *グレースケール入力*\
  ブレンドするグレースケールの高さ。
* **標準**: *カラー入力*\
  ブレンドするベース法線マップ。

### パラメーター

* **法線の強さ**: *0.0 ～ 16.0* Height入力の法線の強さ。
* **標準の形式**: *DirectX、OpenGL*\
  異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
