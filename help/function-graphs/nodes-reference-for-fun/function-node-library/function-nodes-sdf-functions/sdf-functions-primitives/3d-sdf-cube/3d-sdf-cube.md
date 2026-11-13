---
title: 立方体
description: Designer > Substance合成グラフ >ノードリファレンスのSubstance合成グラフ >ノードライブラリ> SDF 関数 >プリミティブ>キューブ
source-git-commit: 3f5ca55e459e04f5b81755565c6f674dbc3c845c
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 2%
---

# 立方体

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![キューブアイコン](./3d-sdf-cube.png "キューブ")

<b>イン：</b> SDF 関数 >プリミティブ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

XYZサイズを調整したり、エッジを丸めたりできる立方体のSDF 関数です。

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
| <b>サイズ</b> *浮動小数3* | X、Y、およびZ上のキューブのサイズ。<br><br><i>既定： (1, 1, 1)</i> |
| <b>丸め</b> *浮動小数* | キューブのエッジに適用される丸みを帯びた円弧の半径です。<br><br><i>注： </i>丸みの半径が交差する部分にハードエッジが表示される場合があります。<br><br><i>既定： 0</i> |
| <b>ピボットの位置 （ローカル）</b> *浮動小数3* | キューブのローカルピボットのワールド空間位置です。(0, 0, 0)は、ピボットをキューブの中心に配置します。<br><br><i>既定値： (0, 0, -0.5)</i> |
| <b>中央位置</b> *浮動小数3* | キューブの基点のワールド空間位置です。<br><br><i>既定値： (0, 0, 0)</i> |
| <b>P</b> *浮動小数3* | ワールド空間の位置。 この入力を使用して、<b>Offset P</b>および<b>Rotate P</b>ノードを使用する他の変換を適用します。<br><br><i>既定：変換されていないワールド空間の位置。</i> |
