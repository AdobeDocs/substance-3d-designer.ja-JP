---
title: 拡大・縮小
description: Designer/Substance合成グラフ/ノードの参照Substance合成グラフ/ノードライブラリ/SDF 関数/トランスフォーム/スケール
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 3%

---


# スケール

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![スケールアイコン](./3d-sdf-transform-scale.png "スケール")

<b>イン：</b> SDF 関数 >トランスフォーム

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

SDFシェイプを均一に尺度変更します。

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
| <b>スケール</b> *フロート* | 均一スケール係数。<br><br><i>既定： 1</i> |
| <b>ピボットの位置</b> *浮動小数点3* | SDFシェイプのローカル基点のワールドスペース位置。(0, 0, 0)は、基点をSDFシェイプの中心に配置します。 <br>スケールの原点を定義します。<br><br><i>既定： (0, 0, 0)</i> |
| <b>P</b> *浮動小数点3* | 変換されたワールド空間の位置。 この入力を使用して、<b>オフセットP</b>および<b>回転P</b>ノードを使用する追加の変換を適用します。<br><br><i>既定：変換されていないワールドスペースの位置。</i> |
