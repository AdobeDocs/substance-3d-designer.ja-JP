---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/the-function-graph.html"
breadcrumb-title: ''
description: カスタム関数や再利用可能なノードネットワークを作成するためのDesignerのSubstance関数グラフについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs > The Substance function graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance関数グラフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---


# グラフとの類似点

一見すると、Substance機能グラフはSubstanceグラフに非常に似ており、ワークフローもほとんど同じです。

![Substance関数のグラフ](the-function-graph.resources/the-function-graph-01.png "Substance関数のグラフ")

## ナビゲーションは類似しています

Substance関数グラフでは、Substanceグラフの場合と同様にノードを作成および編成できます。

ノードには、次の方法でアクセスできます。

* ライブラリから
* スペースバーまたはTabキー
* 右クリックして[ノードを追加]メニューを使用する

### ワークフローは類似しています

グラフの場合と同様に、一連のノードをチェーン接続し、各ノードで前のノードで生成された結果を使用して関数を構築します。

出力は、パラメーターの値またはピクセルプロセッサーーノードの出力を定義します。

## グラフとの相違点

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### ノード

Substance関数グラフで使用可能なノードは、Substanceグラフで発生するノードとは完全に異なります。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![Substance関数グラフノード一覧](the-function-graph.resources/the-function-graph-02.png "Substance関数グラフノード一覧")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 出力

グラフとは異なり、関数には1つの出力しか含めることができません。

もう1つ注意すべき点は、最終的な結果を出力する特定のノードがないことです。 代わりに、期待する結果を生成するノードを出力として直接フラグ付けできます。

</td>
<td style="border: 0;" valign="top">

![Substance関数グラフの出力ノード](the-function-graph.resources/the-function-graph-03.png "Substance関数グラフの出力ノード")

</td>
</tr>
</table>

#### 出力ノードの定義方法

出力を定義するには、必要な出力を生成するノードを右クリックし、*出力として設定ノード：*&#x200B;をクリックします

![出力ノードを定義しています](the-function-graph.resources/the-function-graph-04.gif "出力ノードを定義しています")

>[!WARNING]
>
> <b>生成された結果の種類を再確認してください</b>
> 
> *出力ノードとして設定*&#x200B;が灰色表示されている場合は、ノードによって生成された値が、パラメーターまたはピクセルプロセッサによって予期された値と異なることを意味します。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Substanceグラフの場合は、別のグラフで作成した関数を読み込むことができます。 参照グラフを右クリックして「参照を開く」を選択すると、参照グラフを開くことができます。

</td>
<td style="border: 0;" valign="top">

![参照Substance関数グラフを開く](the-function-graph.resources/the-function-graph-05.png "参照Substance関数グラフを開く")

</td>
</tr>
</table>

複数の関数を含むsbsがある場合は、それをSubstanceの関数グラフに直接ドラッグ&amp;ドロップし、表示されるリストからインポートする関数を選択できます。

![パッケージからSubstance関数グラフを削除](the-function-graph.resources/the-function-graph-06.gif "パッケージからSubstance関数グラフを削除")
