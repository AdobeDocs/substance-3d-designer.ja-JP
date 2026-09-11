---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/noise-upscale-1.html"
breadcrumb-title: ''
description: ノイズの解像度を上げる場合に詳細を維持するために、ノイズベースのアルゴリズムを使用してテクスチャをアップスケールするには、 テクスチャアップスケール1ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Noise Upscale 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ノイズアップスケール1
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 6%

---


# ノイズアップスケール1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](noise-upscale-1.resources/noise-upscale.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力ノイズをプロシージャルし、最大2倍の解像度に拡大します。細部は維持されますが、タイリング度をあまり上げることはありません。 「X」タイプのマスクを使用し、元の入力と同様のコントラストでブレンドします（内部ブレンドモードはコピー）。

このノードは主に、重くて大きなノイズを使用する遅いグラフを最適化するためのものです。 これにより、計算時間をあまり長くすることなく、より高い解像度を使用できます。

このプロセスのバリエーションについては、[ノイズアップスケール2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-2/noise-upscale-2.md)および[ノイズアップスケール3](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/noise-upscale-3/noise-upscale-3.md)も参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>オフセット1X</b> <i>0.0 - 1.0</i> | 上パーツと下パーツをX軸にスライドさせます。 |
| <b>オフセット1Y</b> <i>0.0 - 1.0</i> | 上パーツと下パーツをY軸にスライドさせます。 |
| <b>Offset2X</b> <i>0.0 - 1.0</i> | 左右のパーツをX軸にスライドさせます。 |
| <b>Offset2Y</b> <i>0.0 - 1.0</i> | 左右のパーツをY軸にスライドさせます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="noise-upscale-1.resources/noise1ex.png" />
        </td>
    </tr>
</table>
