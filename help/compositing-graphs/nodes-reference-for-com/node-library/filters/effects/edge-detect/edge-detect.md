---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/edge-detect.html"
breadcrumb-title: ''
description: エッジ検出ノードを使用して、アウトラインやエッジベースのマスクエフェクトを作成するためのテクスチャでエッジを検出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Edge Detect
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エッジ検出
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 7%

---


# エッジ検出

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/edge-detect.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

白黒画像のコントラストを検出し、そのコントラストを強調する黒と白のマスクの画像を作成します。

エッジに対して何らかのマスクが必要な場合に便利です。 コントラストの強い入力では最適に機能することに注意してください。必要に応じて、コントラストを調整してから、このノードに値を渡してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>エッジの幅</b> <i>1.0 - 16.0</i> | エッジの周囲の検出された領域の幅。 |
| <b>エッジの丸み</b> <i>0.0 - 16.0</i> | 生成されたマスクを丸め、ぼかし、滑らかにします。 |
| <b>反転</b> <i>False/True</i> | 結果を反転します。 |
| <b>許容範囲</b> <i>0.0 - 1.0</i> | エッジが表示される場所の許容差トレッシュホールド係数。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/edge-detect-ex.png" />
        </td>
    </tr>
</table>
