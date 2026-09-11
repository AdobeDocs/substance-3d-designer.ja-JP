---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-simplex-noise.html"
breadcrumb-title: ''
description: 「3Dシンプレックス」ノイズノードを使用して、滑らかで自然なボリュームノイズを作成するための3Dシンプレックステクスチャパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Simplex Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dシンプレックスノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8be4dabbdf7bd618ca2ee21c64655952474b9df2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 5%

---


# 3Dシンプレックスノイズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-simplex-noise.resources/3d-simplex-noise.png){width="128px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイクされたPosition Mapが入力スロットに接続されると、プロシージャルノイズが発生します。 これは、GPU エンジンでのみ使用します。\
[3Dパーリンノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)と似ていますが、パフォーマンスと速度が重要な場合は、より速く、簡単になります。

このノイズは、実際のベイク済みマップではなく、[Cube 3D GBuffers](https://support.allegorithmic.com/documentation/display/SDDOC/Cube+3D+GBuffers)を入力としてテストできます（下図の例を参照）。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スケール</b> <i>0.0 - 64.0</i> | エフェクトのグローバルスケールを設定します。 |
| <b>サイズ</b> <i>0.0 - 2.0</i> | X、Y、Z軸に対して個別に不均等スケーリングを実行します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-simplex-noise.resources/3d-simplex.gif" />
        </td>
    </tr>
</table>
