---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/curvature-smooth.html"
breadcrumb-title: ''
description: Curvature Smoothノードを使用して、サーフェスの詳細を抽出するためにHeightマップからスムーズな曲率マップを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Curvature Smooth
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 曲線スムーズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 1%

---


# 曲線スムーズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![曲線スムーズノードアイコン](../../../../../../assets/CurvatureSmooth.png "曲線スムーズノードアイコン"){width="200px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

法線マップによって記述されるサーフェスの曲率を計算します。

曲率マップは、サーフェスの凹領域と凸領域を表します。\
平坦な領域は50%グレーになります。 凸状の領域はより明るく、凹状の領域はより暗くなります。

</td>
</tr>
</table>

また、凹領域と凸領域はそれぞれの出力に分割されるため、これらの特性に基づいて領域を簡単に選択したりマスクしたりできます。

>[!TIP]
>
> よりシャープなバージョンには[曲率](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-filter-node/curvature-filter-node.md)を、その他のオプションが必要な場合には[曲率ソベル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-sobel/curvature-sobel.md)を参照してください。

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
| <b>標準</b> *色* <b>プライマリ</b> | 曲率を計算するサーフェスを記述する法線マップ。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>曲線</b> *グレースケール* | 入力法線マップから計算された曲率マップ。   平坦な領域は50%グレーになります。 凸状の領域はより明るく、凹状の領域はより暗くなります。 |
| <b>凸面</b> *グレースケール* | 入力法線マップから計算された凸状マップ。   領域が凸状であるほど、マップ内の領域は明るくなります。  平坦な領域または凹状の領域は黒になります。 |
| <b>凹部</b> *グレースケール* | 入力法線マップから計算された凹部マップ。   領域が凹面であるほど、マップ内の領域は明るくなります。  平坦または凸状の領域は黒になります。 |

## パラメーター

|  |  |
| --- | --- |
| <b>標準の形式</b> *整数* | 入力法線マップの形式。 グリーンチャンネルを効果的に反転します。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Y軸は上を指しています</li> <li data-preserve-html="true"><b style="">OpenGL:</b> Y軸が下向き</li> </ul> |

## 例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_before.jpg" alt="curvature_smooth_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_1_after.jpg" alt="curvature_smooth_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![曲率スムーズ：例2](../../../../../../assets/curvature_smooth_example_2.jpg "曲率スムーズ：例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![曲率スムーズ：例3](../../../../../../assets/curvature_smooth_example_3.jpg "曲率スムーズ：例3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_before.jpg" alt="curvature_smooth_example_4_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/curvature_smooth_example_4_after.jpg" alt="curvature_smooth_example_4_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![曲率スムーズ：例4](../../../../../../assets/curvature_smooth_example_5.jpg "曲率スムーズ：例4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![曲率スムーズ：例5](../../../../../../assets/curvature_smooth_example_6.jpg "曲率スムーズ：例5"){zoomable="yes"}

</td>
</tr>
</table>
