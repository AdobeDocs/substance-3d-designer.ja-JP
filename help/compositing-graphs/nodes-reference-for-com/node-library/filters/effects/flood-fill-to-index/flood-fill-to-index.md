---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-index.html"
breadcrumb-title: ''
description: Flood Fillからインデックスへのノードを使用して、番号パターンやラベル付きパターンを作成するために、リージョンをインデックス値で塗りつぶします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Index
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 索引へのFlood Fill
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 2%

---


# 索引へのFlood Fill

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-index.png){width="200px"}

## 索引へのFlood Fill

**場所：** *フィルター/効果*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

「Flood Fillをインデックスに変換」を選択すると、すべてのFlood Fillセルが、左上隅の0から始まるインデックス番号に従って値に変換されます。 グレースケール濃淡を正規化された形式（0.0 ～ 1.0、Flood Fillで得られた数のセルで割った形式）またはHDRのクランプされていない値（0 ～ nでnはセルの数）で返すために使用できます。

さらに、インデックスへのFlood Fillでは[値](../../../../../values-compositing-graphs/values-in-substance-compositing-graphs.md)が使用され、見つかった図形の量と、オプションの内部データテーブルが返されます。

### 入力

* **Flood Fillボックス**: *色入力*&#x200B;標準Flood Fill入力マップ。 必須。
* **特殊形状情報**: *色入力*&#x200B;追加のFlood Fillマップは、前のFlood Fillノードで明示的に有効にする必要があり、接続する必要があります！

### パラメーター

* **出力**: *正規化された整数*&#x200B;出力がLDR 0-1またはHDR 0-nの範囲にあるかどうかを確認します。
* **次より小さい図形を無視**: *0.0 ～ 1.0*&#x200B;小さい図形を無視するための許容値。
* **Flood Fillデータテーブルの表示**: *False/True*&#x200B;詳細な使用のために追加の（デバッグ）データを返します。

## 例

![](../../../../../../assets/flood-fill-ex02.jpg)

</td>
</tr>
</table>
