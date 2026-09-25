---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/getting-started/workflow-overview.html"
breadcrumb-title: ""
description: Substance 3D Designerでプロシージャルマテリアルを作成する場合の基本的なワークフローについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Workflow overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ワークフローの概要
user-guide-description: ""
user-guide-title: ""
source-git-commit: 21ee545724852c876444dcf3ed4a82af8d1e3715
workflow-type: tm+mt
source-wordcount: '1117'
ht-degree: 0%
---

# ワークフローの概要

Substance 3D Designerはノードベースのエディターです。 つまり、ほぼすべての種類のプロジェクトやリソースには、ノード（構成要素）を配置し、それらを接続して一連のオペレーション(グラフ)を構築する必要があります。\
このページでは、ノードベースのワークフローの概念と、Designerで作成できる3つの主要なグラフの種類の概要を説明します。

![簡略化されたデータフロー](workflow-overview.resources/graph-direction.png "簡略化されたデータフロー"){zoomable="yes"}

## ノードベースのワークフロー

Designerでの作業は、Photoshopなどの他の2D画像編集ソフトウェアでの作業とは異なります。 手動で操作（メニューオプションに移動して彩度を調整したり、スライダーを変更するなど）を行う代わりに、画像を編集または作成する論理的な手順を構築します。 これは、「ノード」と呼ばれる小さな構成要素のネットワークを構築することによって起こります。 画像データは、<b>から右</b>へと構成要素を通って移動し、情報のパスを決定するリンクによって接続されます。 すべてのノードが接続されている場合は、最終的な結果に貢献します。

主な利点は、ワークフローが&#x200B;**非線形**&#x200B;になることです。履歴スタックに入る手動で実行された操作とは異なり、いつでもノードを入れ替えたり変更したりできます。
最終結果に影響する最初のコントラスト調整が強すぎると判断した場合は、後で実行したすべての作業を失うことなく、前に戻って調整したり、完全に切り抜いたりすることができます。

![簡略化されたグラフインスタンス](workflow-overview.resources/sub-graph.png "簡略化されたグラフインスタンス")

## グラフインスタンスワークフロー

グラフのインスタンス化は、Designerの重要なプロセスです。 グラフまたはノードの一部を再利用可能なノードとしてパッケージ化することで、独自のグラフを構築することができます。 これらは[インスタンス化](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)と呼ばれ、グラフを再利用することでより効率的に作業できます。\
例えば、エッジの摩耗に優れた技術を開発しましたか？ それを別のグラフに分割して、他のプロジェクトで再利用できます。

グラフインスタンスの詳細については、[Substance グラフ](../../compositing-graphs/substance-compositing-graphs.md)での使用に関する[専用セクション](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)があります。

![グラフのパラメーターを簡易化](workflow-overview.resources/parameters-5.png "グラフのパラメーターを簡易化"){zoomable="yes"}

## カスタムパラメーター

操作チェーン内のノードには、最終的な結果に影響を与えるボタン、スライダー、設定など、いくつかの形式のコントロールがあります。\
サブグラフを作成したり、Substanceファイルを別のアプリケーションにエクスポートする場合は、グラフ用に独自の「コントロールパネル」を構築し、他のユーザーが完全に固有のコントロールパネルを使用して微調整および変更を行うことができます。

カスタムパラメーター[こちら](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md)の一般的な概念について説明するか、詳細深度に移動して、[パラメーターの表示を開始](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)してください。

## グラフの種類

Substance 3D Designerで編集できる3種類のグラフの概要と、関連するドキュメントへのリンクを以下に示します。

<table>
<tr style="border: 0;">
<td style="border: 0;">

![](workflow-overview.resources/graph-5.png){width="120px"}

</td>
<td style="border: 0;">

### Substance グラフ

</td>
</tr>
</table>

[グラフ](https://substance3d.adobe.com/)は、Substance 3D Designerで作成されたグラフの主要な種類です。 その目的は、設定された解像度、色、または形状に制限されない2D画像データ</b>を<b>生成および処理することです。 これは、静的であらかじめ設定された結果だけでなく、極めて汎用性の高い画像処理ツールおよび生成ツールとして使用されます。

結果は、単純な白黒パターンや、他の画像でのみ実行され、それ自体ではコンテンツを生成しないフィルター、または複数のチャンネルを持つ本格的なマテリアルの形で作成できます。

グラフは[最も広くサポートされている種類のグラフ](../../getting-started/overview/overview.md)であり、さまざまなワークフローでエクスポートおよび使用できます。

#### 例

一般的なユースケースの典型的な例を以下に示します。

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
<td style="border: 0;">

![](workflow-overview.resources/function-1.png){width="120px"}

</td>
<td style="border: 0;">

### Substance機能グラフ

</td>
</tr>
</table>

関数は、ピクセル（画像）のセットではなく、**単一の値** （整数、フロート、ベクター）を処理します。 関数もノードグラフですが、[ノードが関与](../../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)しており、そのインターフェイスはSubstance グラフとは異なります。

実際、このワークフローは&#x200B;**算術演算と論理演算**&#x200B;に基づいているため、Designerではより高度な方法で作業できます。

関数はさまざまなコンテキストで使用できます。主なコンテキストは次のとおりです。
* [表示されるパラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)の動作を変更しています
* [ピクセルプロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)または[FX-Maps](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)の動作を作成しています
* 特定の目的で、グラフの画像の代わりに[値](../../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)を使用しています

#### 例

以下に、Substance関数グラフの一般的な使用例をいくつか示します。

+++ 単純関数

![単純な関数のグラフ](workflow-overview.resources/lerpfunction.png "単純な関数のグラフ"){width="256px" zoomable="yes"}

表示されるパラメーターのコンテキスト内の単純な関数。 「Intensity」という入力float値を取得し、0 ～ 1（わかりやすい範囲）の範囲を決定し、0.1 ～ 0.8の設定範囲に再マップします。 つまり、ユーザが強度を0に設定すると、内部的には0.1が使用され、UIを1に設定すると0.8が使用され、その間の値はリニアに補間されます。 この種類の関数は、[パラメーターを使用](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)する際に一般的に表示されますが、カスタム関数を使用する場合に使用されます。

この関数は、HLSLやGLSLに似た擬似コードで`lerp(0.1, 0.8, Intensity)`として記述することもできます。

+++

+++ 高度な機能

![高度な関数](workflow-overview.resources/pixel-function.png "高度な関数"){width="512px" zoomable="yes"}

この高度な関数は、2番目のグレースケールマスク入力の強さに基づいてカラーマップ入力の色相を調整するための[ピクセルプロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)の内部動作を示します。

システム「$pos」変数を使用して両方の入力をサンプリングし、Alphaをストリップし、カラー値をHSLに変換します。次に、サンプリングされたグレースケール値を掛けて色相コンポーネントを変更します。 その後、ベクトルが再度組み立てられ、HSLがRGBに変換されて、最終的な出力にAlphaが戻されます。

擬似コードでは、これはずっと複雑な関数で、1行には収まりません。

+++
