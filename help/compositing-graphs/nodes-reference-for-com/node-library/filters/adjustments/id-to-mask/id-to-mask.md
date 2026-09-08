---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: 「IDを使用してグレースケールをマスク」ノードを使用して、マテリアルの値をID マップ選択範囲のグレースケールマスクに変換します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グレースケールをマスクするID
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 1%

---


# グレースケールをマスクするID

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![グレースケールアイコンをマスクするID](../../../../../../assets/IDToMask.png "グレースケールアイコンをマスクするID"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

選択したピクセル値を持つピクセルが白になるID マップからマスクを作成します。

ID マップとは、全体の一部（シェイプなど）であるピクセルがすべて同じ一意のID値を保持している画像です。 この場合、値は整数です。

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
| <b>ID</b> *グレースケール*&#x200B;プライマリ | マスクを抽出する入力ID マップ。 |

## 出力コネクター

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | 入力ID マップから抽出されたバイナリマスク。 |

## パラメーター

|  |  |
| --- | --- |
| <b>選択モード</b> *整数* | マスクで白にする必要があるID マップのピクセル値を選択する方式です。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>ソロ：</b>単一ピクセル値を選択</li> <li data-preserve-html="true"><b>範囲：</b>ピクセル値の範囲を選択します</li> </ul> |
| <b>ID 整数</b> *整数* *[選択モード]が[ソロ]に設定されている場合に利用可能* | 出力マスクで白にするID マップのピクセル値。 |
| <b>ID範囲</b> *整数2* *&#39;選択範囲モード&#39;が&#39;範囲&#39;に設定されている場合に使用可能* | ID マップ内のピクセル値の範囲です。最初から最後までで、出力マスクでは白になります。 |

## 例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_before.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/id_to_mask_grayscale_example_1_after.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![マスクするID：例2](../../../../../../assets/id_to_mask_example_2.gif "マスクするID：例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![マスクするID：例3](../../../../../../assets/id_to_mask_example_3.png "マスクするID：例3"){zoomable="yes"}

</td>
</tr>
</table>
