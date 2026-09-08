---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/plasma.html"
breadcrumb-title: ''
description: プラズマノードを使用して、有機的および流体のテクスチャエフェクトを作成するためのプラズマのようなノイズパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Plasma
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 血漿
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8774511f26429071b91a2eeeb8728ac36dc31ed5
workflow-type: tm+mt
source-wordcount: '88'
ht-degree: 7%

---


# 血漿

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/plasma.png){width="128px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これにより、長い暗い筋が谷となって現れる[ガウスノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/gaussian-noise/gaussian-noise.md)のバリエーションがわずかに異なります。 スケールの[距離]コントロールと同様に、タイリングを保ちます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スケール</b> <i>1 - 128</i> | エフェクトのグローバルスケールを設定します。 |
| <b>障害</b> <i>0.0 - 1.0</i> | ノイズを位相シフトして、小さな変動を発生させます。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/plasma-ex.gif" />
        </td>
    </tr>
</table>
