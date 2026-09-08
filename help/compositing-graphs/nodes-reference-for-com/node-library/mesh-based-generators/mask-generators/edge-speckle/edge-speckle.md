---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/edge-speckle.html"
breadcrumb-title: ''
description: '[エッジの斑点]ノードを使用して、メッシュエッジに斑点のある摩耗パターンを生成し、リアルなエッジのダメージ効果を作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Edge Speckle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジの斑点
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f071c204e1a6c09a04372b7bdaf7cd044080fcc
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 6%

---


# エッジの斑点

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-speckle.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、エッジを分割するためのわずかな斑点が追加されたエッジを表します。 [エッジDirt](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/edge-dirt/edge-dirt.md)も参照してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | エッジのハイライトに使用するベイク済みマップ。 必須！ |
| <b>バリエーションマスク</b> <i>グレースケール入力</i> | ノードのエフェクトをマスクするために使用するオプションのマスクスロット。 「バリエーションマスクを上書き」で有効にします。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | エッジのハイライト表示の合計量を設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>エッジの選択</b> <i>0.0 - 1.0</i> | 凸状エッジの影響を設定します。 |
| <b>バリエーション</b> <i>0.0 - 1.0</i> | バリエーションマスクが効果を分割する範囲を設定します。 |
| <b>バリエーションマスクの上書き</b> <i>False/True</i> | カスタム入力スロットで組み込みマスクを上書きします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-speckle-ex.gif" />
        </td>
    </tr>
</table>
