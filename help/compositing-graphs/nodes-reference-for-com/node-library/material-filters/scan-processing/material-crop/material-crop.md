---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-crop.html"
breadcrumb-title: ''
description: マテリアルの切り抜きノードを使用すると、特定の関心領域を分離するために、スキャンしたマテリアルからテクスチャ領域を切り抜くことができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルの切り抜き
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# マテリアルの切り抜き

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-crop.resources/material-crop-01.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、[切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)のマルチチャンネル、完全なマテリアルバージョンです。 これにより、すべてのマテリアルチャンネルに対して切り抜き操作を並行して実行できます。

>[!NOTE]
>
> [詳細については、元の画像を参照してください](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)[。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用します。 |
| <b>入力サイズ</b> <i>0 - 8192</i> | 入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。 |
| <b>背景</b> <i>（カラー値） / （グレースケール値）</i> | 切り抜きによってカバーされない領域の背景の均一値。 |
| <b>変形</b> <i>（変換行列）</i> | 結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。 |
