---
title: マテリアルを設定
description: SDFシーンのマテリアルのbase color、ラフネス、金属化を設定します。
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# マテリアルを設定

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![マテリアルアイコンの設定](set-material.png "マテリアルの設定")

<b>In:</b> 3D関数> マテリアル

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDFシーンのマテリアルのbase color、ラフネス、金属化を設定します。

これらの値は、[Shape splatter v2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)の出力で、すべてのスプラッタSDFシェイプに対して取得できます。

</td>
</tr>
</table>

>[!INFO]
> 
> SDF 関数に関する概念やワークフローについて詳しくは、専用ページ（[SDF 関数の操作](../../working-with-sdf-functions.md)）を参照してください

## 入力

|                            |                                  |
|----------------------------|----------------------------------|
| <b>SDF シーン</b> *浮動小数* | 入力SDF シーン。 |
| <b>Base color</b> *浮動小数3* | 設定するbase color値。 |
| <b>メタル</b> *浮動小数* | 設定するメタネス値。 |
| <b>ラフネス</b> *浮動小数* | 設定するラフネス値。 |
