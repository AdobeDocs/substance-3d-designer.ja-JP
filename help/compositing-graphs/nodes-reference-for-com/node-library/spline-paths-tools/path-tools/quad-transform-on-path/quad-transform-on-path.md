---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/quad-transform-on-path.html"
breadcrumb-title: ''
description: '[パス上でクアッド変形]ノードを使用して、パスカーブに沿った要素に二次変換を適用します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Quad Transform on Path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パス上のクアッド変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 29dd2e6adc826f63ee26defc0032b0e52d4e30fb
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 2%

---


# パス上のクアッド変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](quad-transform-on-path.resources/quad-transform-on-paths-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

4つのハンドルを使用してパスを変形します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別の&#x200B;*パス*&#x200B;処理ノードに接続します。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | 変形パス。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>p00</b> <i>浮動小数2</i> | 左上ハンドルの位置を指定します。 |
| <b>p01</b> <i>浮動小数2</i> | 右上ハンドルの位置を指定します。 |
| <b>p02</b> <i>浮動小数2</i> | 左下のハンドルの位置。 |
| <b>p03</b> <i>浮動小数2</i> | 右下のハンドルの位置。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>前</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant1-After.jpg" alt="QuadTransformOnPaths-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="quad-transform-on-path.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>前</i>
    </td>
    <td>
      <img src="quad-transform-on-path.resources/QuadTransformOnPaths-Variant2-After.jpg" alt="QuadTransformOnPaths-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](quad-transform-on-path.resources/QuadTransformOnPaths-Demo2.gif "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](quad-transform-on-path.resources/QuadTransformOnPaths-Demo1.gif "ノードの例2")

</td>
</tr>
</table>
