---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library/function-nodes-random/hash-functions.html"
breadcrumb-title: ''
description: 関数グラフでハッシュ関数を使用すると、入力座標に基づいて確定的なランダム値を生成できます。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library > Random > Hash
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ハッシュ関数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 1%

---


# ハッシュ関数

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ハッシュノード：アイコン](hash-functions.resources/hash-functions-01.png "ハッシュノード：アイコン"){width="200px"}

<b>In:</b>関数>ランダム

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

シードとして使用される入力値に基づいて、0 ～ 1の間の擬似乱数値を計算します。

タイトルの数字は、入力する値のタイプと出力する値のタイプを示しています。 例：ハッシュ23はfloat2値を入力として取り、float3値を出力します。

</td>
</tr>
</table>

ハッシュノードが複数のコンポーネントの値を出力する場合、各コンポーネントは異なる擬似ランダム値を持ちます。

使用可能なバージョン（入力タイプと出力タイプ付き）:

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>ハッシュ11:</b> →浮動小数

<b>ハッシュ14:</b> →浮動小数4

<b>ハッシュ21:</b> 浮動小数2 → 浮動小数

<b>ハッシュ22:</b> 浮動小数2 → 浮動小数2

</td>
<td style="border: 0;" valign="top">

<b>ハッシュ24:</b> 浮動小数2 → 浮動小数4

<b>Hash31:</b> 浮動小数3 → 浮動小数

<b>ハッシュ32:</b> 浮動小数3 → 浮動小数2

</td>
</tr>
</table>

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> | 疑似ランダム出力を計算するためのシードとして使用される値。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ハッシュ14の例](hash-functions.resources/hash-functions-02.png "ハッシュ14の例"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ハッシュ32の例](hash-functions.resources/hash-functions-03.png "ハッシュ32の例"){zoomable="yes"}

</td>
</tr>
</table>
