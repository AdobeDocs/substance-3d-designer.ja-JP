---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-select.html"
breadcrumb-title: ''
description: パス選択ノードを使用して、条件に基づいてパスリストから特定のパスを選択し、フィルタリングします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パスの選択
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---


# パスの選択

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](paths-select.resources/paths-select-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

パスに含まれる複数のパスから1つのパスを分離します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>ラベル</b> <i>型</i> | エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | パスは1つのパスでのみ入力されます。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>選択モード</b> <i>整数</i> | パスの選択に使用されたメソッド： <br>*- ID別：* <b>パスID</b>で指定されたインデックスと一致するパスを一覧から選択します。<br>*– 長さ別：*&#x200B;長さが<b>ターゲットの長さ</b>で指定されたしきい値を上回るか、下回るパスを選択します。 |
| <b>パスID</b> <i>Integer</i> （<b>選択モード</b>が&#x200B;*ID別*&#x200B;に設定されている場合に使用可能） | 選択したパスのインデックスです。<br><b>パス&#x200B;*のパス数を超える値を指定すると、空白の出力が*</b>&#x200B;になります。 |
| <b>長さ以下？</b> <i>ブール値</i> （<b>選択モード</b>が&#x200B;*長さ指定*&#x200B;に設定されている場合に使用可能） | 選択範囲に<b>ターゲットの長さ</b>を含めるか、含めるのかを制御します。 |
| <b>ターゲットの長さ</b> <i>浮動小数</i> （<b>Selection Mode</b>が&#x200B;*By Length*&#x200B;に設定されている場合に使用可能） | スプラインの選択に使用する長さのしきい値。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/paths-select-02.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="paths-select.resources/paths-select-03.jpg" alt="PathsSelect-Variant1">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-select.resources/paths-select-02.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="paths-select.resources/paths-select-04.jpg" alt="PathsSelect-Variant2">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
