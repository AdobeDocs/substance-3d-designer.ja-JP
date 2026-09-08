---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/threshold.html"
breadcrumb-title: ''
description: 「しきい値」ノードを使用して、マスクを作成するためのしきい値に基づいてグレースケールテクスチャを白黒に変換します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Threshold
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: しきい値
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 4%

---


# しきい値

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/threshold-2.png){width="200px"}

## しきい値

**イン：** *フィルター/調整*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

**Mode**&#x200B;パラメーターで設定された&#x200B;*比較条件*&#x200B;が、入力ピクセル値に対して&#x200B;**Threshold**&#x200B;値と相対的に満たされた場合、白を返します。\
[ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)と似ていますが、コントラストは常に最大レベルです。 ヒストグラムスキャンと同様の結果をより正確かつ迅速に取得する方法として役立ちます。

### パラメーター

* **しきい値**: *0.0 ～ 1.0*\
  入力ピクセル値を比較する輝度値。
* **モード**:\
  入力ピクセル値を&#x200B;**しきい値**&#x200B;値と比較する基準：
  * *より大きい*
  * *以上*
  * *下*
  * *以下*

## サンプル画像

</td>
</tr>
</table>
