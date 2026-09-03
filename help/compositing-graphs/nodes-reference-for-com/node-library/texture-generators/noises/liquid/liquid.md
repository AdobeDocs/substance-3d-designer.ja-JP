---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/liquid.html"
breadcrumb-title: ''
description: 液体ノードを使用して、水、油、その他の流体サーフェスエフェクトを作成するための液体および流体パターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Liquid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 液体
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '93'
ht-degree: 9%

---


# 液体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](liquid.resources/liquid-01.png){width="128px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これは、[ガウスノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)の単純なバリエーションで、[それ自体で](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)ワープして、液体のような効果を生み出します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スケール</b> <i>1 - 128</i> | エフェクトのグローバルスケールを設定します。 |
| <b>障害</b> <i>0.0 - 1.0</i> | ノイズを位相シフトして、小さな変動を発生させます |
| <b>ワープの強さ</b> <i>0.0 - 1.0</i> | ワープ効果の強さを設定します。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="liquid.resources/liquid-02.gif" />
        </td>
    </tr>
</table>
