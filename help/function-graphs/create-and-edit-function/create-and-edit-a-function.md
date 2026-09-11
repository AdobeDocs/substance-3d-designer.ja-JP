---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/create-and-edit-a-function.html"
breadcrumb-title: ''
description: Substance 3D Designerで機能グラフを作成および編集して、再利用可能なノードネットワークを構築する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Create and edit a function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 関数の作成と編集
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---


# 関数の作成と編集

## 関数の作成

関数を作成するには、関数アイコン![](create-and-edit-a-function.resources/image2017-3-7-17-10-8.png)をクリックし、[**空の関数**]を選択します。

![](create-and-edit-a-function.resources/image2017-3-7-17-8-37.png)

## 関数の編集

作成した関数は、関数アイコンをもう一度クリックするか、ドロップダウンリストで「編集」を選択して変更できます。

![](create-and-edit-a-function.resources/image2017-3-7-17-11-42.png)

次に、グラフの機能モードに入ります。

## 関数グラフ

関数グラフは、Designerの他のグラフの種類と同様に、ノードエディターで機能します。

## ノードを作成

ノードを作成するには、グラフを右クリックして「Add element」を選択するか、スペースバーを押します。

![](create-and-edit-a-function.resources/capture-d-e-cran-2015-02-04-10-05-16.png){width="600px"}

## 出力の設定

グラフとは異なり、関数には「出力」ノードがありません。グラフのどのノードを関数出力とするかを指定する必要があります。

ノードを右クリックし、<b>[出力ノードとして設定]を選択すると、出力を設定できます。</b>

出力として設定されたノードは黄色になります。

>[!NOTE]
>
> **出力の種類**
> 
> 出力として設定するノードは、そのノードが制御するパラメータと同じ値タイプを保持する必要があります。 そうでない場合、「出力ノードとして設定」オプションはグレー表示されます。

>[!WARNING]
>
> 関数が機能するには、出力が必要です。 関数に出力セットがない場合、グラフに警告が表示されます。
