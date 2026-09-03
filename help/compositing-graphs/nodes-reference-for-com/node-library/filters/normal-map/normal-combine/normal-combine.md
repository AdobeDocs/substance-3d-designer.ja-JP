---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-combine.html"
breadcrumb-title: ''
description: '[法線の結合]ノードを使用して、サーフェスの詳細と詳細をレイヤ化するための複数の法線マップを結合します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Combine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通常の結合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# 通常の結合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-combine.resources/normal-combine-01.png){width="128px"}

<b>イン：</b>フィルター>標準マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[法線を結合] 2つの法線マップの詳細を数学的に正しい方法で結合します。

これは、他の2D画像編集ソフトウェアでよく知られている「オーバーレイ」方法と似ていますが、内部的には少し異なる動作をします（3つのオプション）。

</td>
</tr>
</table>

これは、2Dで生成された法線マップの詳細をベイク済みマップに加える最も適切な方法です。

2つの法線マップのディテールを結合せずに（マスクを使用するなどして） 2つの法線マップをブレンドするには、[法線のブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-blend/normal-blend.md)を使用する必要があります。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>標準2</b> <i>色</i> | 説明 |
| <b>標準1</b> <i>色</i> | 説明 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>テクニック</b> *整数* | 使用する内部ブレンド手法を設定し、品質を優先した速度で取引します。<br><br>*– ホワイトアウト（低品質）<br>*&#x200B;チャンネルミキサー（高品質）<br>*詳細を重視（高品質）* |

## 例
