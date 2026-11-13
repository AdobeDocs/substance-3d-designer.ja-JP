---
title: ピラミッド
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ >ノードライブラリ> SDF 関数 >プリミティブ> ピラミッド
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
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
> SDF 関数に関する概念やワークフローについて詳しくは、専用ページ（[SDF 関数の操作](../../../../../../learning-tutorials/nodes/working-with-sdf-functions/working-with-sdf-functions.md)）を参照してください

## 入力

|  |  |
| :--- | :--- |
| <b>Height</b> *浮動小数* | ピラミッドの頂点の底からのZアップHeightです。<br><br><i>既定値： 1</i> |
| <b>基本サイズ</b> *浮動小数2* | XおよびYのピラミッドの底辺のサイズ。<br><br><i>既定値： (1, 1)</i> |
| <b>基本位置</b> *浮動小数3* | ピラミッドの底面のワールド空間位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数3* | ワールド空間の位置。 この入力を使用して、<b>Offset P</b>および<b>Rotate P</b>ノードを使用する他の変換を適用します。<br><br><i>既定：変換されていないワールド空間の位置。</i> |
