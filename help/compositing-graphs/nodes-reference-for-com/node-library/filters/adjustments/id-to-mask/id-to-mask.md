---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/id-to-mask.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 2%

---


# グレースケールをマスクするID

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![グレースケールアイコンをマスクするID](id-to-mask.resources/id-to-mask-01.png "グレースケールアイコンをマスクするID"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

選択したピクセル値を持つピクセルが白になるID マップからマスクを作成します。

ID マップとは、全体の一部（シェイプなど）であるピクセルがすべて同じ一意のID値を保持している画像です。 この場合、値は整数です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>ID</b> <i>グレースケール</i>プライマリ | マスクを抽出する入力ID マップ。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 入力ID マップから抽出されたバイナリマスク。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>選択モード</b> *整数* | IDマップのピクセル値を選択する方法です。マスクでは白にする必要があります。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>ソロ：</b>単一ピクセル値を選択</li> <li data-preserve-html="true"><b>範囲：</b>ピクセル値の範囲を選択します</li> </ul> |
| <b>ID 整数</b> *整数* *[選択モード]が[ソロ]に設定されている場合に使用できます* | 出力マスクで白にする必要があるIDマップ内のピクセル値。 |
| <b>ID範囲</b> *整数2* *&#39;選択範囲モード&#39;が&#39;範囲&#39;に設定されている場合に使用可能* | ID マップ内のピクセル値の範囲です。最初から最後までで、出力マスクでは白になります。 |

## 例

<table>
  <tr>
    <td>
      <img src="id-to-mask.resources/id-to-mask-02.jpg" alt="id_to_mask_grayscale_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="id-to-mask.resources/id-to-mask-03.jpg" alt="id_to_mask_grayscale_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![マスクするID：例2](id-to-mask.resources/id-to-mask-04.gif "マスクするID：例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![マスクするID：例3](id-to-mask.resources/id-to-mask-05.png "マスクするID：例3"){zoomable="yes"}

</td>
</tr>
</table>
