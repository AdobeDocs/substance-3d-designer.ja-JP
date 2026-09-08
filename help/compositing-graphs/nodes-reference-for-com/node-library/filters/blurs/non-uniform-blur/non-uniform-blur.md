---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/non-uniform-blur.html"
breadcrumb-title: ''
description: 不均等ブラーノードを使用して、異方性効果のX方向とY方向に異なる強度のブラーを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Non Uniform Blur
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ブラー（不均等）
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 9%

---


# ブラー（不均等）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/non-uniform-blur-grayscale.png){width="128px"}

![](../../../../../../assets/non-uniform-blur.png){width="128px"}

<b>イン:</b>フィルター/ぼかし

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高品質のぼかしを実行します。強度は入力マスクによって決まります。 オプションを使用すると、異方性および非対称性を追加できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>ぼかしマップ</b> <i>グレースケール入力</i> | 効果の強さを促進するマップをマスク |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 50.0</i> | ぼかしを適用する最大強さ。 ぼかしマップでマスクされているため、この設定はそのマップの黒い領域には影響しません。 |
| <b>異方性</b> <i>0.0 - 1.0</i> | オプションで、ブラーエフェクトに方向性を追加します。 [角度]パラメータによって駆動されます。 |
| <b>非対称</b> <i>0.0 - 1.0</i> | オプションで、サンプリングにバイアスを追加します。 [角度]パラメータによって駆動されます。 |
| <b>角度</b> <i>0.0 - 1.0</i> | [角度]：指向性とサンプリングバイアスを設定します。 |
| <b>サンプル</b> <i>1 - 16</i> | サンプルの量によって品質が決まります。 ブレードの量を掛けた値。 |
| <b>ブレード</b> <i>1 - 9</i> | サンプリングセクタの量により、品質が決まります。 サンプルの量で乗算します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nonuniform-example.gif" /><br><i>以下の例は、ブラーマップスロットのグラデーションランプ（90度）によって駆動されています。</i>
        </td>
    </tr>
</table>
