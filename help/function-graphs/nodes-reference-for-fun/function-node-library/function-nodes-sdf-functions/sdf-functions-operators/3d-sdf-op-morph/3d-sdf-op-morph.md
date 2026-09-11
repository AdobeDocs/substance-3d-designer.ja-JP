---
title: モーフ
description: Designer/Substance合成グラフ/ノード合成の参照Substance合成グラフ/Node library/SDF 関数/演算子/モーフ
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# モーフ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![モーフアイコン](./3d-sdf-op-morph.png "モーフ")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

基本SDF形状と対象SDF形状のリニア補間を調整可能な混合係数に基づいて返します。

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
| <b>基本SDF</b> *フロート* | 基本SDFシェイプ。 |
| <b>ターゲットSDF</b> *フロート* | 対象のSDFシェイプ。 |
| <b>ミックス要素</b> *フロート* | 入力シェイプのモーフィングに使用するミックス係数。0は基本シェイプ、1はターゲットシェイプです。 |
