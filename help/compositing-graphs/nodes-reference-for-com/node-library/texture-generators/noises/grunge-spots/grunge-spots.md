---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-spots.html"
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
source-git-commit: 78ee271bee643682c3815dd1657d66accb2f31c4
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 2%

---


# 経年劣化斑

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/grungespots.jpg){width="200px"}

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
| <b>残高</b> <i>浮動小数</i> | 暗い値と明るい値のバランスを調整します。 |
| <b>コントラスト</b> <i>浮動小数</i> | 画像のコントラストを調整します。 |
| <b>反転</b> <i>ブーリアン</i> | `1-x`操作を使用して画像の出力を反転します。 |
| <b>非正方形拡張</b> <i>ブーリアン</i> | カボチャと伸縮の補正を非正方形の比率で有効にします。 |
| <b>詳細</b> |  |
| <b>詳細</b> <i>浮動小数</i> | *ワープ*&#x200B;したスポットの量を調整し、細かいスポットに分割します。 |
| <b>適用範囲</b> <i>浮動小数</i> | 画像内のスポットの範囲を調整します。 |
| <b>カバレッジのコントラスト</b> <i>浮動小数</i> | 画像内のスポットの範囲を制御するために使用される&#x200B;*マスク*&#x200B;のコントラストを調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/grungespots-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/grungespots-variant.jpg" />
        </td>
    </tr>
</table>
