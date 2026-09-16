---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ""
description: サーフェスの詳細と照明をコントロールするためのテクスチャを処理および操作するには、[法線]ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線
user-guide-description: ""
user-guide-title: ""
source-git-commit: a22681c0410386966a80a0170c62fae57da6ef74
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 7%
---

# 法線

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top">

![アトミックノード：標準](normal.resources/comp_normal_1.png "アトミックノード：標準"){width="100%"}

<b>イン：</b> アトミックノード

</td>
<td style="border: 0;" valign="top">

高さマップとして解釈されたグレースケール画像から法線マップを計算します。

入力グレースケールマップを正接空間法線マップ出力に変換する。 これには、強度とエンコードを設定するためのユーザーオプションがいくつか用意されています。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%"></td>
<td style="border: 0; text-align: center"><img src="normal.resources/normal-tooltip.gif" alt="標準ツールチップ" /></td>
<td style="border: 0; width: 15%"></td>
</tr>
</table>

これは、リアルタイム対応マテリアル用に高さマップ入力を法線マップに変換するために頻繁に使用される非常に便利なノードです。 [通常のソベル](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md)および通常のワールドユニットへのHeightに見つかる代替案があります。



## パラメーター

|  |  |
| --- | --- |
| <b>適用度</b> *浮動小数* | 高さマップの強さを変更します。   法線に変換するために入力高さマップをどの程度変換するかを設定します。 入力マップによっては、100を超える値を指定した場合の効果はほとんどありません。 |
| <b>標準の形式</b> *ブーリアン* | 高さマップのY座標を反転します(OpenGL)。   グリーン(Y)チャンネルのエンコード方法を設定します。 基本的には、「緑色/Y方向に反転」スイッチです。 |
| <b>アルファチャンネルコンテンツ</b> *ブーリアン* | 法線マップのアルファチャンネルを入力テクスチャで塗りつぶします。   入力/力Alphaで塗りつぶしAlphaを1に設定：これにより、入力を追加Alphaとして使用する代わりに、アルファチャンネルを実線に設定できます。 |

## 入力コネクター

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール*&#x200B;プライマリ | 入力画像がHeightマップとして解釈されます。 |


## 例

*近日公開。*
