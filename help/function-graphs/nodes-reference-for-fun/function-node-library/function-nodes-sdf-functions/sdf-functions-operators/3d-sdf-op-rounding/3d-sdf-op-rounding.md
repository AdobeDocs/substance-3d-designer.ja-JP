---
title: 丸め
description: Designer/Substance合成グラフ/ノード合成の参照Substance合成グラフ/ノード・ライブラリ/SDF 関数/演算子/丸め
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 2%

---


# 丸め

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![丸めアイコン](./3d-sdf-op-rounding.png "丸め")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDFシェイプを拡張して膨張させ、ハードエッジを滑らかにします。

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
| <b>SDF</b> *浮動小数* | 入力されたSDFシェイプ。 |
| <b>半径</b> *浮動小数* | 図形のエッジに適用される丸みを帯びた円弧の半径です。<br><br><i>注： </i>丸みの半径が交差する部分にハードエッジが表示される場合があります。<br><br><i>既定： 0.05</i> |
