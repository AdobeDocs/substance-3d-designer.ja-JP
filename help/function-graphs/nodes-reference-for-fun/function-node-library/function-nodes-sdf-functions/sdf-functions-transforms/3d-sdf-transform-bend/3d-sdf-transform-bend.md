---
title: 曲げ（不正確）
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ>ノードライブラリ> SDF 関数 >トランスフォーム>ベンド（不正確）
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 1%

---


# 曲げ（不正確）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![曲げ（不正確）アイコン](./3d-sdf-transform-bend.png "曲げ（不正確）")

<b>イン：</b> SDF 関数 >トランスフォーム

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDFシェイプを、ローカルY軸を中心に一定の角度で曲げます。<br><br><i>注：</i>この変換関数は厳密ではないため、レンダリング時に斑点が現れることがあります。

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
| <b>角度</b> *フロート* | 曲げの終点に適用される回転の角度。 |
| <b>開始</b> *フロート* | 曲げが始まるZ軸上のワールド位置です。 下のすべてのボリュームは曲げられません。 |
| <b>終了</b> *フロート* | 曲げが終了するZ軸上のワールド位置。 上のすべてのボリュームは、指定した角度で均等に回転されます。 |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
