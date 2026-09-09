---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-scan.html"
breadcrumb-title: ''
description: 「ヒストグラムスキャン」ノードは、カラー補正や色調補正のためにテクスチャのヒストグラムをスキャンして分析する場合に使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram Scan
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラムスキャン
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 7%

---


# ヒストグラムスキャン

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](histogram-scan.resources/histogram-scan-1.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力グレースケールイメージのコントラストと明るさを直感的に再マップできる、非常にシンプルで便利なノードです。 ダイナミックな方法でマスクを「拡大」および「縮小」するために使用できます。

[Substanceアカデミーのヒストグラム処理に関するビデオを見るには、ここをクリックしてください。](https://www.youtube.com/watch?v=p9wcmJBFyGA&t=427s)

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>位置</b> <i>0.0 - 1.0</i> | 明るさコントロールと同様に、結果の中間点を移動します。 グラデーションの入力で使用する場合、これによりトランジションポイントが拡大または縮小されます。<br><br>重要：既定値の0は、最終的な結果が常に黒であることを意味します。0.5から始めてみてください。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 トランジションの硬さを設定するために使用できます。 |
| <b>位置を反転</b> <i>False/True</i> | 最終結果を反転します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan2.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="histogram-scan.resources/histogram-scan3.gif" />
        </td>
    </tr>
</table>
