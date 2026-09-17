---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/getting-started/workflow-overview.html"
breadcrumb-title: ""
description: Substance 3D Designerでプロシージャルマテリアルを最初から最後まで作成するための基本的なワークフローについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Workflow overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ワークフローの概要
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '1169'
ht-degree: 0%
---

# ワークフローの概要

Substance 3D Designerはノードベースのエディターです。 つまり、ほぼすべての種類のプロジェクトまたはリソースで、ノードを配置（構成要素）し、それらを接続して一連の操作(グラフ)を作成する必要があります。このページでは、ノードベースのワークフローの概念について説明し、Designerで作成できる3つの主要な種類のグラフの概要を示します。

![簡略化されたデータフロー](workflow-overview.resources/graph-direction.png "簡略化されたデータフロー"){zoomable="yes"}

## ノードベースのワークフロー

Designerでの作業は、Photoshopなどの他の2D画像編集ソフトウェアでの作業とは異なります。 操作（メニューオプションに移動して彩度を調整したり、スライダーを変更するなど）を手動で実行する代わりに、画像を編集または作成する<b>論理的な手順</b>を構築します。 これは、「ノード」と呼ばれる小さな構成要素のネットワークを構築することによって起こります。 画像データは、<b>から右</b>へと構成要素を通って移動し、情報のパスを決定するリンクによって接続されます。 すべてのノードが接続されている場合は、最終的な結果に貢献します。

主な利点は、ワークフローが<b>非線形</b>になることです。 履歴スタックに入る手動の操作とは異なり、いつでもNodeをスワップまたは変更できます。 最初のコントラスト調整で、画像の結果に最後まで影響し過ぎたと判断した場合は、後で実行したすべての作業を失うことなく、元に戻して調整したり、完全に切り抜いたりすることができます。

![簡略化されたグラフインスタンス](workflow-overview.resources/sub-graph.png "簡略化されたグラフインスタンス")

## グラフインスタンスワークフロー

グラフのインスタンス化は、Designerの重要なプロセスです。 任意のサイズや種類のノードを取得し、それを新しいグラフ構築ブロックとしてパッケージ化することで、独自のノードを構築できます。 この種のノードは「グラフインスタンス」と呼ばれます。これにより、はるかに効率的になり、時間を節約し、他の人と作業を分かち合うことができます。 例えば、エッジの摩耗に優れた技術を開発しましたか？ グラフインスタンスを作成して自分で再利用したり、コミュニティやチームと共有したりできます。

[Substance グラフ](../../compositing-graphs/substance-compositing-graphs.md)のグラフインスタンスの詳細については、ドキュメントに[専用のセクション](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)があります。

![簡略化されたグラフパラメーター](workflow-overview.resources/parameters-5.png "簡略化されたグラフパラメーター"){zoomable="yes"}

## カスタムパラメーター

操作のチェーン内のノードには、ボタン、スライダー、微調整のための設定などの何らかの形のコントロールがあり、最終結果に影響します。 サブアプリケーションを作成したり、Substanceファイルを別のグラフに書き出したりする場合、ファイル用に独自の「コントロールパネル」を構築できます。これにより、グラフを使用するすべてのユーザーが、完全に固有のコントロールパネルを使用してファイルの微調整および編集を行うことができ、無限の可能性が表示されます。 [ここでカスタムパラメーターの一般的な概念について説明します](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md)。または、深度をさらに進めて[パラメーターの表示を開始します](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)。

## グラフの種類

Substance 3D Designerで編集できる3種類のグラフの概要と、関連するドキュメントへのリンクを以下に示します。

<table>
<tr style="border: 0;">
<td style="border: 0; width: 20%; vertical-align: top">

![](workflow-overview.resources/graph-5.png){width="120px"}

</td>
<td style="border: 0; vertical-align: top">

### Substance グラフ

