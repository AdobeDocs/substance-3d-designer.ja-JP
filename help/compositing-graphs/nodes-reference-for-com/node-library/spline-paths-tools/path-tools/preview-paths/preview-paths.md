---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/preview-paths.html"
breadcrumb-title: ''
description: 「パスのプレビュー」ノードを使用して、デバッグおよび検証用に2D ビュー内のパスデータを表示します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Preview Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パスをプレビュー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# パスをプレビュー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/preview-paths-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

指定した背景の上にあるパスのセグメントと頂点をトレースします。 パスごとに1つのランダムカラー。

パスへの[マスク](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)の<b>プレビュー</b>出力と同様の結果が得られますが、オプションが増えます。

</td>
</tr>
</table>

## 入力コネクタ

<b>背景</b> *色*\
上に表示された背景画像には、パスが表示されます。 これにより、レンダリングサイズも制御されます。

<b>パス</b> *色*\
エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。

## パラメーター

<b>コーナーを表示</b> *ブール値*\
各頂点にコーナーマークの付いた正方形を表示します（加算ブレンド）。

<b>頂点を表示</b> *ブール値*\
各頂点に円形を表示します（加算ブレンド）。 コーナーは引き続き正方形として表示されます。

<b>セグメントのThickness(px)</b> *フロート*\
レンダリングされたセグメントのThicknessをピクセル単位で調整します。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](../../../../../../assets/PathsToSpline-Variant2-Before_1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/PathsToSpline-Variant1-Before_1.jpg "ノードの例2")

</td>
</tr>
</table>
