---
title: オフセット
description: Designer/Substance合成グラフ/ノード合成の参照グラフ/Substanceライブラリ/SDF 関数/変形/オフセット
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '84'
ht-degree: 3%

---


# オフセット

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![オフセットアイコン](./3d-sdf-transform-offset.png "オフセット")

<b>イン：</b> SDF 関数 >変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベクトルに沿ってSDFシェイプをオフセットします。

</td>
</tr>
</table>

<a name='inputs'></a>

|  |  |
| :--- | :--- |
| <b>SDF</b> *フロート* | 入力されたSDFシェイプ。 |
| <b>オフセット</b> *浮動小数点3* | SDFシェイプがX、Y、Z方向にオフセットされる距離。<br><br><i>既定： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | ワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
