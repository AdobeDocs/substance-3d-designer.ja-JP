---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-perlin-noise-fractal.html"
breadcrumb-title: ''
description: 3Dパーリンノイズフラクタルノードを使用して、詳細なボリュームテクスチャを作成するための3D空間でフラクタルパーリンノイズパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Perlin Noise Fractal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dパーリンノイズフラクタル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '424'
ht-degree: 0%

---


# 3Dパーリンノイズフラクタル

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal.png){width="200px"}

**インチ：** *テクスチャジェネレーター**/ノイズ*

**中級**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**3Dパーリンノイズフラクタル**&#x200B;ノードは、**位置マップ**&#x200B;入力に基づいて、3D空間で&#x200B;*フラクタル*&#x200B;パーリンノイズを生成します。

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
* **スケール** *浮動小数点*\
  フラクタル3Dパーリンノイズの尺度をコントロールします。
* **サイズ** *浮動小数点3*\
  **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のフラクタル3Dパーリンノイズのサイズを制御します。 値が均一でないと、*伸縮*&#x200B;効果が発生します。
* **オフセット** *浮動小数点3*\
  **X**、**Y**&#x200B;および&#x200B;**Z**&#x200B;軸のフラクタル3Dパーリンノイズの&#x200B;*位置*&#x200B;にオフセットを適用します。
* **ゆがみの適用度** *浮動小数点*\
  フラクタル3Dパーリンノイズに適用される&#x200B;*ワープ効果*&#x200B;の強度を制御します。
* **ゆがみスケール乗数** *浮動小数点*\
  **ゆがみの強さ**&#x200B;で制御されるワープ効果で使用される&#x200B;*変形パターン*&#x200B;のスケールを制御します。
* **最小レベル** *整数*\
  フラクタルパターンで使用される繰り返しの最小&#x200B;*レベル*&#x200B;です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる&#x200B;*豊富なパターン*&#x200B;になります。
* **最大レベル** *整数*\
  フラクタルパターンで使用される繰り返しの最大&#x200B;*レベル*&#x200B;です。 最小値/最大値の範囲が広いほど、より多くの周波数範囲で変化が生じる&#x200B;*豊富なパターン*&#x200B;になります。
* **粗さ** *浮動小数点*\
  フラクタルパターンの低&#x200B;*繰り返しレベル*&#x200B;の間の&#x200B;*バランス*&#x200B;を制御します。\
  *注意*: **0**&#x200B;の値を指定すると、出力は&#x200B;*行*&#x200B;ではなく、その後に他の低い値が続きます。 これは予期される動作です。
* **空隙性** *浮動小数点*\
  適用されたフラクタルパターン&#x200B;*がスペースを塗りつぶす方法*&#x200B;を制御します。 *高い*&#x200B;値を指定すると、パターンのギャップが&#x200B;*少なくなり*、ノイズが&#x200B;*密度が高く*&#x200B;なります。
* **グローバルの不透明度** *浮動小数点*\
  フラクタル3Dパーリンノイズ値の&#x200B;*範囲*&#x200B;を制御します。**基準**&#x200B;値&#x200B;*前後*。
* **ベースライン** *浮動小数点*\
  *オフセット*&#x200B;を、3Dパーリンノイズ値の分布の基準&#x200B;*輝度*&#x200B;値に適用します。
* **コントラスト** *浮動小数点*\
  3Dパーリンノイズのコントラストを調整します。
* **絶対** *ブール値*\
  3Dパーリンノイズの絶対値を使用します。 これにより、値&#x200B;*が0.5*&#x200B;未満の場合に、値の分布が&#x200B;*反転*&#x200B;します。
* **タイル表示を有効にする** *ブール値*\
  3Dパーリンのノイズを調整して、結果のパターンがX、Y、Z軸で&#x200B;*繰り返される*&#x200B;ようにします。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dfractal.gif){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dperlinnoisefractal-variant2.jpg){width="256px"}

</td>
</tr>
</table>
