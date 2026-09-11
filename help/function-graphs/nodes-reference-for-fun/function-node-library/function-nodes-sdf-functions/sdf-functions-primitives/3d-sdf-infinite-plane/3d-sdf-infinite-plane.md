---
title: 無限平面
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ > Node library > SDF 関数 >プリミティブ> Infinite plane
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '136'
ht-degree: 1%

---


# 無限平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![無限平面アイコン](./3d-sdf-infinite-plane.png "無限平面")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

方向と位置を調整できる無限平面のSDF 関数。

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
| <b>標準</b> *浮動小数3* | 無限の平面のワールド空間法線ベクトル。このベクトルは、その方向を制御します。<br>ベクトルが正規化されています。<br><br><i>既定値： (0, 0, 1)</i> |
| <b>中央位置</b> *浮動小数* | 平面の基点のワールド空間位置。ワールド原点から平面の法線に沿った距離です。<br><br><i>既定値： 0</i> |
| <b>P</b> *浮動小数3* | ワールド空間の位置。 この入力を使用して、<b>Offset P</b>および<b>Rotate P</b>ノードを使用する他の変換を適用します。<br><br><i>既定：変換されていないワールド空間の位置。</i> |
