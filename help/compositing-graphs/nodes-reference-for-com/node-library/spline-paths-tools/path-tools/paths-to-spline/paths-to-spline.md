---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
breadcrumb-title: ''
description: '[スプラインへのパス]ノードを使用して、パスデータをスプラインに変換し、スプラインベースのノードで使用します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths to Spline
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインへのパス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 1%

---


# スプラインへのパス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](paths-to-spline.resources/paths-to-spline-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[スプラインレンダリング](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-render/spline-render.md)ノードを使用して視覚化でき、[スプラインノード](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-tools.md)を使用して処理できるスプラインにパスを変換します。

</td>
</tr>
</table>

>[!NOTE]
>
> スプラインは曲線であるため、パスのシャープさを維持することはできません。 パスをスプラインに変換する場合は、シェイプの滑らかさが期待できます。

>[!TIP]
>
> このノードは、[Mask to Paths](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)ノードの後で、マスクをスプラインに変換するチェーンを形成するために使用できます。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> *記号：スプラインが閉じている（負）か開いている（正）;<br> *絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | <b>color</b>画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ：<br><b>R</b> - 正接 X<br><b>G</b> - 正接 Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スプラインの精度</b> <i>整数</i> | Paths入力の各パスでサンプリングされた頂点数の2を底とする対数(log2)で、対応するスプラインを構築します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-02.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-03.jpg" alt="PathsToSpline-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-04.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="paths-to-spline.resources/paths-to-spline-05.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
