---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/normal.html"
breadcrumb-title: ''
description: 法線ノードを使用して、法線マップテクスチャを処理および操作し、サーフェスのディテールとライティングを制御します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '222'
ht-degree: 8%

---


# 法線

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：標準](../../../../assets/comp_normal_1.png "原子ノード：標準"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

高さマップとして解釈されたグレースケール画像から法線マップを計算します。

このノードは、入力グレースケールマップを接線空間ノーマルマップ出力に変換します。 これには、強度とエンコードを設定するためのユーザーオプションがいくつか用意されています。

</td>
</tr>
</table>

これは、リアルタイム対応のマテリアル用にHeightマップの入力を法線マップに変換するために頻繁に使用される非常に便利なノードです。 [通常のソベル](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-sobel/normal-sobel.md)および通常のワールドユニットへのHeightに見つかる代替案があります。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>適用度</b> *フロート* | Heightマップの強さを変更します。   法線に変換するために入力Heightマップを変換する度合いを設定します。 入力マップによっては、100を超える値の効果はほとんどありません。 |
| <b>標準の形式</b> *ブール値* | Heightマップ(OpenGL)のY座標を反転します。   グリーン(Y)チャンネルのエンコード方法を設定します。 基本的には、「緑色/Y方向に反転」スイッチです。 |
| <b>Alphaチャンネルコンテンツ</b> *ブール値* | 法線マップのアルファチャンネルを入力テクスチャで塗りつぶします。   Fill Alphaの入力/フォースAlphaを1に設定する：このオプションを選択すると、入力を追加Alphaとして使用する代わりに、Alphaチャンネルを実線に設定することができます。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール*&#x200B;プライマリ | 入力画像がHeightマップとして解釈されます。 |

## 出力コネクター

|  |  |
| --- | --- |
| <b>出力</b> *色* |  |

## 例

*近日公開。*
