---
title: オフセットP
description: Designer > Substance合成グラフ >ノード合成のリファレンスグラフ > Substanceライブラリ> SDF 関数 > 変形 >オフセットP
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 1%

---


# オフセットP

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![オフセットPアイコン](./3d-sdf-transform-offset-p.png "オフセットP")

<b>イン：</b> SDF 関数 >変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベクトルに沿ってワールド空間をオフセットします。<br>出力の変形されたワールド位置は、この変形されたワールド空間で定義するために、ほとんどのSDF 関数の<b>P</b>入力に接続できます。<br><br><i>ヒント：</i> P変形は連鎖できますが、結果は演算の順序に依存することに注意してください。

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
| <b>オフセット</b> *浮動小数点3* | ワールド空間がX、Y、Z方向にオフセットされる距離。 |
| <b>P</b> *浮動小数点3* | ワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
