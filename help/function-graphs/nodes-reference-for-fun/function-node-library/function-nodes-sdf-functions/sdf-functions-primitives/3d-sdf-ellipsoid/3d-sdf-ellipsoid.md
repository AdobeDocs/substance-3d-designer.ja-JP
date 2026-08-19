---
title: 楕円体
description: Designer/Substance合成グラフ/ノード合成の参照グラフ/Substanceライブラリ/SDF 関数/プリミティブ/準拠楕円体
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 1%

---


# 楕円体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![準拠楕円体アイコン](./3d-sdf-ellipsoid.png "準拠楕円体")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

楕円体のSDF 関数は、調整可能な三次元の半径の丸みを帯びた形状です。

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
| <b>半径</b> *浮動小数点3* | X、Y、Zの楕円体の半径。<br><br><i>既定： (0.35、0.35、0.5)</i> |
| <b>中央位置</b> *浮動小数点3* | 準拠楕円体の基点のワールドスペース位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
