---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: 変形ノードを使用して、回転、スケール、オフセットなどのマテリアル出力にトランスフォームを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '157'
ht-degree: 2%

---


# 変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-transform.resources/material-transforms.png){width="128px"}

<b>内：</b> マテリアルフィルター > 変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

マテリアル 変形は、単に[アトミック変形 2Dノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)の「マルチチャンネル」マテリアルバージョンです。 変形2Dと同じインターフェイスを使用して、入力マテリアルのすべてのチャンネルを同時に変形します。

チャンネルを正しく設定してください。 デフォルトでは、メタリック/ラフネスとSpecular/光沢度の両方が有効になっているため、混乱する可能性があります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>変換</b> <i>（変換行列）</i> | 結果を回転およびスケールします。 移動/パンはオフセットパラメーターを使用して実行されます |
| <b>オフセット</b> <i>-0.5 - 0.5</i> | 結果を移動または移動します。 変形コントロールがある場合、カンバスと直接相互作用することで結果を変更できます。 |
| <b>標準の形式</b> | DirectX形式とOpenGL形式（緑色に反転）から選択します。 |
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。例えば、メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合などです。 |
