---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-voronoi.html"
breadcrumb-title: ''
description: 3D Voronoiノードを使用すると、3Dワールドポジションに基づいてボロノイパターンを生成し、体積細胞テクスチャを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D Voronoi
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '545'
ht-degree: 0%

---


# 3D Voronoi

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi.png){width="200px"}

**イン：** *テクスチャジェネレーター* */ノイズ*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**3D Voronoi**&#x200B;ノードは、**Position Map**&#x200B;の入力に基づいて、3D空間でVoronoi ノイズを生成します。

このノードは、実際のベイク済みマップではなく、[Cube 3D GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)を入力としてテストできます（下図の例を参照）。

>[!WARNING]
>
> このノイズは、*GPUエンジンのみ* （**Direct3D**&#x200B;または&#x200B;**OpenGL**）で使用することを目的としています。 **ツール/エンジンの切り替え…**&#x200B;に移動するか、**F9**&#x200B;キーを押して、目的のエンジンを選択します。

</td>
</tr>
</table>

## パラメーター

* **反転** *ブール値*\
  出力イメージを反転します。
* **スケール** *浮動小数*\
  3Dボロノイノイズのスケールを制御します。\
  *注意*: *任意の軸*&#x200B;で&#x200B;**タイル**&#x200B;が有効になっている場合、スケール調整は&#x200B;*段階的*&#x200B;です。 これは予期される動作です。
* **サイズ** *浮動小数点3*\
  **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸の3Dボロノイノイズのサイズを制御します。 値が均一でないと、*伸縮*&#x200B;効果が発生します。\
  *注意*: **タイリング**&#x200B;が&#x200B;*任意の軸*&#x200B;で有効になっている場合、サイズの調整は&#x200B;*段階的*&#x200B;です。 これは予期される動作です。
* **オフセット** *浮動小数点3*\
  **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸の3D Voronoiノイズの&#x200B;*position*&#x200B;にオフセットを適用します。
* **障害** *浮動小数3*\
  *ランダムオフセット*&#x200B;の強度は、**X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のノイズの各点に適用されます。
* **ゆがみの適用度** *浮動小数点*\
  3Dボロノイノイズに適用される&#x200B;*ワープ効果*&#x200B;の強さを制御します。
* **ゆがみスケール乗数** *浮動小数*\
  **ゆがみの強さ**&#x200B;で制御されるワープ効果で使用される&#x200B;*変形パターン*&#x200B;のスケールを制御します。
* **角丸カーブ** *浮動小数*\
  *勾配*&#x200B;をノイズの各点の周りに丸めて、*凸型*&#x200B;にします。\
  *注意* : **Style**&#x200B;パラメーターが&#x200B;*Edge*&#x200B;に設定されている場合、このパラメーターは使用できません。
* **距離尺度** *浮動小数*\
  ノイズの各点の周囲の&#x200B;*グラデーションの距離*&#x200B;を調整します。
* **ディスタンスモード** *整数*\
  ノイズの各点の周囲の&#x200B;*距離グラデーションの計算*&#x200B;を行うように設定します：
  * *ユークリッド*
  * *マンハッタン*
  * *チェビシェフ*
  * *ミンコフスキー*
* **ミンコフスキー数** *浮動小数*\
  ミンコフスキー距離の次数&#x200B;*p*。 距離グラデーションを象限に分割すると、この数値は次のように象限に影響します。
  * pは&#x200B;*正確* 1：直線
  * pは1より&#x200B;*低い*&#x200B;です：凹型
  * pは1より&#x200B;*大きい*&#x200B;です：凸\
    対象の値：\
    *- 1.0*:マンハッタンの距離\
    *- 2.0*:ユークリッドの距離\
    *– 無限大*:チェビシェフの距離\
    *注意*：このパラメーターは、**Distance Mode**&#x200B;パラメーターが&#x200B;*Minkowski*&#x200B;に設定されている場合にのみ使用できます。
* **スタイル** *整数* 3D空間の一連の点に基づくノイズを考慮して、3Dボロノイノイズの&#x200B;*データのレンダリング*&#x200B;方法を設定します：
  * *F1*: 3D空間の&#x200B;*最も近い点*&#x200B;までの距離
  * *F2*: 3D空間の&#x200B;*2番目に近い点*&#x200B;までの距離
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;エッジ&#x200B;*: 3Dスペースのノイズの各セル*&#x200B;の間の*エッジ
  * *ランダムな色*: 3Dスペースのノイズの各セルに&#x200B;*ランダムなフラットな色*&#x200B;を割り当てます
* **エッジのThickness** *浮動小数* 3Dボロノイノイズのセル間で検出されるエッジのThicknessを調整します。 X、Y、およびZ軸でエッジが検出されるため、セルの&#x200B;*深度*&#x200B;によっては、一部の厚みが他よりも速く増加する場合があります。\
  *注意*：このパラメーターは、**Style**&#x200B;パラメーターが&#x200B;*Edge*&#x200B;に設定されている場合にのみ使用できます。
* **タイリングを有効にする** *ブーリアン*\
  3Dボロノイノイズを調整して、結果のパターンがX、Y、Z軸に&#x200B;*繰り返す*&#x200B;ようにします。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvoronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
