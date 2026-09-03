---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/warnings-in-function-graphs.html"
breadcrumb-title: ''
description: Substance 3D Designer機能グラフの警告について理解し、よくある問題を解決する方法を学びます。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Warnings in function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 関数グラフの警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '450'
ht-degree: 0%

---


# 関数グラフの警告

このページには、Substance 3D Designerの[関数グラフ](../../function-graphs/function-graphs.md)によってトリガーされる可能性のある警告メッセージとエラーメッセージが一覧表示され、それぞれの一般的なトラブルシューティング手順が示されます。

警告は、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルのグラフリソースに対する警告アイコンのツールヒントと、グラフが読み込まれている場合は、[グラフビュー](../../interface/the-graph-view/the-graph-view.md)の左下隅に表示されます。\
関数が[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)のパラメーター&#x200B;*に適用されている*&#x200B;場合、警告が発生すると、そのパラメーターに関して「*[x]パラメーターの関数にエラーがあります*」が発生します。

## ![（エラー）](warnings-in-function-graphs.resources/error.svg)出力ノードが定義されていません

関数に出力ノードが定義されていません。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg)ソリューション**

この関数に予期される型と一致する値を出力するグラフ内のノードがある場合は選択し、RMBをクリックして、コンテキストメニューの&#x200B;**出力ノードとして設定**&#x200B;オプションを選択します。\
関数グラフの出力ノードは&#x200B;*オレンジ*&#x200B;色で表示されます。

>[!NOTE]
>
> 関数に必要な出力値の種類がある場合は、[グラフビュー](../../interface/the-graph-view/the-graph-view.md)の左下隅にメモが表示され、その種類を知ることができます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-01.gif)

</td>
</tr>
</table>

### ![（エラー）](warnings-in-function-graphs.resources/error.svg)現在の出力ノードは、型&#x200B;*x*&#x200B;の値を返します

関数の出力ノードは、その関数で期待される出力値の型と一致しない値を返します。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg)ソリューション**

この関数に対して期待される型と一致する値を出力するグラフ内のノードを選択し、[RMB]をクリックして、コンテキストメニューの&#x200B;**出力ノードとして設定**&#x200B;オプションを選択します。\
関数グラフの出力ノードは&#x200B;*オレンジ*&#x200B;色で表示されます。

>[!NOTE]
>
> 関数に必要な出力値の種類がある場合は、[グラフビュー](../../interface/the-graph-view/the-graph-view.md)の左下隅にメモが表示され、その種類を知ることができます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-02.gif)

</td>
</tr>
</table>

### ![（エラー）](warnings-in-function-graphs.resources/error.svg)一部のGetノードに変数名がありません

1つ以上の[Get](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)ノードの<b>Get...</b>プロパティが空白のままです。したがって、変数がないことを示しています。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg)ソリューション**

この警告を発生させているGetノードの&#x200B;**Get...**&#x200B;プロパティに、関数のスコープ&#x200B;*で使用可能な変数*&#x200B;の名前と一致する文字列を入力してください。

>[!NOTE]
>
> 入力文字列は&#x200B;*ノードに表示*&#x200B;されるため、空の値を持つノードを簡単に見つけることができます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-03.gif)

</td>
</tr>
</table>

### ![（エラー）](warnings-in-function-graphs.resources/error.svg)一部のSetノードに変数名がありません

1つ以上の[Set](../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md)ノードの&#x200B;**Set**&#x200B;プロパティが空白のままであるため、変数がないことを示しています。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

**![(tick)](warnings-in-function-graphs.resources/check.svg)ソリューション**

この警告を発生させたSetノードの&#x200B;**Set**&#x200B;プロパティに任意の文字列を入力してください。

>[!NOTE]
>
> 入力文字列は&#x200B;*ノードに表示*&#x200B;されるため、空の値を持つノードを簡単に見つけることができます。

>[!NOTE]
>
> 文字列が関数のスコープで使用可能な変数と&#x200B;*一致しない*&#x200B;場合、そのスコープ内に&#x200B;*新しい変数が作成*&#x200B;され、文字列の名前が付けられます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](warnings-in-function-graphs.resources/warnings-in-function-graphs-04.gif)

</td>
</tr>
</table>
