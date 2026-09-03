---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-spots.html"
breadcrumb-title: ''
description: 「経年劣化スポット」ノードを使用して、マテリアルに磨耗や経年劣化効果を加えるためのスポットパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Spots
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 経年劣化斑
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---


# 経年劣化斑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](grunge-spots.resources/grunge-spots-01.jpg){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**経年劣化スポット**&#x200B;ノードは、細かい飛び散ったスポットに似た経年劣化マップを生成します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>残高</b> <i>フロート</i> | 暗い値と明るい値のバランスを調整します。 |
| <b>コントラスト</b> <i>フロート</i> | 画像のコントラストを調整します。 |
| <b>反転</b> <i>ブール値</i> | `1-x`操作を使用して画像の出力を反転します。 |
| <b>非正方形拡張</b> <i>ブール値</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |
| <b>詳細</b> |  |
| <b>詳細</b> <i>フロート</i> | *ワープ*&#x200B;したスポットの量を調整し、細かいスポットに分割します。 |
| <b>適用範囲</b> <i>フロート</i> | 画像内のスポットの範囲を調整します。 |
| <b>カバレッジのコントラスト</b> <i>フロート</i> | 画像内のスポットの範囲を制御するために使用される&#x200B;*マスク*&#x200B;のコントラストを調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="grunge-spots.resources/grunge-spots-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="grunge-spots.resources/grunge-spots-03.jpg" />
        </td>
    </tr>
</table>
