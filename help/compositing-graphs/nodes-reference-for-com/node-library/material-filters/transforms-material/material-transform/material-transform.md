---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/transforms-material/material-transform.html"
breadcrumb-title: ''
description: マテリアルの変換ノードを使用して、回転、スケール、オフセットなどの変換をマテリアル出力に適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Transforms (Material) > Material Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルの変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '170'
ht-degree: 1%

---


# マテリアルの変換

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-transforms.png){width="128px"}

## マテリアルの変換

**場所：** *マテリアルフィルター/変換*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

Material Transformは、単に[Atomic Transformation 2Dノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)の「マルチチャンネル」マテリアルバージョンです。 [2D変換]と同じインタフェースを使用して、入力マテリアルのすべてのチャンネルを同時に変換します。

チャンネルを正しく設定してください。 デフォルトでは、「メタリック/粗さ」と「Specular/光沢」の両方が有効になっているため、混乱する可能性があります。

## パラメーター

* **変換**: *（変換行列）*\
  結果を回転およびスケールします。 移動/パンはオフセットパラメーターを使用して実行されます
* **オフセット**: *-0.5 - 0.5*\
  結果を移動または変換します。 変形コントロールがある場合、カンバスと直接相互作用することで結果を変更できます。
* **標準の形式**\
  DirectX形式とOpenGL形式（緑色に反転）から選択します。
* **チャネル**\
  この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
