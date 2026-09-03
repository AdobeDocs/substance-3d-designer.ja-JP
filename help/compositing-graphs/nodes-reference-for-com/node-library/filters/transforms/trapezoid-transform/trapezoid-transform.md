---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/trapezoid-transform.html"
breadcrumb-title: ''
description: 台形トランスフォームノードを使用して、テクスチャに台形ゆがみを適用し、遠近感の補正効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Trapezoid Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 台形変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 6%

---


# 台形変換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](trapezoid-transform.resources/trapezoid-transform-01.png){width="128px"}

![](trapezoid-transform.resources/trapezoid-transform-02.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

遠近法/台形ワープで入力を変更する特殊な変形ノード。 上下の伸縮を制御できます。 より強いエフェクトを得るには、値を制限を超える値に設定します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>トップ伸縮</b> <i>0.0 - 1.0</i> | 上部に伸縮またはスカッシュの量をセットします。 |
| <b>下の伸縮</b> <i>0.0 - 1.0</i> | ボタンに伸縮やカボチャの量をセットします。 |
| <b>背景色</b> <i>（グレースケール/カラー値）</i> | タイル表示がオフになっている場合は、単色の背景色を設定します。 |
| <b>サンプリング</b> <i>バイリニア、最も近い</i> | サンプリング品質を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="trapezoid-transform.resources/trapezoid-transform-03.gif" />
        </td>
    </tr>
</table>
