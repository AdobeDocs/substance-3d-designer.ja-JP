---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: 結合された法線マップデータを個々のX、Y、Z構成部品に分離するには、「通常の結合解除」ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通常の結合解除
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# 通常の結合解除

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![通常の結合解除アイコン](normal-uncombine.resources/NormalUncombine.png "通常の結合解除アイコン"){width="200px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高さマップによって記述されたサーフェスの詳細を法線マップから削除します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>標準の組み合わせ</b> <i>色</i>プライマリ | 詳細を削除する法線マップです。 |
| <b>Height</b> <i>グレースケール</i> | 結合法線マップから除去するサーフェスの詳細を表す高さマップ。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>結合されていない標準</b> <i>色</i> | 入力高さマップによって記述されたサーフェスの詳細が削除された法線マップ。 |
| <b>推測強度</b> <i>浮動小数</i> | 入力法線マップの強さに合わせて、入力ノードに接続されている[Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md) 高さマップに設定する必要がある強さの見積もり。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>標準の形式</b> *整数* | 入力法線マップの書式です。 グリーンチャンネルを効果的に反転します。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Y軸が上を指しています</li> <li data-preserve-html="true"><b>OpenGL:</b> Y軸が下を指しています</li> </ul> |

## 例

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_before.jpg" alt="normal_uncombine_example_3_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_3_after.jpg" alt="normal_uncombine_example_3_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![通常の結合解除：例2](normal-uncombine.resources/normal_uncombine_example_4.png "通常の結合解除：例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_before.jpg" alt="normal_uncombine_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_1_after.jpg" alt="normal_uncombine_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![通常の結合解除：例4](normal-uncombine.resources/normal_uncombine_example_6.png "通常の結合解除：例4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_before.jpg" alt="normal_uncombine_example_2_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal_uncombine_example_2_after.jpg" alt="normal_uncombine_example_2_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![通常の結合解除：例6](normal-uncombine.resources/normal_uncombine_example_5.png "通常の結合解除：例6"){zoomable="yes"}
