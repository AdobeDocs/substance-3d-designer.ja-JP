---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: ヒストグラムスキャンノードを使用して、テクスチャヒストグラムをスキャンし、カラー補正と調整のために分析します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラムスキャン
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '149'
ht-degree: 5%

---


# ヒストグラムスキャン

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/histogram-scan-1.png){width="128px"}

## ヒストグラムスキャン

**イン：** *フィルター/調整*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

入力グレースケール画像のコントラストと明るさを直感的に再マップできる、非常にシンプルでありながら便利なノードです。 ダイナミックな方法でマスクを「拡大」および「縮小」するために使用できます。

[Substanceアカデミーのヒストグラム処理に関するビデオを見るには、ここをクリックしてください。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

## パラメーター

* **位置**: *0.0 ～ 1.0*&#x200B;明るさコントロールと同様に、結果の中間点を移動します。 グラデーション入力で使用すると、トランジションポイントが拡大または縮小されます。\
  重要：デフォルト値の0は、最終結果が常に黒であることを意味します。0.5から始めてみてください。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。 トランジションの硬さの設定に使用できます。
* **位置を反転**: *False/True*&#x200B;最終結果を反転します。

## サンプル画像

![](../../../../../../assets/histogram-scan.gif)

![](../../../../../../assets/histogram-scan2.gif)

![](../../../../../../assets/histogram-scan3.gif)

</td>
</tr>
</table>
