---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
breadcrumb-title: ''
description: 「IDを使用してグレースケールをマスク」ノードを使用して、IDマップ値をマテリアル選択用のグレースケールマスクに変換します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > ID To Mask Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グレースケールをマスクするID
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
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

選択したピクセル値を持つピクセルが白になるIDマップからマスクを作成します。

IDマップは、全体（例えば、シェイプ）の一部であるピクセルがすべて同じ一意の識別値を保持する画像です。 この場合、値は整数です。

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
| <b>ID</b> *グレースケール*&#x200B;プライマリ | マスクの抽出元となる入力IDマップ。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | 入力IDマップから抽出されたバイナリマスク。 |

## パラメーター

|  |  |
| --- | --- |
| <b>選択モード</b> *整数* | IDマップのピクセル値を選択する方法です。マスクでは白にする必要があります。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>ソロ：</b>単一ピクセル値を選択</li> <li data-preserve-html="true"><b>範囲：</b>ピクセル値の範囲を選択します</li> </ul> |
| <b>ID整数</b> *整数* *[選択モード]が[ソロ]に設定されている場合に使用できます* | 出力マスクで白にする必要があるIDマップ内のピクセル値。 |
| <b>ID範囲</b> *Integer2* *&#39;選択モード&#39;が&#39;範囲&#39;に設定されている場合に使用できます* | IDマップのピクセル値の範囲（開始から終了まで）です。出力マスクでは白になります。 |

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