[グラフ](https://substance3d.adobe.com/)は、Substance 3D Designerで作成されたグラフの主要な種類です。 その目的は、設定された解像度、色、または形状に制限されない2D画像データ</b>を<b>生成および処理することです。 これは、静的であらかじめ設定された結果だけでなく、極めて汎用性の高い画像処理ツールおよび生成ツールとして使用されます。

結果は、単純な白黒パターンや、他の画像でのみ実行され、それ自体ではコンテンツを生成しないフィルター、または複数のチャンネルを持つ本格的なマテリアルの形で作成できます。

グラフは[最も広くサポートされている種類のグラフ](../../getting-started/overview/overview.md)であり、さまざまなワークフローでエクスポートおよび使用できます。

</td>
</tr>
</table>

#### 例

一般的な使用例を以下に示します。

+++ シンプルなシェイプ

![グラフのシンプルなシェイプ](workflow-overview.resources/simpleshape.png "Substanceグラフのシンプルなシェイプ"){width="512px" zoomable="yes"}

デカールの単純なマスクシェイプは、[テキストの一部](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)と[ディスクシェイプ](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md)を生成し、[ディスクからエッジを抽出](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)し、最後に[これらをブレンド](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)してから、最終的な[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)として設定することで作成されます。

数字を含むテキストまたはエッジのThicknessを外部に表示して、よりダイナミックなグラフにすることができます。

+++

+++ 調整フィルター

![グラフの調整フィルター](workflow-overview.resources/simplefilter.png "Substanceグラフの調整フィルター"){width="512px" zoomable="yes"}

フィルターグラフでは、法線マップを[入力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md) （カスタムプレビュー付き）として指定し、[曲率に変換](../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)して、[コントラストを調整](../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)して、最終的な[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)として凸型のエッジのマスクを作成します。

ヒストグラムに設定されたコントラスト値を表示できるため、これはダイナミック入力スロットと組み合わせたシンプルで便利なフィルターになります。

+++

+++ フルマテリアル

![グラフの完全なマテリアル](workflow-overview.resources/simplematerial.png "Substanceグラフの完全なマテリアル"){width="512px" zoomable="yes"}

より複雑なグラフ [は2つのベースマテリアルをブレンドします](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)。 一方の[ベースマテリアル](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)はシンプルに保たれ、もう一方はユーザー設定の入力を使用して趣を加えます。 マスクを使用して、最後の[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)として設定される前に2つのマテリアルのどちらが表示されるかを判断します。

この例では、[リンク作成モード](../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)を使用して、複数のリンクの使用を簡略化します。

+++

<table>
<tr style="border: 0;">
<td style="border: 0; width: 20%; vertical-align: top">

![](workflow-overview.resources/function-1.png){width="120px"}

</td>
<td style="border: 0; vertical-align: top">

### Substance関数グラフ

関数<b>は、画像データ（ピクセルのセット全体）ではなく、単一の値</b>を処理します。 関数はノードネットワークを持つグラフでもありますが、[使用されるノード](../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)およびインターフェイスは[通常のSubstance グラフ](../../compositing-graphs/substance-compositing-graphs.md)とは異なります。 このワークフローは、<b>算術演算</b>に完全に基づいており、画像プレビューのサムネールが表示されることはありません。そのため、Substance 3D Designerを使用した<b>はるかに高度な作業</b>になります。

関数は、多くの異なるコンテキストで使用できます。主なコンテキストは、[公開されたパラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)の動作を変更すること、[ピクセルプロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)または[FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)の動作を作成すること、およびSubstanceグラフで[値](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)を使用することです。

</td>
</tr>
</table>

#### 例

以下に、Substance関数グラフの一般的な使用例をいくつか示します。

+++ 単純関数

![簡易関数グラフ](workflow-overview.resources/lerpfunction.png "簡易関数グラフ"){width="256px" zoomable="yes"}

公開されたパラメーターのコンテキスト内の単純な関数です。 「Intensity」という入力float値を取得し、0 ～ 1（わかりやすい範囲）の範囲を決定し、0.1 ～ 0.8の設定範囲に再マップします。 つまり、ユーザが強度を0に設定すると、内部的には0.1が使用され、Uiが1に設定されると0.8が使用され、その間の値はリニアに補間されます。 この種類の関数は、[パラメーターを公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)する際に一般的に使用されますが、カスタム関数を使用します。

この関数は、HLSLやGLSLに似た擬似コードで&#x200B;*lerp(0.1, 0.8, Intensity)*&#x200B;と記述することもできます。

+++

+++ 高度な機能

![高度な関数](workflow-overview.resources/pixel-function.png "高度な関数"){width="512px" zoomable="yes"}

この高度な関数は、2番目のグレースケールマスク入力の強度に基づいてカラーマップ入力の色相を調整するための[ピクセルプロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)の内部動作を示しています。

システム「$pos」変数を使用して両方の入力をサンプリングし、Alphaを取り除き、カラー値をHSLに変換します。次に、サンプリングしたグレースケール値を掛けて色相コンポーネントを変更します。 その後、ベクトルを再度組み立て、HSLをRGBに戻し、最終出力にAlphaを戻します。

疑似コードでは、これは1行では収まらない、より複雑な関数になります。

+++
