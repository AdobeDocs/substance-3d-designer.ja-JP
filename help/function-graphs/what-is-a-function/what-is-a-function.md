---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/what-is-a-function.html"
breadcrumb-title: ''
description: Substance 3D Designerの機能と、それらの機能を使用して再利用可能なノードネットワークを作成する方法について説明します。
helpx_creative_field: ""
helpx_description: "Designer > Function graphs > What is a function "
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: '関数とは '
user-guide-description: ''
user-guide-title: ''
source-git-commit: baf36ab85717512cc9e52d67d00293eabb5ebcf6
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 0%

---


# 関数とは

Substance 3D Designerの関数を使用すると、プログラミング言語のロジックを使用して結果を生成できます。

しかし、Designerの関数は、コード行を使用するのではなく、同じノードのアプローチを維持します。 一見すると、関数グラフは通常のグラフに非常に似ています。

![](what-is-a-function.resources/image2015-12-17-18-19-37.png)

関数が検出される主なケースには、次の2つがあります。

* パラメータの結果を制御するには
* ピクセルプロセッサーを

## パラメーターの結果を制御する

Substance 3D Designerでは、任意のパラメーターを関数で制御できます。

![](what-is-a-function.resources/image2015-12-17-21-3-46.png)

したがって、グラフの各部間の規則や依存性を想像して、独自の結果を得ることができます。

例えば、ブレンドノードの不透明度をワープノードの強度の半分に設定することができます。

![](what-is-a-function.resources/warpblend.gif)

実際、気付かないうちに関数を作成してしまった可能性があります。

パラメーターを表示した場合は、関数と変数が自動的に作成されています。関数には、新しく作成された変数の値をキャッチするget floatノードが含まれています。

![](what-is-a-function.resources/expose.gif)
