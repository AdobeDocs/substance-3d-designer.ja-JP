---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-render.html"
breadcrumb-title: ''
description: ヒストグラムレンダリングノードを使用すると、ヒストグラムデータを分析やデバッグ用のテクスチャとして視覚化できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラムレンダリング
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '220'
ht-degree: 1%

---


# ヒストグラムレンダリング

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![異方性桑原グレースケールアイコン](../../../../../../assets/histogram_render.png "異方性桑原グレースケールアイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

グレースケール画像のヒストグラムを描画します。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
</tr>
</table>

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール*&#x200B;プライマリ | ヒストグラムを描画する画像。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | ヒストグラム可視化は、入力画像から計算されました。 |

## パラメーター

|  |  |
| --- | --- |
| <b>ヒストグラムの解像度</b> *整数* | ヒストグラムの幅。 値を大きくすると、より細かい値の分布が可能になります。   使用可能な解像度は、ピクセル単位で256、512、1024、2048、4096です |
| <b>自動スケール</b> *ブール値* | 「True」の場合、ヒストグラムを再マップして、画像のフルHeightを使用します。   &#39;False&#39;の場合、入力画像の値の出現数に応じて、各列でHeightのピクセルが使用されます。 |
| <b>スケール</b> *フロート* | ヒストグラムを縦方向に拡大縮小します。値1はヒストグラムのHeightの最大値です。 |
| <b>サンプリング</b> *整数* | ヒストグラム画像をフィルタリングする方法です。ヒストグラムの解像度とレンダリングの解像度が一致しない場合に、結果に影響します。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>バイリニア：</b>では、ヒストグラムにバイリニアフィルタリングを適用し、補間されたポイントを作成します</li> <li data-preserve-html="true"><b>最も近い：</b>で最も近いピクセルがサンプリングされ、フィルター処理は行われないため、手順はフラットになります</li> </ul> |
| <b>Y軸を反転</b> *ブール値* | 「True」の場合、ヒストグラムを垂直方向にミラーリングします。 |

## 例

![ヒストグラムのレンダリング：例1](../../../../../../assets/histogram_render_example_1.png "ヒストグラムのレンダリング：例1"){zoomable="yes"}

![ヒストグラムのレンダリング：例2](../../../../../../assets/histogram_render_example_2.png "ヒストグラムのレンダリング：例2"){zoomable="yes"}
