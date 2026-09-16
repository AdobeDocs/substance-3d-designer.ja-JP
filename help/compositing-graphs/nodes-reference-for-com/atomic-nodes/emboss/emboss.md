---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ""
description: エンボスノードを使用して、テクスチャにエンボス効果を加え、サーフェスのディテールに深度とリリーフを加えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エンボス
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '255'
ht-degree: 9%
---

# エンボス

<table>
<tr style="border: 0;">
<td width="20%" style="border: 0;" valign="top">

![アトミックノード: エンボス](emboss.resources/comp_emboss_1.png "アトミックノード: エンボス"){width="100%"}

</td>
<td style="border: 0;" valign="top">

画像内の形状の側面を、指定した光源方向に合わせて照明することで、エンボス効果を適用します。

すなわち、2つの入力に基づいて単純な2Dシェーディングを行い、Heightと深度変動を伴う光をサーフェス上に落としてシミュレートします。

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="emboss.resources/emboss-tooltip.gif" alt="エンボスツールチップ" /></div>

このノードはPBRのようなプロジェクトでは頻繁に使用されませんが、テクスチャ内でシンプルでベイクされた照明が必要な場合に使用できます。 また、[グロスのエンボス](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md)と[Uberのエンボス](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)は、同様の機能を備えていますが、より広範な機能を提供します。



## パラメーター

|  |  |
| --- | --- |
| <b>適用度</b> *浮動小数* | イルミネーションエフェクトのグローバルな強度を調整します。   「Height」マップの強さを設定し、照明効果の強さを設定します |
| <b>明るい角度</b> *浮動小数* | ライトをシミュレートする角度を設定します。   エンボス画像のハイライトの照明角度を定義します |
| <b>ハイライトの色</b> *浮動小数/浮動小数4* | 明るい角度に向いている領域のカラーを設定します。   入力画像がカラーの場合にハイライトのカラーを設定します。 |
| <b>シャドウの色</b> *浮動小数/浮動小数4* | 明るい角度から遠ざかる領域のカラーを設定します。   エンボス画像のシャドウ領域のカラーを設定します。 |

## 入力コネクター

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー*&#x200B;プライマリ | シェーディングされていない基本カラーを提供します。 拡散反射光またはベースカラーテクスチャの一種として表示します。 |
| <b>強度入力</b> *グレースケール* | サーフェス上の照明の計算に使用する高さマップを表します。 黒は低く、白は高い。 |


## 例

*近日公開。*
