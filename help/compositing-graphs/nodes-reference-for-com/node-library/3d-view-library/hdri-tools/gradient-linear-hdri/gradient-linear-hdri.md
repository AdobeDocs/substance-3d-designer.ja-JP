---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/gradient-linear-hdri.html"
breadcrumb-title: ''
description: グラデーション線形HDRIノードを使用して、カスタムの照明設定用のHDRI環境で線形グラデーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Gradient Linear (HDRI)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 線形グラデーション(HDRI)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 4%

---


# 線形グラデーション(HDRI)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](gradient-linear-hdri.resources/gradient-linear-hdri-01.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

中心を横切り、ユーザーがポイントを配置した線形グラデーションを作成します。 通常の[線形グラデーション1](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)とは異なり、最終結果は球面投影法を調整されます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ポイント位置</b> | グラデーションの方向の決定に使用するポイントの位置。 |
| <b>上の色</b> <i>（カラー値）</i> | グラデーションの上部のカラー（ポイント） |
| <b>下の色</b> <i>（カラー値）</i> | グラデーションの下部（点から離れた部分）のカラー。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="gradient-linear-hdri.resources/gradient-linear-hdri-02.gif" />
        </td>
    </tr>
</table>
