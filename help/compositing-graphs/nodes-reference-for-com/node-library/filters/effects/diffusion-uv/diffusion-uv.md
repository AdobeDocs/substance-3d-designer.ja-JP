---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: 拡散UVノードを使用してUV空間に拡散エフェクトを適用し、カラーの変化を滑らかにしてブレンドを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拡散UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---


# 拡散UV

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/diffusion-uv-icon.png){width="200px"}

**場所：** *フィルター/効果*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

指定された&#x200B;**マスク**&#x200B;画像入力に従って&#x200B;**ソース**&#x200B;画像入力のUV座標に誤差拡散処理を適用し、**ソース**&#x200B;からの値の間の座標を補間します。

マスクに一致するピクセルのUVだけが拡散され、他のピクセルは拡散されません。

タイリングは特別な方法で処理されます：タイリングが&#x200B;*有効* （デフォルトでは有効）の場合、隣接する座標は0/1の制限を超えて平均することができます。

たとえば、あるピクセルでU座標値が0.1、別のピクセルで0.8の場合、座標の&#x200B;*タイリング*&#x200B;と仮定されるため、平均値は0.45ではなく0.95になります。 これは、実際のピクセル位置とは関係ありません。座標値は、画像全体で同じように処理されます。

このフィルターを&#x200B;*テクスチャ変形*&#x200B;に使用すると、望ましくない結果が生じる可能性があります。 その場合は、マスクで「コントロールカーブ/ポイント」が&#x200B;*テクスチャの長さの半分*&#x200B;以内に定義されていることを確認してください。

</td>
</tr>
</table>

## パラメーター

* **反復回数**: *0.0 ～ 64.0*&#x200B;実行するディフュージョン反復回数です（値を大きくすると良くなりますが、時間がかかります）。 有効な値は[8, 48]の範囲です。\
  数学的な正確さを求めていない場合は、低い値でも良い結果が得られます。

## 入力

* **ソース** *色*\
  拡散するUV。 このフィルターでは、タイル表示が特別な方法で処理されることに注意してください（*説明*&#x200B;を参照）。
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
