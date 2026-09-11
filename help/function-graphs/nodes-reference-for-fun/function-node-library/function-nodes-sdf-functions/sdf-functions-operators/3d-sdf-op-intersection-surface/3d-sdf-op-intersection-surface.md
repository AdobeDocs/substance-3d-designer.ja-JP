---
title: 交差サーフェス
description: Designer > Substance合成グラフ >ノード合成のリファレンスグラフ > Substanceライブラリ> SDF 関数 >オペレータ> Intersection surface
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 1%

---


# 交差サーフェス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![交差サーフェスアイコン](./3d-sdf-op-intersection-surface.png "交差サーフェス")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

別のSDF図形と交差する基本SDF図形の部分のサーフェスを、Thicknessを調整して返します。

</td>
</tr>
</table>

<a name='inputs'></a>

>[!INFO]
> 
> SDF 関数に関する概念やワークフローについて詳しくは、専用ページ（[SDF 関数の操作](../../working-with-sdf-functions.md)）を参照してください

## 入力

|  |  |
| :--- | :--- |
| <b>基本SDF</b> *フロート* | 作成されるサーフェスの基になるSDFシェイプ。 |
| <b>交差するSDF</b> *フロート* | 基本SDFシェイプと交差するSDFシェイプ。 |
| <b>Thickness</b> *フロート* | 結果のサーフェスのThickness。<br><br><i>既定： 0.02</i> |
