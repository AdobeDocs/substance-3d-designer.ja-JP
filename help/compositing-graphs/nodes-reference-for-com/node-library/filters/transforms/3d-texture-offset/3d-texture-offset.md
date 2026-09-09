---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/3d-texture-offset.html"
breadcrumb-title: ''
description: パララックスエフェクトやサーフェスのバリエーションを作成するために3D空間でテクスチャをオフセットするには、「3D テクスチャオフセット」ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > 3D Texture Offset
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D テクスチャオフセット
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 3%

---


# 3D テクスチャオフセット

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3dtextureoffsetgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](3d-texture-offset.resources/3dtextureoffsetcolor.png){width="200px"}

</td>
</tr>
</table>

<b>イン：</b>フィルター/変換

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**3D テクスチャオフセット**&#x200B;ノードは、**入力**&#x200B;に接続されている&#x200B;*3D テクスチャ*&#x200B;によって記述されているオブジェクトに、**X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸の&#x200B;*オフセット変換*&#x200B;を適用します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール/カラー</i> | 3Dオブジェクトを表す<i>3D テクスチャ</i>。<br>オブジェクトは通常、<i>単位キューブ</i>で記述されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>オフセット</b> <i>浮動小数3</i> | <b>入力</b>に接続された<i>3D テクスチャ</i>によって記述されたオブジェクトに適用された<i>ワールド空間</i>のオフセットの量。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3dtextureoffset-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-offset.resources/3dtextureoffset-node.png" />
        </td>
    </tr>
</table>
