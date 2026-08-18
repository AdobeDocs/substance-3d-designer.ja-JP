---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/voronoi.html"
breadcrumb-title: ''
description: Voronoiノードを使用して、細胞のテクスチャや有機的なマテリアルエフェクトを作成するためのVoronoiパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Voronoi
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ボロノイ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '618'
ht-degree: 0%

---


# ボロノイ

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/voronoi.png){width="200px"}

**インチ：** *テクスチャジェネレーター* */ノイズ*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**Voronoi**&#x200B;ノードは、*Zダウンの正射投影*&#x200B;を使用して2Dイメージにマップされた3D Voronoiノイズを生成します。

このノードは、実際のノードではなく、[Cube GBuffers](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d-gbuffers/cube-3d-gbuffers.md)を入力としてテストできます（以下の図の例を参照）。

>[!WARNING]
>
> このノイズは、*GPUエンジンのみ* （**Direct**&#x200B;または&#x200B;**OpenGL**）で使用することを目的としています。 **ツール/エンジンの切り替え…**&#x200B;に移動するか、**F9**&#x200B;キーを押して、目的のエンジンを選択します。

</td>
</tr>
</table>

## パラメーター

* **反転** *ブール値*\
  出力イメージを反転します。
* **スケール** *浮動小数点*\
  ボロノイノイズのスケールを制御します。\
  *注意*: *任意の軸*&#x200B;で&#x200B;**タイル**&#x200B;が有効になっている場合、スケール調整は&#x200B;*段階的*&#x200B;です。 これは予期される動作です。
* **サイズ** *浮動小数点3*\
  **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のボロノイノイズのサイズを制御します。 値が均一でないと、*伸縮*&#x200B;効果が発生します。\
  *注意*: *任意の軸*&#x200B;で&#x200B;**タイル**&#x200B;が有効になっている場合、サイズ調整は&#x200B;*段階的*&#x200B;です。 これは予期される動作です。
* **オフセット** *浮動小数点3*\
  **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のボロノイノイズの&#x200B;*位置*&#x200B;にオフセットを適用します。
* **障害** *フロート3*\
  *ランダムオフセット*&#x200B;の強度は、**X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のノイズの各点に適用されます。
* **ゆがみの適用度** *浮動小数点*\
  ボロノイノイズに適用される&#x200B;*ワープ効果*&#x200B;の強度を制御します。
* **ゆがみスケール乗数** *浮動小数点*\
  **ゆがみの強さ**&#x200B;で制御されるワープ効果で使用される&#x200B;*変形パターン*&#x200B;のスケールを制御します。
* **角丸曲線** *浮動小数点*\
  ノイズの各点の周りに&#x200B;*勾配*&#x200B;を丸めて、*凸状*&#x200B;にします。\
  *注意* : **Style**&#x200B;パラメーターが&#x200B;*Edge*&#x200B;に設定されている場合、このパラメーターは使用できません。
* **距離スケール** *浮動小数点*\
  ノイズの各点の周囲の&#x200B;*グラデーションの距離*&#x200B;を調整します。
* **距離モード** *整数*\
  ノイズの各点の周囲の距離グラデーションを&#x200B;*計算*&#x200B;するようにメソッドを設定します：
  * *ユークリッド*
  * *マンハッタン*
  * *チェビシェフ*
  * *ミンコフスキー*
* **ミンコフスキー数** *浮動小数点*\
  ミンコフスキー距離の次数&#x200B;*p*。 距離グラデーションを象限に分割すると、この数値は次のように象限に影響します。
  * pは&#x200B;*正確* 1：直線
  * pは1より&#x200B;*低い*&#x200B;です：凹型
  * pは1より&#x200B;*大きい*&#x200B;です：凸\
    対象の値：\
    *- 1.0*:マンハッタンの距離\
    *- 2.0*:ユークリッドの距離\
    *– 無限大*:チェビシェフの距離\
    *注意*：このパラメーターは、**Distance Mode**&#x200B;パラメーターが&#x200B;*Minkowski*&#x200B;に設定されている場合にのみ使用できます。
* **スタイル** *整数* Voronoiノイズのデータ&#x200B;*レンダリング方法*&#x200B;を設定します。ノイズは空間内の一連の点に基づいていると考えられます：
  * *F1*：空間内の&#x200B;*最も近い点*&#x200B;までの距離
  * *F2*：空間内の&#x200B;*番目に近い点*&#x200B;までの距離
  * *F2-F1*- *F1\* F2 *-* F1/F2 *-*&#x200B;エッジ&#x200B;*:スペース内のノイズの各セル*&#x200B;間の*エッジ
  * *ランダムな色*:スペース内のノイズの各セルに&#x200B;*ランダムなフラットカラー*&#x200B;を割り当てます
* **エッジのThickness** *フロート*&#x200B;ボロノイノイズのセル間で検出されるエッジのThicknessを調整します。 X、Y、およびZ軸でエッジが検出されるため、セルの&#x200B;*深度*&#x200B;によっては、一部の厚みが他よりも速く増加する場合があります。\
  *注意*：このパラメーターは、**Style**&#x200B;パラメーターが&#x200B;*Edge*&#x200B;に設定されている場合にのみ使用できます。
* **ランダムカラーシードモード** *整数*\
  セルごとの色選択のランダムシードを&#x200B;*取得*&#x200B;する方法を設定します：
  * *グローバルランダムシード*:ノードによって継承されたシード&#x200B;*を使用します*
  * *手動シード*: *個別*&#x200B;シードを使用します\
    *注意*：このパラメーターは、**Style**&#x200B;パラメーターが&#x200B;*Random color*&#x200B;に設定されている場合にのみ使用できます。
* **ランダムカラーシード** *整数*\
  セルごとのカラー選択に使用する個別のランダムシード。\
  *注意*：このパラメーターを使用できるのは、**Style**&#x200B;パラメーターを&#x200B;*ランダムな色*&#x200B;に設定し、**ランダムカラーシードモード**&#x200B;パラメーターを&#x200B;***手動シード***&#x200B;に設定した場合のみです。
* **非正方形拡張** *ブール値*\
  スカッシュとストレッチを非正方形の比率で補正できます。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/voronoi-variant6.jpg){width="256px"}

</td>
</tr>
</table>
