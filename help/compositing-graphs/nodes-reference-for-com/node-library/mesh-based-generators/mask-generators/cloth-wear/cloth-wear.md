---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/cloth-wear.html"
breadcrumb-title: ''
description: クロスの摩耗ノードを使用して、曲率と接触領域に基づいてクロスサーフェスに摩耗マスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Cloth Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 布地の摩耗
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# 布地の摩耗

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cloth-wear.resources/cloth-wear-01.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

マスクは、布マテリアルのエッジのすり切れを表します。 効果の大部分を決定する布地のディテールの高さマップを使用します。適切なマップがなければ、効果は非常に基本的に見えます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>布のHeight</b> <i>グレースケール入力</i> | 布パターンのみのHeight。 これは、（ベイクされた）オブジェクトのHeightではなく、タイリングの詳細パターンです。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>曲線</b> <i>グレースケール入力</i> | 隆起したエッジを判別するためのベイク/生成された曲率。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ハードエッジの量</b> <i>0.0 - 1.0</i> |  |
| <b>柔らかさを加える</b> <i>0.0 - 5.0</i> | 損耗したエッジをぼかす/柔らかくする度合いを指定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cloth-wear.resources/cloth-wear-02.gif" />
        </td>
    </tr>
</table>
