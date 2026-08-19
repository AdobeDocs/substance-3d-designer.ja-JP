---
title: 角錐
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ>ノードライブラリ> SDF 関数 >プリミティブ>ピラミッドスクエア
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 1%

---


# 角錐

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![角錐アイコン](./3d-sdf-pyramid-square.png "角錐")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Heightとベースの位置を調整できる、正方形のベースを持つピラミッド用SDF 関数です。

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
| <b>Height</b> *フロート* | ピラミッドの頂点の底からのZアップHeightです。<br><br><i>既定値： 1</i> |
| <b>基本サイズ</b> *フロート* | 角錐の底面のエッジの長さ。<br>すべてのエッジが同じ長さです。<br><br><i>既定： 1</i> |
| <b>基本位置</b> *浮動小数点3* | ピラミッドの底面のワールドスペース位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
