---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Extend Shapeノードを使用して、シェイプの境界を超えてシェイプを拡張し、拡張されたマスクおよびパターン効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

**イン:**&#x200B;フィルター*/効果*

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**Extend Shape**&#x200B;ノードは、**入力**&#x200B;の&#x200B;*セクション*&#x200B;を設定された方向と距離に拡張します。

**Show helper**&#x200B;パラメーターを使用すると、拡張セクションと拡張方向を視覚化できます。

</td>
</tr>
</table>

## パラメーター

* **モード** *整数*&#x200B;拡張機能の適用に使用する&#x200B;*パラメーター*&#x200B;を定義します：
  * *双方向*: **拡張位置**&#x200B;および&#x200B;**拡張角度**&#x200B;によって指定された&#x200B;**入力**&#x200B;のセクションは、**拡張距離**&#x200B;を超えて、*反対方向*&#x200B;に拡張されます
  * *一方向*: **拡張位置**&#x200B;および&#x200B;**拡張角度**&#x200B;で指定された&#x200B;**入力**&#x200B;のセクションは、*単一方向*&#x200B;で&#x200B;**拡張距離**&#x200B;を超えて拡張されています
  * *開始位置/終了位置*：拡張&#x200B;*ベクトル*&#x200B;は、**開始位置**&#x200B;と&#x200B;**終了位置**&#x200B;で定義されています。 **開始位置**&#x200B;の&#x200B;**入力**&#x200B;の&#x200B;*垂線*&#x200B;セクションは、**終了位置**&#x200B;までこのベクトル&#x200B;*に*&#x200B;延長されます
* **拡張距離** *浮動小数点* **拡張位置**&#x200B;および&#x200B;**拡張角度**&#x200B;で指定されたセクションを拡張する距離です。 距離は、画像スパンの&#x200B;*比率*&#x200B;で表されます。
* **拡張位置** *浮動小数点*&#x200B;拡張する必要があるセクションの画像内の位置です。 値は、中心からの&#x200B;*オフセット*&#x200B;として表されます。
* **拡張角度** *浮動小数点*&#x200B;開始点が&#x200B;*垂直セクション*&#x200B;であることを考慮して、拡張する必要があるセクションの角度です。
* **開始位置** *浮動小数点2**拡張ベクター*&#x200B;の開始位置です。
* **終了位置** *Float2**拡張ベクター*&#x200B;の終了位置です。
* **開始輝度オフセット** *浮動小数点*&#x200B;拡張セクションの&#x200B;*前*&#x200B;の画像の領域に輝度オフセットを適用します。 この輝度オフセットは、セクションに続く画像の領域の輝度に合わせて&#x200B;*セクションに沿って補間*&#x200B;されます。\
  *注意*：このパラメーターは、ノードの&#x200B;**グレースケール**&#x200B;バージョンでのみ使用できます。
* **終了輝度オフセット** *浮動小数点*&#x200B;画像の領域に輝度オフセットを適用します&#x200B;*後*&#x200B;拡張セクション。 この輝度オフセットは、セクションの前の画像の領域の輝度までセクションに沿って&#x200B;*補間*&#x200B;されます。\
  *注意*：このパラメーターは、ノードの&#x200B;**グレースケール**&#x200B;バージョンでのみ使用できます。
* **ラムだ。 オフセットで黒のピクセル** *ブール値*&#x200B;を&#x200B;*真*&#x200B;に設定すると、*両方* **開始輝度オフセット**&#x200B;と&#x200B;**終了輝度オフセット**&#x200B;で指定された輝度オフセットは、*黒でない*&#x200B;ピクセル（つまり、値が0より大きいピクセル）にのみ適用されます。\
  *注意*：このパラメーターは、ノードの&#x200B;**グレースケール**&#x200B;バージョンでのみ使用できます。
* **フィルターモード** *整数*&#x200B;ピクセル間の&#x200B;*補間*&#x200B;でサンプリングされた結果を処理する方法を定義します：
  * *最も近い*: *同じ*&#x200B;値を正確にサンプリングします（高速）
  * *バイリニア*：結果にバイリニアフィルターを適用して、*より滑らかな*&#x200B;外観にします
* **ヘルパーの表示** *ブール値**拡張セクション*&#x200B;をオーバーレイとして視覚化し、拡張機能の&#x200B;*方向*&#x200B;を矢印で示します。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape.gif){width="512px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/extendshape-node.png){width="360px"}

</td>
</tr>
</table>
