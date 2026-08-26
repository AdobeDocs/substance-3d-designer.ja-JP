---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-warp.html"
breadcrumb-title: ''
description: パスワープノードを使用して、パスカーブに沿ってテクスチャをワープし、カーブした有機的なパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パスワープ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# パスワープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/paths-warp-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>グラデーション入力</b>に従って入力パスを変形します。 （[ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)ノードと同じ効果）

</td>
</tr>
</table>

## 入力コネクタ

<b>パス</b> *色*\
エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。

<b>グラデーション入力</b> *グレースケール*\
ワープの量と向きの両方を制御するHeightのような入力。 （[ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)ノードと同じ効果）

## 出力コネクタ

<b>パス</b> *色*\
変形したパス。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。

## パラメーター

<b>適用度</b> *フロート*\
<b>強度</b>パラメーターは、ワープの強度を設定します。

<b>ステップ数</b> *整数*\
入力パスを複数の小さな増分でワープするには、大きい値を使用します。\
これにより、特に高い<b>強度</b>値を使用している場合、パスが交差するのを防ぐことができます。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/PathsToSpline-Variant2-Before.jpg" alt="PathsToSpline-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/PathsWarp-Variant1-After.jpg" alt="PathsWarp-Variant1-After">
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
      <img src="../../../../../../assets/PathsWarp-Variant2-After.jpg" alt="PathsWarp-Variant2-After">
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

![ノードの例1](../../../../../../assets/PathsWarp-Demo1.gif "ノードの例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
