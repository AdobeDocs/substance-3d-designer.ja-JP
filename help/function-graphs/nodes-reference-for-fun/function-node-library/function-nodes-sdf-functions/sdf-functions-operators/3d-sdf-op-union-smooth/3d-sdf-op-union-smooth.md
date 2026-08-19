---
title: ユニオンスムーズ
description: Designer/Substance合成グラフ/ノードの参照Substance合成グラフ/Node library/SDF 関数/演算子/和集合スムーズ
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '101'
ht-degree: 1%

---


# ユニオンスムーズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ユニオンスムーズアイコン](./3d-sdf-op-union-smooth.png "ユニオンスムーズ")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2つのSDF図形の追加された土量を返します。交差のエッジのスムージングを調整できます。

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
| <b>Smoothness</b> *フロート* | 交点のエッジから開始されるスムージング半径。<br><br><i>既定値： 0</i><br><br><i>注：</i>スムージング半径が交差する部分にハードなエッジが表示される場合があります。 |
