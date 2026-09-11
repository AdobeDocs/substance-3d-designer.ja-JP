---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/stripes.html"
breadcrumb-title: ''
description: Stripeノードを使用して、テクスチャを作成するためのカスタマイズ可能な幅、間隔、方向を持つストライプパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Stripes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ストライプ
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 11%

---


# ストライプ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](stripes.resources/stripes.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

タイリング、角度、ストライプパターンを生成します。 パターンは、常に連続性を確保するように自動的に調整されます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>Stripe</b> <i>1 - 100</i> | ストライプの量を設定します。 結果を自動的にシフトして、タイリングを確保します。 |
| <b>幅</b> <i>0.0 - 1.0</i> | Stripe幅を設定します。 |
| <b>柔らかさ</b> <i>0.0 - 1.0</i> | ストライプエッジの遷移を設定します。 |
| <b>シフト</b> <i>0 - 20</i> | ストライプを傾けます。 ストライプを自動的に追加してタイリングを確保します。 |
| <b>整列</b> <i>エッジ、中心</i> | シフトの基点を設定します。 |
| <b>フィルター</b> <i>False/True</i> | フィルタリングを有効にします。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="stripes.resources/stripes-ex.gif" />
        </td>
    </tr>
</table>
