---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-equalize.html"
breadcrumb-title: ''
description: ヒストグラムのイコライザーノードを使用して、ピクセルの強度を再分散し、コントラストと明るさを向上させます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram equalize
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラムイコライザー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '189'
ht-degree: 2%

---


# ヒストグラムイコライザー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ヒストグラムのイコライズ：アイコン](../../../../../../assets/histogram_equalize.png "ヒストグラムのイコライズ：アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

グレースケールイメージのヒストグラムを平均化し、均一な分布を目指してグレースケール値を効率的に調整します。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 出力コネクター

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
</tr>
</table>

## 入力コネクター

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール*&#x200B;プライマリ | ヒストグラムを平均化する画像。 |

## 出力コネクター

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | ヒストグラムのイコライゼーションが適用された結果画像。 |

## パラメーター

|  |  |
| --- | --- |
| <b>ヒストグラムの解像度</b> *整数* | ヒストグラムの幅。 値を大きくすると、より細かい値の分布が可能になります。   使用可能な解像度は、ピクセル単位で256、512、1024、2048、4096です |
| <b>ヒストグラムのスムージング</b> *浮動小数* | ヒストグラムは、画像内のグレースケール値を再配分して、各値の間の&#x200B;*差*&#x200B;を均等にすることでスムージングできます。   このパラメーターは、スムージングの強度を調整します。 |

## 例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_1_before.jpg" alt="histogram_equalize_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_1_after.jpg" alt="histogram_equalize_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![ヒストグラムのイコライズ：例1](../../../../../../assets/histogram_equalize_example_3.png "ヒストグラムのイコライズ：例1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_2_before.jpg" alt="histogram_equalize_example_2_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_2_after.jpg" alt="histogram_equalize_example_2_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![ヒストグラムのイコライズ：例2](../../../../../../assets/histogram_equalize_example_5.png "ヒストグラムのイコライズ：例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_4_before.jpg" alt="histogram_equalize_example_4_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/histogram_equalize_example_4_after.jpg" alt="histogram_equalize_example_4_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![ヒストグラムのイコライズ：例3](../../../../../../assets/histogram_equalize_example_6.png "ヒストグラムのイコライズ：例3"){zoomable="yes"}
