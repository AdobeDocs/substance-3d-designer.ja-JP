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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 1%

---


# ヒストグラムスキャンの不均一

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-non-uniform.png){width="128px"}

## ヒストグラムスキャンの不均一

**イン：** *フィルター/調整*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

[ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)の高度なバージョンです。画像全体で均一にではなく、ピクセル単位のレベルで効果を制御するための追加のコントロールと入力を備えています。 マスクのコントラストとトランジションをさらに複雑にするために使用できます。

通常の[ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)よりも使用が複雑です。Non-Uniformバージョンを使用する前に、よく理解していることを確認してください。

## パラメーター

### 入力

* **入力**: *グレースケール入力*&#x200B;変更するソース結果。
* **位置マップ**: *グレースケール入力*&#x200B;位置パラメーターを駆動する入力スロット。 「位置入力を使用」がTrueに設定されている場合にアクティブになります。 有効な値の範囲は小さく、コントラストマップと設定に依存します。
* **コントラストマップ**: *グレースケール入力*&#x200B;コントラストパラメーターを駆動する入力スロット。 「コントラスト入力を使用」がTrueに設定されている場合にアクティブになります。 有効値の範囲が小さいです。

### パラメーター

* **位置入力を使用**: *False/True*&#x200B;位置マップ入力スロットの使用を切り替えます。
* **位置**: *0.0 ～ 1.0*&#x200B;位置設定を制御または変更するために、マップ結果を制御または変更します。
* **コントラスト入力を使用**: *False/True*&#x200B;コントラストマップ入力スロットの使用を切り替えます。
* **コントラスト**: *0.0 ～ 1.0*&#x200B;コントラスト設定を調整するために、マップ結果を制御または変更します。

## サンプル画像

</td>
</tr>
</table>
