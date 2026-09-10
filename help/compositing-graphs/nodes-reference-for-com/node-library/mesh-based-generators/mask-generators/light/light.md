---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/light.html"
breadcrumb-title: ''
description: ライトノードを使用して、メッシュの照明条件に基づいてマスクを作成し、リアルなマテリアルバリエーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライト
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 9%

---


# ライト

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](light.resources/light-2.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて、黒と白のマスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)と同様。

このマスクは、他のジェネレータとは少し異なります。ワールド空間のNormalmapに基づいて、白黒の「Lightmap」マスクを返す、純粋に偽の照明を行います。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>水平角度</b> <i>0.0 - 1.0</i> | フェイクライトの水平角度を設定します。 |
| <b>頂角</b> <i>0.0 - 1.0</i> | フェイクライトの頂角を設定します。 |
| <b>光沢度の強調表示</b> <i>0.0 - 0.999</i> | ハイライト表示された領域のフォールオフの広がりを設定します。 |
| <b>ハイライトレベル</b> <i>0.0 - 1.0</i> | ハイライト表示された領域の明るさのレベルを設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="light.resources/light-ex.gif" />
        </td>
    </tr>
</table>
