---
title: 球
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ > Node library > SDF 関数 >プリミティブ> Sphere
source-git-commit: c3acf6cdb931126827d2a35dec1135800788ed81
workflow-type: tm+mt
source-wordcount: '103'
ht-degree: 3%
---

# 球面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![球のアイコン](./3d-sdf-sphere.png "球")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

単純な球のSDF 関数。

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
| <b>半径</b> *浮動小数* | 球の半径。<br><br><i>既定値： 0.5</i> |
| <b>中央位置</b> *浮動小数3* | 球の基点のワールド空間位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数3* | ワールド空間の位置。 この入力を使用して、<b>Offset P</b>および<b>Rotate P</b>ノードを使用する他の変換を適用します。<br><br><i>既定：変換されていないワールド空間の位置。</i> |
