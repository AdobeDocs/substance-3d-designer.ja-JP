---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-select.html"
breadcrumb-title: ''
description: エッジ選択ノードを使用して、エッジベースのウェザリングおよび摩耗効果を作成するためのメッシュエッジを選択するマスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジ選択
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '276'
ht-degree: 7%

---


# エッジ選択

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-select.resources/edge-select.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、曲率に基づいて任意の種類のエッジを選択する最適な方法です。 [レベルノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)を使用して手動で行う必要がない場合は、任意のレベルまたはコントラストの凸型と凹型を分離できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | エッジのハイライト表示に使用するベイク済みマップ。 必須！ |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | [凸状]と[凹状]の両方のエッジハイライトの合計量を設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | ハイライトのコントラストを[凸状]と[凹状]の両方で調整します。 |
| <b>凸型</b> |  |
| <b>凸型エッジの幅</b> <i>0.0 - 1.0</i> | 凸状エッジのハイライトの幅を設定します。 「柔らかさ」を少し上げると、エッジが薄くなる可能性があることに注意してください。 |
| <b>凸型の柔らかさ</b> <i>0.0 - 1.0</i> | 凸状エッジの変化の柔らかさを設定します。 |
| <b>凸強度</b> <i>0.0 - 1.0</i> | 凸状エッジのエッジハイライトの最大強度を設定します。 0に設定すると、ハイライト表示されません。 |
| <b>凹型</b> |  |
| <b>凹型エッジの幅</b> <i>0.0 - 1.0</i> | 凹状エッジのハイライトの幅を設定します。 「柔らかさ」を少し上げると、エッジが薄くなる可能性があることに注意してください。 |
| <b>凹形の柔らかさ</b> <i>0.0 - 1.0</i> | 凹状エッジの変化の柔らかさを設定します。 |
| <b>凹形の強度</b> <i>0.0 - 1.0</i> | 凹状エッジのエッジハイライトの最大強度を設定します。 0に設定すると、ハイライト表示されません。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-select.resources/edge-select-ex.gif" />
        </td>
    </tr>
</table>
