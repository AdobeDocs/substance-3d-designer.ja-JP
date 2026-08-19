---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: 3Dボリュームマスクノードを使用して、3D位置に基づくボリュームマスクを作成し、高度なマテリアルエフェクトを実現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dボリュームマスク
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# 3Dボリュームマスク

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask.png){width="256px"}

**イン：**&#x200B;ジェネレーター*/パターン*

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**3Dボリュームマスク**&#x200B;ノードは、**位置**&#x200B;入力マップに基づいて、*プリミティブシェイプ*&#x200B;の表現を生成します。

</td>
</tr>
</table>

## パラメーター

### 入力

* **位置** *色*\
  プリミティブを表す&#x200B;*3D空間座標*&#x200B;を表すマップ。\
  **X/Y/Z**&#x200B;座標は、それぞれ&#x200B;**R/G/B**&#x200B;チャンネルにマップされます。

### パラメーター

* **図形** *整数*\
  表現する必要があるプリミティブ図形です。
  * *立方体*- *円柱*- *球*
* **スケール** *浮動小数点*\
  プリミティブの&#x200B;*グローバル*&#x200B;尺度を定義します。すべての軸に&#x200B;*均一*&#x200B;に適用されます。
* **サイズ** *浮動小数点3*\
  各軸上のシェイプのサイズを定義します。
* **位置入力** *整数*\
  **位置**&#x200B;入力を介して&#x200B;*スペースを表現*&#x200B;するメソッド：
  * *UV位置*: *UVマップ*&#x200B;を使用します。 X/Y(U/V)座標は、それぞれR/Gチャンネルにマッピングされる。 Z軸は&#x200B;*直交前方*&#x200B;ベクトルと見なされます。
  * *ワールド空間の位置*: *位置マップ*&#x200B;を使用して、プリミティブを3D空間にマップします。 X/Y/Z座標は、それぞれR/G/Bチャンネルにマップされます。
* **UVの位置** *浮動小数点2*\
  UV空間でのプリミティブの位置。\
  *注意*：このパラメーターは、**位置入力**&#x200B;パラメーターが&#x200B;*UV位置*&#x200B;に設定されている場合にのみ使用できます。
* **位置** *浮動小数点3*\
  ワールド空間でのプリミティブの位置。\
  *注意*：このパラメーターは、**Position Input**&#x200B;パラメーターが&#x200B;*ワールドスペース位置*&#x200B;に設定されている場合にのみ使用できます。
* **回転** *浮動小数点3*\
  ワールド空間でのシェイプの回転を定義します。
* **ぼかしの幅** *浮動小数点*\
  プリミティブのサーフェスから内側に&#x200B;*フェードするグラデーション*&#x200B;の幅を調整します。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dvolumemask-variant4.jpg){width="256px"}

</td>
</tr>
</table>
