---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/weave-generator.html"
breadcrumb-title: ''
description: Weave Generatorノードを使用して、Substance 3D Designerでプロシージャルな織布パターンとテキスタイルテクスチャを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Weave Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ウィーブジェネレータ
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 9%

---


# ウィーブジェネレータ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](weave-generator.resources/weave-generator.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、いくつかのオプションを持つ単純な織りパターンを生成します。 これにより、事前に定義された織りパターンよりも多くの制御が可能になり、他のノードでは達成できないパターンを提示します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>タイルX</b> <i>1 - 20</i> | X軸上で繰り返されるブロックの数を設定します。 |
| <b>タイルY</b> <i>1 - 20</i> | Y軸に繰り返すブロックの数を設定します。 |
| <b>図形</b> <i>0.0 - 1.0</i> | ステッチのカーブHeightプロファイルを設定します。 |
| <b>織り</b> <i>1 - 10</i> | ブロックあたりのステッチ数を設定します。 |
| <b>ギャップ</b> <i>0.0 - 1.0</i> | X方向とY軸のステッチの間隔を設定します。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="weave-generator.resources/weave-generator-ex.gif" />
        </td>
    </tr>
</table>
