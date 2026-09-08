---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-notch.html"
breadcrumb-title: ''
description: '[エッジノッチ]ノードを使用して、メッシュエッジにノッチパターンを生成し、リアルなエッジのダメージやインデント効果を作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Notch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジノッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 5%

---


# エッジノッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-notch.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、高周波ノイズによって分割されたエッジの単純なマスクです。 その他のオプションについては、[エッジDirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)または[エッジの損害](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-damages/edge-damages.md)を参照してください。

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
| <b>レベル</b> <i>0.0 - 1.0</i> | エッジノッチエフェクトのレベルを設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-notch-ex.gif" />
        </td>
    </tr>
</table>
