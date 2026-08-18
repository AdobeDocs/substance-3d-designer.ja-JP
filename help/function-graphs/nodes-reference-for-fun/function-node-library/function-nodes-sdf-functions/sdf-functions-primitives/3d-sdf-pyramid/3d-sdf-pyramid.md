---
title: ピラミッド
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ>ノードライブラリ> SDF 関数 >プリミティブ>ピラミッド
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '129'
ht-degree: 3%

---


# ピラミッド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ピラミッドアイコン](./3d-sdf-pyramid.png "ピラミッド")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Height、ベースサイズ、およびベースポジションを調整可能なピラミッド用のSDF 関数を提供する。

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
| <b>基本サイズ</b> *浮動小数点2* | XおよびYのピラミッドの底辺のサイズ。<br><br><i>既定値： (1, 1)</i> |
| <b>基本位置</b> *浮動小数点3* | ピラミッドの底面のワールドスペース位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
