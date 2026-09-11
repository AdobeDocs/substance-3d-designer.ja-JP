---
title: トーラス
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ >ノードライブラリ> SDF 関数 >プリミティブ>トーラス
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 2%

---


# トーラス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![トーラスアイコン](./3d-sdf-torus.png "トーラス")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

トーラスのSDF 関数。主円に沿って補助円をスイープして形成される形状です。<i>両方の円の半径を調整できます。

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
| <b>主半径</b> *フロート* | トーラスのサーフェスを形成するためにマイナーディスクをスイープする円の半径。<br><br><i>既定： 0.5</i> |
| <b>半径のマイナー</b> *フロート* | トーラスのサーフェスを形成するために主円に沿ってスイープされる円の半径。<br><br><i>既定： 0.2</i> |
| <b>中央位置</b> *浮動小数点3* | トーラスの基点のワールド空間位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | ワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
