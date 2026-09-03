---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-sobel.html"
breadcrumb-title: ''
description: サーフェスの詳細のソベルエッジ検出を使用して高さマップから法線マップを作成するには、[標準ソベル]ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Sobel
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 標準のソベル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 5%

---


# 標準のソベル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-sobel.resources/normal-sobel-01.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ハイトマップ入力をノーマルマップ出力に変換します。 [標準ノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)の少し高度なアトミックノードです。このノードでは、標準のサンプリング方式ではなくSobelサンプリングを使用します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 3.0</i> | 変換された法線の強さ。 |
| <b>標準の形式</b> <i>OpenGL, DirectX</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
