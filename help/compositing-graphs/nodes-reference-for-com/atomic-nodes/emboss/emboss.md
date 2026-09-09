---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/emboss.html"
breadcrumb-title: ''
description: '[エンボス]ノードを使用して、テクスチャにエンボス効果を加え、サーフェスのディテールに深度とリリーフを加えます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: エンボス
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca8beeed4bcddc6518237761ba87c319a1624018
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 9%

---


# エンボス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomicノード：エンボス](emboss.resources/comp_emboss_1.png "Atomicノード：エンボス"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

画像内の形状の側面を、指定した光源方向に合わせて照明することで、エンボス効果を適用します。

すなわち、2つの入力に基づいて単純な2Dシェーディングを行い、Heightと深度変動を伴う光をサーフェス上に落としてシミュレートします。

</td>
</tr>
</table>

このノードはPBRのようなプロジェクトではあまり使用されませんが、テクスチャにベイク処理されたシンプルなライティングが必要な場合に使用できます。 代わりに、[グロスによるエンボス](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/emboss-with-gloss/emboss-with-gloss.md)と[Uberエンボス](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/uber-emboss/uber-emboss.md)を使用すると、同様の機能が、より広範な機能を利用できます。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>適用度</b> *フロート* | イルミネーションエフェクトのグローバルな強度を調整します。   「Height」マップの強さを設定し、照明効果の強さを設定します |
| <b>明るい角度</b> *フロート* | ライトをシミュレートする角度を設定します。   エンボス画像のハイライトの照明角度を定義します |
| <b>ハイライトの色</b> *フロート/フロート4* | 明るい角度に向いている領域のカラーを設定します。   入力画像がカラーの場合にハイライトのカラーを設定します。 |
| <b>シャドウの色</b> *フロート/フロート4* | 明るい角度から遠ざかる領域のカラーを設定します。   エンボス画像のシャドウ領域のカラーを設定します。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー*&#x200B;プライマリ | シェーディングされていない基本カラーを提供します。 拡散反射光テクスチャまたはベースカラーテクスチャの一種として表示します。 |
| <b>強度入力</b> *グレースケール* | サーフェス上の照明の計算に使用する高さマップを表します。 黒は低く、白は高い。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
