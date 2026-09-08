---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: テクスチャ解像度を上げるときにディテールを保持するノイズベースのアルゴリズムを使用してテクスチャをアップスケールするには、ノイズアップスケール1ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ノイズアップスケール1
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# ノイズアップスケール1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/noise-upscale.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力ノイズの手続きを取り、ディテールを維持しながらタイリングをあまり発生させずに、2倍の解像度までスケールします。 「X」タイプのマスクを使用し、元の入力と同様のコントラストでブレンドします（内部ブレンドモードはコピー）。

このノードは、主に重くて大きなノイズを使用する遅いグラフの最適化を目的としています。 これにより、計算時間をあまり長くすることなく、より高い解像度を使用できます。

このプロセスのバリエーションについては、[ノイズアップスケール2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)および[ノイズアップスケール3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md)も参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>オフセット1X</b> <i>0.0 - 1.0</i> | 上パーツと下パーツをX軸にスライドさせます。 |
| <b>オフセット1Y</b> <i>0.0 - 1.0</i> | 上部と下部をY軸に沿ってスライドします。 |
| <b>Offset2X</b> <i>0.0 - 1.0</i> | 左右のパーツをX軸にスライドさせます。 |
| <b>Offset2Y</b> <i>0.0 - 1.0</i> | 左右のパーツをY軸にスライドさせます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/noise1ex.png" />
        </td>
    </tr>
</table>
