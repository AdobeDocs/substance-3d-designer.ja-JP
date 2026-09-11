---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry.html"
breadcrumb-title: ''
description: Symmetryノードを使用して、指定した軸に沿ってテクスチャをミラーリングし、対称パターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 対称
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 7%

---


# 対称

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry.resources/symmetry-9.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力イメージに対して各種のシンメトリ操作を実行します。 幾何学的シェイプを対称にするために使用できます。

このノードは[ミラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md)によく似ていますが、描画モードの制御が追加されています。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>対称モード</b> <i>ミラーY、ミラーX、斜め左、斜め右、ミラーX/Y、ミラーX/ミラーY、斜め左/斜め右、斜め右/斜め左、8</i> | 対称形状モードを選択します。 |
| <b>転送モード</b> <i>0 - 6</i> | 対称描画モード（コピー、追加、減算、乗算、サブを追加、最大、最小）を選択します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry.resources/symmetry-ex.png" />
        </td>
    </tr>
</table>
