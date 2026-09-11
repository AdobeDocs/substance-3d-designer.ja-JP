---
title: 反転
description: Designer/Substance合成グラフ/ノード合成の参照グラフ/Substanceライブラリ/SDF 関数/変形/反転
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '119'
ht-degree: 3%

---


# 反転

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![反転アイコン](./3d-sdf-transform-flip.png "反転")

<b>イン：</b> SDF 関数 >変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力されたSDFシェイプにミラー変形を適用します。<br>選択した軸に対して負のスケールを実行します。

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
| <b>ミラー軸</b> *Integer3* | 整数3を使用して、目的のミラー軸を設定します。<br>例： (1, 0, 0)はX軸をミラーリングします。<br><br><i>既定： (1, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | ワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
