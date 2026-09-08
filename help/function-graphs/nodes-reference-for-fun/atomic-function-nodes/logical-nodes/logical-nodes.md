---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/logical-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer関数グラフの論理ノードにアクセスして、ブール論理演算と比較を行います。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Logical
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 論理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---


# 論理ノード

論理ノードは、グラフに複数の条件を追加するために使用されます。

![](../../../../assets/image2015-12-23-11-23-21.png)

## *および*&#x200B;ノード

![](../../../../assets/image2015-12-23-11-30-9.png)

Andノードは、次の2つのブーリアンノードを入力として受け取ります。

* 両方の入力がTrueの場合、*And*&#x200B;ノードの出力は&#x200B;*True*&#x200B;になります
* いずれの場合も、*And*&#x200B;ノードは&#x200B;*False*&#x200B;を返します

## *または*&#x200B;ノード

![](../../../../assets/image2015-12-23-11-30-44.png)

Orノードは、次の2つのブーリアンノードを入力として受け取ります。

* 少なくとも1つの入力がTrue (1)の場合、*または*&#x200B;ノードの出力は&#x200B;*True*&#x200B;になります
* 両方の入力がFalseの場合、*または*&#x200B;ノードは&#x200B;*False*&#x200B;を返します

## *Not*&#x200B;ノード

![](../../../../assets/image2015-12-23-11-31-46.png)

Notノードは、入力としてブーリアンを受け取ります。入力値を調べ、その逆を返します。

* *True*&#x200B;の入力で&#x200B;*False*&#x200B;の出力が得られます
* *False*&#x200B;の入力で&#x200B;*True*&#x200B;の出力が得られます
