---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dripping-rust.html"
breadcrumb-title: ''
description: '[滴下]錆ノードを使用して、メッシュジオメトリと重力方向に基づいて錆の滴下パターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dripping Rust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 滴下錆
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 7%

---


# 滴下錆

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/dripping-rust.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて、黒と白のマスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)と同様。

このマスクは、錆のフレークと斑点を表し、漏れが伝わります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲率</b> <i>グレースケール入力</i> | 錆の配置に役立つマップをベイクまたは生成しました。 |
| <b>Ambient occlusion</b> <i>グレースケール入力</i> | 錆の配置に役立つマップをベイクまたは生成しました。 |
| <b>位置</b> <i>グレースケール入力</i> | 点滴方向のマップをベイクまたは生成しました。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>錆の分散</b> <i>0.0 - 1.0</i> | 錆量のメインコントロールです。 |
| <b>錆のコントラスト</b> <i>0.0 - 1.0</i> | 生成される錆の斑点のコントラストの量を設定します（滴り落ちには影響しません）。 |
| <b>Smoothnessを展開しています</b> <i>0.0 - 1.0</i> | 錆の斑点に適用するぼかし/にじみの効果の量。 |
| <b>滴の強さ</b> <i>0.0 - 1.0</i> | 斑点から滴り落ちる強さと長さを設定します。 |
| <b>Smoothnessの滴り</b> <i>0.0 - 1.0</i> | しずくに適用するぼかしとスムージングの量。 |
| <b>滴のサンプル量</b> <i>0 - 32</i> | ドロップエフェクトの画質レベル（ステップ）を設定します。 速度にわずかな影響を与えます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/dripping-rust-ex3.gif" />
        </td>
    </tr>
</table>
