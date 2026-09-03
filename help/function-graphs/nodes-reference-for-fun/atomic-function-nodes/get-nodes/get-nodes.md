---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/get-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer関数グラフの「取得」ノードにアクセスして、変数値とデータを取得します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 変数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '477'
ht-degree: 6%

---


# 変数

変数は、後で取得(<b>Get</b>)または変更(<b>Set</b>)するために<b>値</b>を保存する方法です。

![Substance関数グラフ – 浮動小数点の取得](get-nodes.resources/get-nodes-01.gif "Substance関数グラフ – 浮動小数点の取得"){zoomable="yes"}

Getノードの基本的な機能は、ダイナミック変数をグラブし、それをGet Nodesの出力から返して関数で使用することです。 これらのGetノードは、[入力パラメーターパラメーター](../../../../compositing-graphs/graph-parameters/graph-parameters.md)と[グラフー関数](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)で定義されたパラメーター間のリンクを形成します。

Getノードを使用するたびに、ドロップダウンメニューから使用可能な値を選択する必要があります。 Get nodesは<b>対応する型の値</b>を取得します。 つまり、Getノードのメニューには有効なオプションのみが表示され、無効なオプションを選択することはできません。 変数を使用できない場合は、型の不一致が発生しています

<b>「システム」変数</b>が多数あります：自分自身を宣言できない定義済みの特殊変数です。 これらは非常に重要であり、その下のノードでは、使用可能なシステム変数がリストされています。

パラメーターが[表示](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)の場合、正しい型のGetノードのみを含むパラメーター関数をパラメーターに適用することになります。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## Get

</td>
<td style="border: 0;" valign="top">

### 設定

</td>
<td style="border: 0;" valign="top">

### 定義済み

</td>
</tr>
</table>

## Get

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![Get float2 – アイコン](get-nodes.resources/get-nodes-02.png "Get float2 – アイコン"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

これらのノードでは、現在のスコープ&#x200B;*に*&#x200B;存在する変数の値を取得できます。

取得される変数の名前は、プロパティドックで設定します。

</td>
</tr>
</table>

注意が必要な制限事項を「取得」ノードで確認してください。

* <b>型が</b>であるため、変数がノードと同じ型の値を保持していることを確認する必要があります。 型の不一致がコンソールで報告されます。
* <b>現在のスコープに変数</b>が存在するかどうかは確認されません。 見つからない変数は、コンソールに報告されます。
* シーケンスなどの制御フローノードを使用する複雑な関数では、<b>変数の設定および取得の順序</b>に注意してください。 Designerが「Get before Set」のケースを検出すると、コンソールに報告されます。

>[!NOTE]
>
> ビルトイン変数
> 
> いくつかの&#39;Get&#39;ノードは、現在のコンテキストに応じて既存の値にアクセスするための組み込み変数を提供します。例えば、ピクセルプロセッサ内の現在のピクセル位置、ノードの現在のタイリングモードなどです。
> 
> すべての組み込み変数は、[この専用ページ](../../../../function-graphs/variables/system-variables/system-variables.md)に一覧表示されます。

### ノードの取得

+++フロート
![フロートの取得 – アイコン](get-nodes.resources/get-nodes-03.png "フロートの取得 – アイコン"){width="200px"}



浮動小数を取得

![Get float2 – アイコン](get-nodes.resources/get-nodes-02.png "Get float2 – アイコン"){width="200px"}



浮動小数 2 を取得

![Get float3 – アイコン](get-nodes.resources/get-nodes-04.png "Get float3 – アイコン"){width="200px"}



浮動小数 3 を取得

![Get float4 – アイコン](get-nodes.resources/get-nodes-05.png "Get float4 – アイコン"){width="200px"}



浮動小数 4 を取得

+++

+++整数
![Get integer – アイコン](get-nodes.resources/get-nodes-06.png "Get integer – アイコン"){width="200px"}



整数を取得

![Get integer2 – アイコン](get-nodes.resources/get-nodes-07.png "Get integer2 – アイコン"){width="200px"}



整数 2 を取得

![Get integer3 – アイコン](get-nodes.resources/get-nodes-08.png "Get integer3 – アイコン"){width="200px"}



整数 3 を取得

![Get integer4 – アイコン](get-nodes.resources/get-nodes-09.png "Get integer4 – アイコン"){width="200px"}



整数 4 を取得

+++

+++その他
![ブール値を取得 – アイコン](get-nodes.resources/get-nodes-10.png "ブール値を取得 – アイコン"){width="200px"}



ブーリアンを取得

![文字列の取得 – アイコン](get-nodes.resources/get-nodes-11.png "文字列の取得 – アイコン"){width="200px"}



文字列を取得

+++

## 設定

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![設定：ノードアイコン](get-nodes.resources/get-nodes-12.png "設定：ノードアイコン"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

テキスト

</td>
</tr>
</table>

## 定義済み

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![定義：ノードアイコン](get-nodes.resources/get-nodes-13.png "定義：ノードアイコン"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

テキスト

</td>
</tr>
</table>
