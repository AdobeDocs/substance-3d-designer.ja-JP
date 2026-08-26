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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%

---


# パスの選択

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/paths-select-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

パスに含まれる複数のパスから1つのパスを分離します。

</td>
</tr>
</table>

## 入力コネクタ

<b>ラベル</b> *型*\
エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。

## 出力コネクタ

<b>パス</b> *色*\
パスは1つのパスでのみ入力されます。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。

## パラメーター

<b>選択モード</b> *整数*&#x200B;パスの選択に使用するメソッド：\
*- ID別：* <b>パスID</b>で指定されたインデックスと一致するパスを一覧から選択します。\
*– 長さ：*&#x200B;長さが<b>ターゲットの長さ</b>で指定されたしきい値を上回るか下回るパスを選択します。

<b>パスID</b> *Integer* （<b>選択モード</b>が&#x200B;*ID別*&#x200B;に設定されている場合に使用可能）\
選択したパスのインデックス。\
<b>パス&#x200B;*のパス数を超える値を指定すると、空白の出力が*</b>&#x200B;になります。

<b>長さ以下？</b> *ブール値* （<b>選択モード</b>が&#x200B;*長さ指定*&#x200B;に設定されている場合に使用可能）\
選択範囲に<b>ターゲットの長さ</b>を含めるか、含めるのかを制御します。

<b>ターゲットの長さ</b> *浮動小数点* （<b>選択モード</b>が&#x200B;*長さ指定*&#x200B;に設定されている場合に使用可能）\
スプラインの選択に使用する長さのしきい値。

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
      <img src="../../../../../../assets/PathsSelect-Variant1.jpg" alt="PathsSelect-Variant1">
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
      <img src="../../../../../../assets/PathsSelect-Variant2.jpg" alt="PathsSelect-Variant2">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
