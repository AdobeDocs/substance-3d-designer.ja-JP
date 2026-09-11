---
title: 対称
description: Designer/Substance合成グラフ/ノード合成の参照グラフ/Substanceライブラリ/SDF 関数/演算子/対称
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# 対称

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![対称アイコン](./3d-sdf-op-symmetry.png "対称")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

対称面を横切るSDFシェイプをフリップして複製し、基本のSDFシェイプとその複製の和を返します。<br>対称は、すべての軸に同時に適用できます。

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
| <b>SDF</b> *フロート* | 入力されたSDFシェイプ。 |
| <b>ミラー面の位置</b> *浮動小数点3* | ミラー平面の中心のワールド空間位置。<br>対称が複数の軸に適用されている場合、この位置はすべてのミラー面で共有されます。<br><br><i>既定： (0, 0, 0)</i> |
| <b>ミラー軸</b> *Integer3* | 必要なミラー軸を設定します。<br><br>例： (1, 0, 0)は、X 軸に対称を適用します。<br><br><i>既定： (1, 0, 0)</i> |
| <b>軸を反転</b> *Integer3* | 反転する軸を設定します。<br><br>例： (1, 0, 0) X軸の対称方向を反転します。<br><br><i>既定： (0, 0, 0)</i> |
| <b>事前オフセット</b> *浮動小数点3* | 対称演算子を適用する前にシェイプに適用されるX、Y、Z軸上のオフセット。 |
