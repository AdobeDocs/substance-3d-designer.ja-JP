---
title: ユニオン面取り
description: Designer/Substance合成グラフ/ノード合成の参照Substance合成グラフ/Node library/SDF 関数/演算子/結合面取り
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# ユニオン面取り

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ユニオン面取りアイコン](./3d-sdf-op-union-chamfer.png "ユニオン面取り")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2つのSDF図形の追加された体積を返します。この値には、交差のエッジに沿って調整できる半径の追加の体積が含まれます。

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
| <b>SDF 1</b> *フロート* | 最初のSDFシェイプ。 |
| <b>SDF 2</b> *フロート* | 2番目のSDFシェイプ。 |
| <b>半径</b> *フロート* | シェイプの交差のエッジに沿って追加されたボリュームの半径。<br><br><i>既定： 0</i> |
