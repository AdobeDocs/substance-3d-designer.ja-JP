---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-uncombine.html"
breadcrumb-title: ''
description: 結合された法線マップデータを個々のX、Y、Zコンポーネントに分割するには、[法線の結合解除]ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal map > Normal uncombine
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 通常の結合解除
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 2%

---


# 通常の結合解除

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![通常の結合解除アイコン](normal-uncombine.resources/normal-uncombine-01.png "通常の結合解除アイコン"){width="200px"}

<b>イン：</b>フィルター>標準マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

法線マップから、Heightマップによって記述されたサーフェスの詳細を削除します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>標準の組み合わせ</b> <i>色</i>プライマリ | 詳細を削除する必要がある法線マップ。 |
| <b>Height</b> <i>グレースケール</i> | 結合された法線マップから削除する必要があるサーフェスの詳細を表すHeightマップ。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>結合されていない標準</b> <i>色</i> | 入力Heightマップによって記述されたサーフェスの詳細が削除された法線マップ。 |
| <b>推測強度</b> <i>フロート</i> | 入力法線マップの強さに合わせて、入力Heightマップに接続された[Normal](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)ノードに設定する必要がある強さの見積もり。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>標準の形式</b> *整数* | 入力法線マップの形式。 グリーンチャンネルを効果的に反転します。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>DirectX:</b> Y軸は上を指しています</li> <li data-preserve-html="true"><b>OpenGL:</b> Y軸が下向き</li> </ul> |

## 例

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-02.jpg" alt="normal_uncombine_example_3_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-03.jpg" alt="normal_uncombine_example_3_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![通常の結合解除：例2](normal-uncombine.resources/normal-uncombine-04.png "通常の結合解除：例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-05.jpg" alt="normal_uncombine_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-06.jpg" alt="normal_uncombine_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![通常の結合解除：例4](normal-uncombine.resources/normal-uncombine-07.png "通常の結合解除：例4"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-08.jpg" alt="normal_uncombine_example_2_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="normal-uncombine.resources/normal-uncombine-09.jpg" alt="normal_uncombine_example_2_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

![通常の結合解除：例6](normal-uncombine.resources/normal-uncombine-10.png "通常の結合解除：例6"){zoomable="yes"}
