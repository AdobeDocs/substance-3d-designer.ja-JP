---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-warp.html"
breadcrumb-title: ''
description: 方向ワープノードを使用して、テクスチャに方向ゆがみを適用し、フローエフェクトやモーションエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 指向性ワープ
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 9%

---


# 指向性ワープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：方向ワープ](../../../../assets/comp_directionalwarp_1.png "原子ノード：方向ワープ"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

強度マップに従ってピクセルを指定した方向に移動します。これにより、変形が発生する場合があります。

ユーザが設定した方向に入力をワープし、ユーザが設定した強度マップを掛けます。 これはワープと似ていますが、特定の方向に対してのみ機能します。

</td>
</tr>
</table>

ワープノードは、非常に単純ですが便利なノードで、他のより高度なエフェクトの良い基盤として機能します。 その他の関連するノードとして、[勾配ぼかし](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/slope-blur/slope-blur.md)および[ベクトルワープ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)など、より高度な代替手段があります。

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
| <b>適用度</b> *フロート* | ワープの強さを設定します。 |
| <b>ワープ角度</b> *フロート* | ワープ効果の角度をターン数で設定します。 |
| <b>入力フィルターモード</b> *ブール値* | <b>入力</b>のサンプリングに最も近いフィルターとバイリニアフィルターのどちらを使用するかを制御します。 |
| <b>強度マップのオフセット</b> *フロート* | この値は、<b>強度入力</b>画像の値から差し引かれます。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー*&#x200B;プライマリ | ワープ効果を適用するグレースケールまたはカラー入力画像。 |
| <b>強度入力</b> *グレースケール* | <b>入力</b>画像に適用する必要のあるワープの量を定義するグレースケール画像です。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![方向ワープ – 例1](../../../../assets/dir-warp.gif "方向ワープ – 例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向ワープ – 例2](../../../../assets/dir-warp02.gif "方向ワープ – 例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![方向ワープ – 例3](../../../../assets/dir-warp03.gif "方向ワープ – 例3"){zoomable="yes"}

</td>
</tr>
</table>
