---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/mirror-filter-node.html"
breadcrumb-title: ''
description: ミラーフィルターノードを使用すると、テクスチャを水平方向または垂直方向にミラーして、シンメトリーなパターンやエフェクトを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Mirror (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ミラー（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 4%

---


# ミラー（フィルタノード）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mirror-filter-node.resources/mirror-2.png){width="128px"}

![](mirror-filter-node.resources/mirror-grayscale.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

選択した軸で、選択した側から入力画像を鏡像化します。 対称的な効果をすばやく得るための非常に便利な方法です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>モード</b> <i>ミラー軸X、ミラー軸Y、コーナーをミラー</i> | 左右対称、上下対称、またはその両方を選択します。 |
| <b>軸 Xオフセット</b> <i>0.0 - 1.0</i> | 軸Xが選択されている場合にのみ使用され、オフセットを定義します。 |
| <b>軸 Yオフセット</b> <i>0.0 - 1.0</i> | 軸Yが選択されている場合にのみ使用され、オフセットを定義します。 |
| <b>軸X</b>を反転 <i>False/True</i> | [軸X]が選択されている場合にのみ使用されます。[方向を反転]を選択します。 |
| <b>軸Yを反転</b> <i>False/True</i> | [軸Y]が選択されている場合にのみ使用されます。[方向を反転]を選択します。 |
| <b>角の種類</b> <i>左上、右上、左下、右下</i> | コーナータイプを選択した場合にのみ使用し、ミラーの基準となるコーナーを定義します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mirror-filter-node.resources/mirror-example.png" />
        </td>
    </tr>
</table>
