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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 1%

---


# マテリアルの切り抜き

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-material.png){width="128px"}

## マテリアルの切り抜き

**イン：** *マテリアルフィルター/スキャン処理*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、[切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)のマルチチャンネル、完全なマテリアルバージョンです。 これにより、すべてのマテリアルチャンネルに対して切り抜き操作を並行して実行できます。

>[!NOTE]
>
> [詳細については、元の画像を参照してください](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md) [。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)

## パラメーター

### パラメーター

* **チャネル**
  * この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用します。
* **入力サイズ**: *0 - 8192*&#x200B;入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。
* **背景**: *（カラー値） / （グレースケール値）*切り抜きによってカバーされない領域の背景の均一値。
* **変換**: *（変換行列）*\
  結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。
* **オフセット**: *0.0 - 1.0*\
  結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
