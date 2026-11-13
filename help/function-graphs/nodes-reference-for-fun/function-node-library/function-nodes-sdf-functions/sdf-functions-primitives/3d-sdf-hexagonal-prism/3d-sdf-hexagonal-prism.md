---
title: 六角柱
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ >ノードライブラリ> SDF 関数 >プリミティブ>六角プリズム
source-git-commit: c3acf6cdb931126827d2a35dec1135800788ed81
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 1%
---

# 六角柱

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![六角プリズムアイコン](./3d-sdf-hexagonal-prism.png "六角プリズム")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

エッジのHeight、半径、丸みを調整できる6辺プリズム用のSDF 関数です。

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
| <b>Height</b> *浮動小数* | 六角形プリズムの底面からのZ-upHeight。<br><br><i>既定値： 1</i> |
| <b>半径</b> *浮動小数* | 六角形プリズムの半径。<br><br><i>既定： 0.5</i> |
| <b>丸め</b> *浮動小数* | 六角プリズムのエッジに適用される角丸円弧の半径。<br><br><i>注： </i>角丸半径が交差する部分にハードエッジが表示される場合があります。<br><br><i>既定： 0</i> |
| <b>中央位置</b> *浮動小数3* | 六角柱の基点のワールド空間位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数3* | ワールド空間の位置。 この入力を使用して、<b>Offset P</b>および<b>Rotate P</b>ノードを使用する他の変換を適用します。<br><br><i>既定：変換されていないワールド空間の位置。</i> |
