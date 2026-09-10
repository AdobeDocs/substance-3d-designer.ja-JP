---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height-hq.html"
breadcrumb-title: ''
description: '[法線からHeightへ] HQノードを使用して、サーフェスの詳細を抽出するために法線マップを高品質の高さマップに変換します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal To Height HQ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HeightHQに標準
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 3%

---


# HeightHQに標準

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-to-height-hq.resources/normal-to-height-hq.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

正接空間のノーマルマップを再びハイトマップに変換しようとする逆変換ノード。 これは、より高度なノードです。[Heightに対して標準](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height/normal-to-height.md)では、選択肢が少なく、異なる計算を使用します。

ノーマルマップソースしかなくても、ハイトマップと組み合わせて操作を実行したい場合に便利です。 Heightを通常に変換すると情報が失われるため、100%正しい結果を得ることはできないことに注意してください。 正しく生成されたHeightmapを置き換えることはできません。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>リリーフ残高</b> <i>0.0 - 1.0</i> | 低周波バイアスと高周波バイアスの間のブレンド。 |
| <b>Heightの適用度</b> <i>0.0 - 1.0</i> | 高さマップの強度または乗数は、グローバル不透明度に少し似ています。 |
| <b>Heightの正規化</b> <i>False/True</i> | [自動レベル補正](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)のように、ハイトマップの範囲を自動的に拡大・縮小して完全なコントラストを使用します。 |
| <b>クォリティ</b> <i>標準、高</i> | 速度と画質を切り替えます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-to-height-hq.resources/normal2height-hq-ex.png" />
        </td>
    </tr>
</table>
