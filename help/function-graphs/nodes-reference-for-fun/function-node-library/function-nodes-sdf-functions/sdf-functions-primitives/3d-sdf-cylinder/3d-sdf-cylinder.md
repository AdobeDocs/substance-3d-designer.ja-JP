---
title: 円柱
description: Designer > Substance合成グラフ>ノードリファレンスSubstance合成グラフ> Node library > SDF 関数 >プリミティブ> Cylinder
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 2%

---


# 円柱

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![円柱アイコン](./3d-sdf-cylinder.png "円柱")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

調整可能なHeight、半径、およびエッジの丸みのシリンダ用のSDF 関数。

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
| <b>Height</b> *フロート* | 円柱の底からのZ-upHeight。<br><br><i>既定値： 1</i> |
| <b>半径</b> *フロート* | 円柱の半径。<br><br><i>既定： 0.5</i> |
| <b>丸め</b> *フロート* | 円柱のエッジに適用された丸みを帯びた円弧の半径です。<br><br><i>注： </i>丸みの半径が交差する部分にハードエッジが表示される場合があります。<br><br><i>既定： 0</i> |
| <b>ピボットの位置 （ローカル）</b> *浮動小数点3* | 円柱のローカル基点のワールドスペース位置です。(0, 0, 0)は、基点を円柱の中心に配置します。<br><br><i>既定値： (0, 0, -0.5)</i> |
| <b>中央位置</b> *浮動小数点3* | 円柱の基点のワールドスペース位置。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
