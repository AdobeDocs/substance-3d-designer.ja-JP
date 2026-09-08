---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-linear-gradient.html"
breadcrumb-title: ''
description: 3D Linear gradientノードを使用して、空間効果の3Dワールド位置に基づいて線形グラデーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Linear Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Linear gradient
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 3%

---


# 3D Linear gradient

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-linear-gradient.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力の位置マップに基づいてボリュームグラデーションを作成します。 3D空間の2点間で黒から白へのトランジションを効果的に生成します。 GPU エンジンでのみ使用されます。

同様の効果については、[3Dボリュームマスク](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)も参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ポイント位置モード</b> <i>UV職位、ワールド空間職位</i> | グラデーションポイントを手動で正確に配置する場合は、UV空間（2D ビューに設定する場合に最適）で動作するか、3D座標で動作するかを選択します。 |
| <b>ポイント1</b> | グラデーションの開始点。 位置モードに基づいて2D座標または3D座標を指定できます。 |
| <b>ポイント2</b> | グラデーションの終点です。 位置モードに基づいて2D座標または3D座標を指定できます。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-gradient.gif" />
        </td>
    </tr>
</table>
