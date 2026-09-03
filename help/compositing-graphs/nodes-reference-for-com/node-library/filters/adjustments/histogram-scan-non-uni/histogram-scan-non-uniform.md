---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan-non-uniform.html"
breadcrumb-title: ''
description: 「ヒストグラムスキャンの不均一」ノードを使用して、カラー補正を高度に行う場合の不均一なヒストグラムスキャンを実行します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan Non-Uniform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラムスキャンの不均一
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# ヒストグラムスキャンの不均一

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan-non-uniform.resources/histogram-scan-non-uniform-01.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)の高度なバージョンです。画像全体で均一にではなく、ピクセル単位のレベルで効果を制御するための追加のコントロールと入力を備えています。 マスクのコントラストとトランジションをさらに複雑にするために使用できます。

通常の[ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)よりも使用が複雑です。Non-Uniformバージョンを使用する前に、よく理解していることを確認してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール入力</i> | 変更するソース結果。 |
| <b>位置マップ</b> <i>グレースケール入力</i> | ドライブ位置パラメータへの入力スロット。 「位置入力を使用」がTrueに設定されている場合にアクティブになります。 有効な値の範囲は小さく、コントラストマップと設定に依存します。 |
| <b>コントラストマップ</b> <i>グレースケール入力</i> | コントラストパラメータを駆動する入力スロット。 「コントラスト入力を使用」がTrueに設定されている場合にアクティブになります。 有効値の範囲が小さいです。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>職位の入力を使用</b> <i>False/True</i> | 位置マップ入力スロットの使用を切り替えます。 |
| <b>位置</b> <i>0.0 - 1.0</i> | マップ結果をコントロールまたは変更して、位置設定を駆動します。 |
| <b>コントラスト入力を使用</b> <i>False/True</i> | コントラストマップ入力スロットの使用を切り替えます。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | コントラスト設定を駆動するために、マップ結果をコントロールまたは変更します。 |
