---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/grease.html"
breadcrumb-title: ''
description: Greaseノードを使用して、メッシュジオメトリと接触領域に基づいてグリース蓄積マスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Grease
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グリース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 5%

---


# グリース

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grease.resources/grease-01.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて、黒と白のマスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)と同様。

このマスクは、特にキャラクタ面やその他の特定領域を対象としています。 Thicknessの低い領域にスキングリースタイプのマスクを生成します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Thickness</b> <i>グレースケール入力</i> | エフェクト全体の基になる厚みマップをベイクしました。 必須！ |
| <b>ノイズ</b> <i>グレースケール入力</i> | グリースデータを上書きするためのノイズ経年劣化マップ（オプション）。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | 表示するエフェクトの総量を設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>Thicknessしきい値</b> <i>0.0 - 1.0</i> | エフェクトを表示する最小Thicknessを設定します。 レベルも同様に重要です。Thicknessマップに合わせて調整してください。 |
| <b>ノイズの上書き</b> <i>False/True</i> | カスタム入力スロットで内部グリース経年劣化マップを上書きします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grease.resources/grease-02.gif" />
        </td>
    </tr>
</table>
