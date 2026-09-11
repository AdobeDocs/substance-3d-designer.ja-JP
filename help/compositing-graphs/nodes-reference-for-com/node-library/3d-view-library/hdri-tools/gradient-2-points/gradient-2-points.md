---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-2-points.html"
breadcrumb-title: ''
description: グラデーション2点ノードを使用して、空と地面の色のトランジション用のHDRI環境で2点グラデーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient 2 Points
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラデーション2ポイント
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 5%

---


# グラデーション2ポイント

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-2-points.resources/gradient-2-points.png){width="250px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ユーザーが選択した2つのポイント間に2色のグラデーションを作成します。 結果は球面投影法に合わせて調整されます。 [線形グラデーション(HDRI)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/gradient-linear-hdri/gradient-linear-hdri.md)と似ていますが、1つのポイントではなく2つのポイントがあります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ポイント1の位置</b> | ユーザが選択した最初のポイント位置。 2D ビューにハンドルがあります。 |
| <b>ポイント1の色</b> <i>（カラー値）</i> | グラデーションの開始点のカラー。 |
| <b>ポイント1コントラスト</b> <i>0.0 - 1.0</i> | 最初のポイントマスクのコントラスト。 |
| <b>ポイント2の位置</b> | ユーザが選択した2点目の位置。 2D ビューにハンドルがあります。 |
| <b>ポイント2の色</b> <i>（カラー値）</i> | グラデーションの終了点のカラー。 |
| <b>ポイント2コントラスト</b> <i>0.0 - 1.0</i> | 2点目マスクのコントラスト。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-2-points.resources/gradient-ex2.gif" />
        </td>
    </tr>
</table>
