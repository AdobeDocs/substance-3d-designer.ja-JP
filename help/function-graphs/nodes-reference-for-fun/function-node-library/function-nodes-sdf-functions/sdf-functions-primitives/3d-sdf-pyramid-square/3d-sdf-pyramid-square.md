---
title: ピラミッド正方形
description: Designer > Substance合成グラフ >ノード合成のリファレンスグラフ > Substanceライブラリ> SDF 関数 >プリミティブ> ピラミッドスクエア
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# ピラミッド正方形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ピラミッド正方形のアイコン](./3d-sdf-pyramid-square.png "ピラミッド正方形")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Heightとベースの位置を調整できる、正方形のベースを持つピラミッド用SDF 関数です。

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
| <b>Height</b> *浮動小数* | ピラミッドの頂点の底からのZアップHeightです。<br><br><i>既定値： 1</i> |
| <b>基本サイズ</b> *浮動小数* | 角錐の底面のエッジの長さ。<br>すべてのエッジが同じ長さです。<br><br><i>既定： 1</i> |
| <b>基本位置</b> *浮動小数3* | ピラミッドの底面のワールド空間位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数3* | ワールド空間の位置。 この入力を使用して、<b>Offset P</b>および<b>Rotate P</b>ノードを使用する他の変換を適用します。<br><br><i>既定：変換されていないワールド空間の位置。</i> |
