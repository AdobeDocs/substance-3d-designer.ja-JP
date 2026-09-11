---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dirt.html"
breadcrumb-title: ''
description: Dirtノードを使用して、メッシュの曲率、位置、オクルージョンに基づいてDirtのアキュムレーションマスクを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dirt
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 汚れ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 7%

---


# 汚れ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dirt.resources/dirt.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて、黒と白のマスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)と同様。

このマスクは、ベイクされたAOと曲率に基づいて、隠れたエッジと沈んだエッジおよびコーナーのDirtを表します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲率</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 必須！ |
| <b>Ambient occlusion</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 必須！ |
| <b>経年劣化入力</b> <i>グレースケール入力</i> | カスタム経年劣化マップ入力、オプション、パラメーターにより有効化 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>ワールド空間法線</b> <i>カラー入力</i> | Triplanarにのみ使用されます。 |
| <b>位置</b> <i>カラー入力</i> | Triplanarにのみ使用されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>Dirtレベル</b> <i>0.0 - 1.0</i> | Dirt量のメインコントロール。 |
| <b>Dirtのコントラスト</b> <i>0.0 - 1.0</i> | マスクのDirtのメインコントラストを制御します。 |
| <b>経年劣化量</b> <i>0.0 - 1.0</i> | Dirtのグランジ度合いを設定します。 Dirtを完全に滑らかにするには、0に設定します。 |
| <b>エッジのマスク</b> <i>0.0 - 1.0</i> | 隆起したエッジから取り除くDirtの量（曲率マップに基づく）。 |
| <b>カスタム経年劣化を使用する</b> <i>False/True</i> | 組み込み経年劣化の代わりにカスタム経年劣化マップ入力を使用できるようにします。 |
| <b>経年劣化スケール</b> <i>1 - 16</i> | 経年劣化詳細のタイリング尺度を設定します。 |
| <b>三平面を使用</b> <i>False/True</i> | 経年劣化マッピングに[トライプラナー投影](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)を使用すると、シームが削除されます。 |
| <b>3平面のブレンドコントラスト</b> <i>0.001 - 1.0</i> | トライプラナー投影のコントラストを設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dirt.resources/dirt-ex.gif" />
        </td>
    </tr>
</table>
