---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 3DテクスチャSDFノードを使用して、滑らかな形状と効果を作成するために、3Dデータから署名付き距離フィールドテクスチャを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3DテクスチャSDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# 3DテクスチャSDF

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf.png){width="200px"}

**イン：** *フィルター/効果*

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**3DテクスチャSDF**&#x200B;ノードは、図形の&#x200B;*体積*&#x200B;のスライスを表す&#x200B;**入力**&#x200B;の&#x200B;*3Dテクスチャ*&#x200B;マスクから、図形の&#x200B;*署名付き距離フィールド*&#x200B;を生成します。

</td>
</tr>
</table>

## パラメーター

### 入力

* **マスク入力** *グレースケール*\
  図形の&#x200B;*体積*&#x200B;のスライスを表す&#x200B;*3Dテクスチャ*&#x200B;マスクです。

### パラメーター

* **しきい値** *浮動小数点*\
  シェイプのボリュームが&#x200B;*フェードグラデーション*&#x200B;で記述されている場合、シェイプの&#x200B;*サーフェス*&#x200B;が&#x200B;*検出*&#x200B;されるグラデーション値を設定します。
* **出力** *整数*\
  出力する距離フィールドのタイプ：
  * *距離フィールド*：図形の&#x200B;*外側*&#x200B;の距離を示す距離フィールドを出力します。
  * *符号付き距離場*：図形の&#x200B;*外側* （正）と&#x200B;*内側* （負）の距離を示すディスタンスフィールドを出力します。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesdf-node.png){width="256px"}

</td>
</tr>
</table>
