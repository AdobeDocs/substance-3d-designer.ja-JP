---
title: マテリアルを設定
description: SDFシーンのマテリアルのベースカラー、粗さ、メタルを設定します。
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 5%

---


# マテリアルを設定

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![マテリアルアイコンを設定](set-material.png "マテリアルを設定")

<b>In:</b> 3D関数>マテリアル

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDFシーンのマテリアルのベースカラー、粗さ、メタルを設定します。

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
| <b>SDFシーン</b> *フロート* | 入力SDFシーン。 |
| <b>基本色</b> *浮動小数点3* | 設定するRGBのベースカラー値。 |
| <b>メタル</b> *フロート* | 設定するメタネス値。 |
| <b>粗さ</b> *フロート* | 設定する粗さの値。 |
