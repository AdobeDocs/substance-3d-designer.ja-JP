---
title: '減算スムーズ '
description: 'Designer/Substance合成グラフ/ノード参照Substance合成グラフ/ノードライブラリ/SDF 関数/演算子/減算スムーズ '
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 1%

---


# 減算スムーズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![減算スムーズアイコン](./3d-sdf-op-subtraction-smooth.png "減算スムーズ")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDF 2の交差に適用される調整可能なスムージングを使用して、SDF 1の形状の体積をSDF 2の形状から差し引きます。

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
| <b>SDF 1</b> *フロート* | から差し引かれるSDFシェイプ。 |
| <b>SDF 2</b> *フロート* | SDF 1形状から差し引かれるSDF形状。 |
| <b>Smoothness</b> *フロート* | 2つの図形の交差に適用されたスムージングです。<br><br><i>注： </i>滑らかさの半径が交差する部分に、はっきりしたエッジが表示される場合があります。 |
