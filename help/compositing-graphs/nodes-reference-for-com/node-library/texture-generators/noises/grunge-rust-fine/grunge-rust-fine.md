---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/grunge-rust-fine.html"
breadcrumb-title: ''
description: 錆の微細ノードを使用して、金属に腐食および風化効果を加える微細な錆パターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Grunge Rust Fine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 錆罰金
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78ee271bee643682c3815dd1657d66accb2f31c4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 1%

---


# 錆罰金

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/grungerustfine.jpg){width="200px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**錆の詳細**&#x200B;ノードは、詳細な経年劣化錆オーバーレイに似た経年劣化マップを生成します。

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
| <b>基本経年劣化コントラスト</b> <i>フロート</i> | 錆のベースとして使用する経年劣化テクスチャのコントラストを調整します。 |
| <b>基本ワープの適用度</b> <i>フロート</i> | 錆のベースとして使用する経年劣化マップに適用するワープ効果の強さを調整します。 |
| <b>筋の強さ</b> <i>フロート</i> | ベーステクスチャに重なる明るい縞とスポットの強さを調整します。 |
| <b>ノイズの適用度</b> <i>フロート</i> | ベーステクスチャに適用されるノイズの強さを調整します。 |
| <b>シャープの適用度</b> <i>フロート</i> | グローバルなシャープ効果の適用度を調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/grungerustfine-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/grungerustfine-variant.jpg" />
        </td>
    </tr>
</table>
