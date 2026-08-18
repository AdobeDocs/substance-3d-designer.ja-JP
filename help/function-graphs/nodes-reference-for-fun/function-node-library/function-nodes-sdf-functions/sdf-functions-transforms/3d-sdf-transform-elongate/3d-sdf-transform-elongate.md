---
title: 細長い
description: Designer/Substance合成グラフ/ノードの参照用Substance合成グラフ/ノードライブラリ/SDF 関数/トランスフォーム/描画を延長
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 1%

---


# 細長い

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![アイコンを引き伸ばす](./3d-sdf-transform-elongate.png "引き伸ばす")

<b>イン：</b> SDF 関数 >トランスフォーム

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDFシェイプを調整可能な位置から引き伸ばします。<br>調整可能なスライスから始まるSDFシェイプのボリュームを効果的に線形に拡張します。

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
| <b>伸び</b> *浮動小数点3* | X、Y、Z軸の伸び長さ。 |
| <b>中央位置</b> *浮動小数点3* | 図形を引き延ばす元となるワールド空間の位置です。<br>つまり、スライスを引き延ばす位置です。 |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
