---
title: キャップ付き円錐2ポイント
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ> Node library > SDF 関数 >プリミティブ>キャップ付きコーン2ポイント
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# キャップ付き円錐2ポイント

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![円錐形の2ポイントアイコン](./3d-sdf-capped-cone-2-points.png "円錐形の2ポイント")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

底面と上面の位置によって定義される、キャップされた円錐のSDF 関数。<br>底面と上面の半径を調整できます。

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
| <b>位置の基準</b> *浮動小数点3* | 円錐の底面の位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>上に配置</b> *浮動小数点3* | 円錐の上部の位置です。<br><br><i>既定値： (0, 0, 1)</i> |
| <b>半径ベース</b> *フロート* | 円錐の底面の半径です。<br><br><i>既定値： 0.5</i> |
| <b>半径（上）</b> *フロート* | 円錐の上面の半径。<br><br><i>既定値： 0.2</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
