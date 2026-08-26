---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-to-spline.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 1%

---


# スプラインへのパス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/paths-to-splines-icon.png "ノードアイコン")

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

## 入力コネクタ

<b>パス</b> *色*\
エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。

## 出力コネクタ

<b>スプライン座標&#x200B;</b>*色*&#x200B;入力スプラインの点の座標は、カラー画像のRGBAチャンネルでエンコードされます。\
<b>R</b> - X位置\
<b>G</b> - Y位置\
<b>B</b> -Height\
<b>A</b> – パックされたデータ：\
*記号：スプラインが閉じている（負）か、開いている（正）;\
*絶対値：Thickness + 1。

<b>スプラインデータ</b> *色*\
<b>color</b>画像のRGBAチャンネルにエンコードされた入力スプラインの追加データ：\
<b>R</b> – 接線X\
<b>G</b> – 接線Y\
<b>B</b> – 未使用\
<b>A</b> – 未使用

<b>スプラインの量</b> *整数*\
入力スプラインの数。

## パラメーター

<b>スプラインの精度</b> *整数*\
対応するスプラインを構築するために入力されたパスの各パスでサンプリングされた頂点の数の2を底とする対数(log2)。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-Before.jpg" alt="PathsToSpline-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant1-After.jpg" alt="PathsToSpline-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-After.jpg" alt="PathsToSpline-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
