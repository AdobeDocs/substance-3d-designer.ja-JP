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
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '126'
ht-degree: 3%

---


# Heightノーマルブレンダー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/height-normal-blender.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

グレースケールの高さマップをノーマルマップにブレンドするショートカットノード。 Height入力は内部でノーマルマップに変換され、ノーマル入力と正しく合成されます。

これは、個別のノードを使用して手動でディテールをブレンドするよりも迅速にディテールをブレンドする方法ですが、特定のニーズに対するコントロールと調整が欠けている場合があります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Height</b> <i>グレースケール入力</i> | ブレンドするグレースケールの高さ。 |
| <b>標準</b> <i>カラー入力</i> | ブレンドするベース法線マップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>法線の強度</b> <i>0.0 - 16.0</i> | Height入力の標準変換の強さ。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
