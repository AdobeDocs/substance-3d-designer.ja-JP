---
title: 平面
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ> Node library > SDF 関数 >プリミティブ>プレーン
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 2%

---


# 平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![平面アイコン](./3d-sdf-plane.png "平面")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

方向、位置、サイズを調整できる平面のSDF 関数です。

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
| <b>標準</b> *浮動小数点3* | 平面の方向を制御する、平面のワールド空間法線ベクトル。<br>ベクトルが正規化されています。<br><br><i>既定値： (0, 0, 1)</i> |
| <b>サイズ</b> *浮動小数点2* | X方向とY方向の平面のサイズ。<br><br><i>既定： (1, 1)</i> |
| <b>Thickness</b> *フロート* | すべての方向に適用される平面のThickness。<br>Thicknessを上げると平面が丸められます。<br><br><i>既定値： 0</i> |
| <b>中央位置</b> *浮動小数点3* | 平面の基点のワールドスペース位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
