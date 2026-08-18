---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/properties.html"
breadcrumb-title: ''
description: Substance 3D Designerのプロパティパネルを使用して、ノードのプロパティとグラフパラメーターを表示および編集します。
helpx_creative_field: ""
helpx_description: Designer > Interface > Properties
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: プロパティ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 99e410384cec6569f613bb771db26585887704d8
workflow-type: tm+mt
source-wordcount: '444'
ht-degree: 0%

---


# プロパティ

Substance 3D Designerの<b>プロパティ</b>パネルとそのレイアウト、および各種ロールアウトとカテゴリとパラメーターについて説明します。 [Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)のプロパティにフォーカスしています。 [関数グラフ](../../function-graphs/function-graphs.md)と[FX-Mapグラフ](../../function-graphs/fxmaps/fxmaps.md)のレイアウトは単純です。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 概要

<b>プロパティ</b>パネルは、コンテキストに応じて変化するパネルで、[グラフビュー](../../interface/the-graph-view/the-graph-view.md)および[エクスプローラー](../the-explorer-window/the-explorer-window.md)ウィンドウでの選択に基づいて変化します。

</td>
<td style="border: 0;" valign="top">

![プロパティドック](../../assets/image2020-11-9-13-49-48.png "プロパティドック")

</td>
</tr>
</table>

選択したノードとリソースのプロパティを[グラフビュー](../../interface/the-graph-view/the-graph-view.md)と共に変更できます。Designerで2番目に頻繁に使用されるUIパネルである可能性があります。

[プロパティ]パネルは、選択内容に応じて、いくつかのロールアウトに分割されています。

* ノードの<b>基本パラメーター</b>と<b>入力 – </b>または<b>特定パラメーター</b>
* ほとんどのノードおよびパッケージの<b>属性</b>および<b>メタデータ</b>

Substanceエコシステムの主要な機能である[パラメーターの公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)は、プロパティパネルを使用して実行されます。

>[!NOTE]
>
> ほとんどの数値フィールドは、入力として&#x200B;*基本的な数式*&#x200B;をサポートしています（例： `17+3.5`、`7/3`、`(4+2)*3`）。 *Enter*&#x200B;を押して式を検証すると、結果がフィールドに入力されます。 数式が無効な場合、フィールドは以前の値に戻ります。\
> [パラメーターを公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)ダイアログなど、アプリケーションの他の部分の数値フィールドの中にも、この機能をサポートしているものがあります。

## ノードとSubstanceグラフ

[ノード](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/nodes-reference-129368078.html)と[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)には、プロパティカテゴリのセットがわずかに重複しており、その機能も同様です。

<b>基本パラメーター</b>と<b>属性</b>がノードとグラフで同じです。

ノードは、<b>特定のパラメーター</b>または<b>のインスタンスパラメーター</b>を提供します（[アトミックノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)または[インスタンス](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)であるかどうかによって異なります）。また、Substanceグラフの[値](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/values-in-substance-3d-graphs-180192235.html)を操作するための<b>入力値</b>も提供されます。

[Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)および[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)atomicノードは、可視性に<b>統合属性</b>および<b>条件</b>を備えているため、例外です。 これら2つのプロパティのセットは、「入力」および「出力」の「グラフのプロパティ」で一元的にアクセスすることもできます。

グラフにはいくつかの余分なカテゴリがあります。 <b>入力パラメーター</b>は、[公開パラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)、<b>入力</b>および<b>出力</b>は、入力ノードと出力ノードのすべてのプロパティを一覧表示します。 [専用のページで、詳細を説明したすべてのグラフプロパティを検索できます。](../../compositing-graphs/graph-parameters/graph-parameters.md)

## リソースとパッケージ

プロパティパネルは、[エクスプローラウィンドウ](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)の選択の変更にも応答します。 空の領域をダブルクリックする代わりに、グラフを選択する別の方法として使用できます。また、パッケージと[リソース](../../resources/resources.md)のプロパティを変更することもできます。

パッケージには、**Information**、**Attributes**&#x200B;および&#x200B;**Metadata**&#x200B;セクションがあります。 [パッケージメタデータは専用のページに記述されています。](../../package-metadata/package-metadata.md)

リソースには、リソースの種類に固有のプロパティがあります。[専用ページの詳細](../../resources/resources.md)。
