---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-dirt.html"
breadcrumb-title: ''
description: エッジDirtノードを使用して、メッシュエッジにDirtのアキュムレーションマスクを作成し、リアルなエッジのウェザリングエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジDirt
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 6%

---


# エッジDirt

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](edge-dirt.resources/edge-dirt.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、Dirtマップのみに基づいてエッジの周囲に集まる曲率エフェクトを表します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | エフェクトの配置に使用されるベイク済みマップ。 必須！ |
| <b>バリエーションマスク</b> <i>グレースケール入力</i> | ノードのエフェクトをマスクするために使用されるマスクスロット。オーバーライドパラメータが有効な場合にのみ使用されます。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | Dirt量を設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>バリエーション</b> <i>0.0 - 1.0</i> | 大規模なマスク/分割を行う場合のブレンド。 |
| <b>バリエーションマスクの上書き</b> <i>False/True</i> |  |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="edge-dirt.resources/edge-dirt-ex.gif" />
        </td>
    </tr>
</table>
