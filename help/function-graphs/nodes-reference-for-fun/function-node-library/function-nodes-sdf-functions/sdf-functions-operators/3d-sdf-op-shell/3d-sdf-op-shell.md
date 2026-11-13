---
title: シェル
description: Designer/Substance合成グラフ/ノード合成の参照グラフ/Substanceライブラリ/SDF 関数/演算子/シェル
source-git-commit: c3acf6cdb931126827d2a35dec1135800788ed81
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 4%
---

# シェル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![シェルアイコン](./3d-sdf-op-shell.png "シェル")

<b>イン：</b> SDF 関数 >演算子

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

作成されるエンベロープのThicknessを調整して、SDFシェイプを中空にします。

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
| <b>Thickness</b> *浮動小数* | シェルのThicknessは、内側と外側の両方に適用されます。<br>Thicknessを上げると、シェルが丸められます。<br><br><i>既定値： 0.02</i> |
