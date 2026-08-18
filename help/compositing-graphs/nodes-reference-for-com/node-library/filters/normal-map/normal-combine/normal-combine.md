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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 2%

---


# 通常の結合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-combine.png){width="128px"}

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

## 入力コネクタ

<b>通常2</b> *色*&#x200B;説明

<b>通常1</b> *色*&#x200B;説明

## パラメーター

<b>手法</b> *整数*&#x200B;使用する内部合成手法を設定します。品質を優先した速度で取引します。\
* – ホワイトアウト（低画質）
* チャンネルミキサー（高品質）
* ディテール指向（高品質）*

## 例
