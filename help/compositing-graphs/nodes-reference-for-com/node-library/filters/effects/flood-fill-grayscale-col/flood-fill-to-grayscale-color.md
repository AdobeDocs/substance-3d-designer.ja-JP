---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-grayscale-color.html"
breadcrumb-title: ''
description: Flood Fillからグレースケールへのカラーノードを使用して、接続された領域をグレースケールで塗りつぶし、モノクロパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to GrayscaleColor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GrayscaleColorへのFlood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 4%

---


# Flood Fillからグレースケール/カラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-grayscale-color.resources/flood-fill-to-grayscale-color-01.png){width="128px"}

![](flood-fill-to-grayscale-color.resources/flood-fill-to-grayscale-color-02.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Flood Fillデータを使用して、グレースケールまたはカラー値のスウォッチを生成します。 [Flood Fillからランダムグレースケールへ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)とは異なり、これらの2つのノードでは、厳密なバリエーションやトーンをより細かく制御でき、セルごとにランダム化する基本値を決定する入力マップが追加されています。

これは、すべてのセルに独自の値や色を与えながら、制御を維持し、事前に決定された入力をベースとする強力なシステムです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>カラー入力</i> |  |
| <b>グレースケール/カラー入力</b> <i>グレースケール/カラー入力</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>輝度/色の調整</b> <i>-1.0 - 1.0</i> | ノードのバイアスまたはベース値を設定します。 グレースケールまたはカラー入力を使用する場合は、開始点としてその初期値を変更するために使用されます。 |
| <b>輝度/カラーランダム</b> <i>-1.0 - 1.0</i> | 変化の量を設定します。 |
