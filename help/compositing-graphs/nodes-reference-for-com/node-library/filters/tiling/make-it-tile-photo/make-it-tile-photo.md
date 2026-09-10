---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-photo.html"
breadcrumb-title: ''
description: 「写真をタイル状にする」ノードを使用すると、素材を作成するために写真をシームレスなタイリングテクスチャに変換できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Photo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Make It Tile Photo
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 9%

---


# Make It Tile Photo

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-photo.resources/make-it-tile-photo.png)

![](make-it-tile-photo.resources/make-it-tile-photo-grayscale.png)

<b>イン：</b>フィルター> タイリング

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、エッジが連続していないためにタイリングできない可能性のあるイメージに対して、エッジ修正機能を提供します。 これは、入力画像のエッジ以外には影響しません。 尺度を調整したり、タイルを異なる方法で並べたりする場合は、[タイルパッチを作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-patch/make-it-tile-patch.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>マスクのワープH</b> <i>-100.0 - 100.0</i> | 未定義のトランジションを避けるために、水平軸にワープを導入します。 |
| <b>マスクワープV</b> <i>-100.0 - 100.0</i> | 未定義のトランジションを避けるために、垂直方向の軸にワープを導入します。 |
| <b>マスクサイズH</b> <i>0.0 - 1.0</i> | トランジションのエッジが水平方向に到達する距離を設定します。 |
| <b>マスクサイズV</b> <i>0.0 - 1.0</i> | トランジションの端が垂直方向に達する距離を設定します。 |
| <b>マスク精度H</b> <i>0.0 - 1.0</i> | 水平方向の変化の滑らかさを設定します。 |
| <b>マスク精度V</b> <i>0.0 - 1.0</i> | 垂直方向の変化の滑らかさを設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-photo.resources/mit-photo-ex.png" />
        </td>
    </tr>
</table>
