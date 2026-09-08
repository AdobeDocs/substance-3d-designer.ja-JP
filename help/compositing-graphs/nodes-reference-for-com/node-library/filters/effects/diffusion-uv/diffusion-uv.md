---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: UVノードを使用してUV空間に拡散効果を適用し、滑らかな色の変化とブレンドを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# UV

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**場所：** *フィルター/効果*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

指定された&#x200B;**マスク**&#x200B;画像入力に従って&#x200B;**ソース**&#x200B;画像入力のUV座標に拡散プロセスを適用し、**ソース**&#x200B;からの値の間の座標を補間します。

マスクに一致するピクセルのUVだけが拡散され、他のピクセルは拡散されません。

タイリングは特別な方法で処理されることに注意してください。タイリングが&#x200B;*有効*&#x200B;の場合（デフォルトでは有効）、周辺座標は0/1の制限を超えて平均化されます。

たとえば、あるピクセルでU座標値が0.1、別のピクセルで0.8の場合、*座標のタイリング*&#x200B;と仮定されるため、平均値は0.45ではなく0.95になります。 これは、実際のピクセル位置とは関係ありません。座標値は、画像全体で同じように処理されます。

このフィルターを&#x200B;*テクスチャの変形*&#x200B;に使用すると、望ましくない結果が生じる可能性があります。 その場合は、マスクで「コントロールカーブ/ポイント」が&#x200B;*テクスチャの半分*&#x200B;以内に定義されていることを確認してください。

</td>
</tr>
</table>

## パラメーター

* **反復**: *0.0 ～ 64.0*&#x200B;実行する拡散反復の数です（値を大きくすると良くなりますが、時間がかかります）。 有効な値は[8, 48]の範囲です。\
  数学的な正確さを求めていない場合は、低い値でも良い結果が得られます。

## 入力

* **ソース** *色*\
  拡散するUV。 このフィルターでは、タイリングが特別な方法で処理されることに注意してください（*説明*&#x200B;を参照）。
* **マスク** *グレースケール*&#x200B;拡散マスク：白のピクセルが&#x200B;*ソース*&#x200B;でサンプリングされ、黒のピクセルで拡散されます。 画像は白黒である必要があります。 マスクにグラデーションが含まれている場合、カットオフ値は0.5です。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01a-after.jpg){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-before.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-01b-after.jpg){width="256px"}

</td>
</tr>
</table>
