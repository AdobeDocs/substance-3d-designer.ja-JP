---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/directional-blur.html"
breadcrumb-title: ''
description: ブラー（方向）ノードを使用して、モーションブラーおよび筋エフェクトを作成する特定の方向にブラー効果を適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Directional blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 指向性ブラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 9%

---


# 指向性ブラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：方向ブラー](../../../../assets/comp_dirmotionblur_1.png "原子ノード：方向ブラー"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

強度マップに従って、指定した方向にぼかしを適用します。

このノードは、入力に対してモーションブラーと同様の操作を実行します。 すべての方向に均等にぼかす通常の&#39;[ブラー](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blur/blur.md)&#39;ノードとは異なり、&#39;方向ぼかし&#39;はユーザー定義の角度に沿って機能します。

</td>
</tr>
</table>

「ぼかし」と同様に、より高速で低品質な操作です。 拡張された高品質の代替エフェクトが[異方性反射ブラー](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)で提供されます。性能のトレードオフがあります

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

## ブラー（方向）とブラー（異方性）

次の画像は、同じ入力シェイプに対して有効な方向ぼかしと[異方性ぼかし](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/anisotropic-blur/anisotropic-blur.md)を、同様のパラメーターで示しています。 異方性反射ブラーがフル異方性で高品質に設定されています。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>ブラー（方向）</b>

![方向のぼかしの比較](../../../../assets/dirblur-01.png "方向ぼかしの比較"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

<b>異方性反射ぼかし</b>

![異方性ぼかしの比較](../../../../assets/aniso-01.png "異方性ぼかしの比較"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### パラメーター

</td>
<td style="border: 0;" valign="top">

### 入力コネクタ

</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>適用度</b> *フロート* | ぼかしの半径をピクセル単位で設定します。 |
| <b>角度</b> *フロート* | 水平から開始し、時計回りに数ターン単位でぼかし効果の方向を指定します。つまり、方向ベクトル(1, 0)です。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー* [プライマリ](../../../../glossary/glossary.md) | 処理する画像。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
