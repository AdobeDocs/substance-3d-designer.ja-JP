---
title: 円柱2点
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ > Node library > SDF 関数 >プリミティブ> Cylinder 2 point
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 1%

---


# 円柱2点

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![円柱2ポイントアイコン](./3d-sdf-cylinder-2-points.png "円柱2ポイント")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

開始円盤と終了円盤の位置によって定義される半径を調整できる円筒のSDF 関数。

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
| <b>開始</b> *浮動小数点3* | 円柱の開始ディスクの位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>終了</b> *浮動小数点3* | 円柱の終了ディスクの位置です。<br><br><i>既定値： (0, 0, 1)</i> |
| <b>半径</b> *フロート* | 円柱の半径。<br><br><i>既定： 0.25</i> |
| <b>P</b> *浮動小数点3* | ワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
