---
title: カプセル
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ> Node library > SDF 関数 >プリミティブ>カプセル
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# カプセル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![カプセルアイコン](./3d-sdf-capsule.png "カプセル")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

長さ及び半径を調整可能なカプセル用SDF 関数を提供する。<br>カプセルは2つの球をブリッジした結果です。

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
| <b>開始</b> *浮動小数点3* | 開始球の位置。<br><br><i>既定： (0, 0, 0)</i> |
| <b>終了</b> *浮動小数点3* | 終了球の位置。<br><br><i>既定： (0, 0, 1)</i> |
| <b>半径</b> *フロート* | 開始球と終了球の両方の半径。<br><br><i>既定値： 0.25</i> |
| <b>ヒントで開始/終了</b> *ブール値* | <b>開始</b>位置と<b>終了</b>位置を球の端に合わせるかどうかを制御します。<br>つまり、カプセルのHeightに球の半径を含めるかどうかを制御します。<br><br><i>既定値： False</i> |
| <b>中央位置</b> *浮動小数点3* | カプセルの基点のワールドスペース位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
