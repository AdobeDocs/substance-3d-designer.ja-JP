---
title: 交差のスムーズ
description: Designer/Substance合成グラフ/ノードの参照Substance合成グラフ/ノードライブラリ/SDF 関数/演算子/交点の滑らかさ
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 1%

---


# 交差のスムーズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![交差点のスムーズアイコン](./3d-sdf-op-intersection-smooth.png "交差点のスムーズ")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2つのSDF図形に共通の体積を返します。2つの図形が重なり合う場所に作成される体積であり、交差のエッジのスムージングを調整することができます。

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
| <b>Smoothness</b> *フロート* | 2つのSDF形状の交点のエッジのSmoothness。<br><br><i>注：</i>滑らかさの半径が交差する部分にハードエッジが表示されることがあります。<br><br><i>既定： 0</i> |
