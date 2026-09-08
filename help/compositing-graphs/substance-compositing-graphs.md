---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs.html"
breadcrumb-title: ''
description: テクスチャやマテリアルワークフローを作成するためのSubstance 3D DesignerのSubstance合成グラフについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance グラフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 1%

---


# Substance グラフ

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](substance-compositing-graphs.resources/graph-5.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td width="100.00%" style="border: 0;" valign="top">

[グラフ](https://substance3d.adobe.com/)は、Substance 3D Designerで作成されたグラフの主要な種類です。 その目的は、設定された解像度、色、または形状に制限されない2D画像データ</b>を<b>生成および処理することです。 これは、静的であらかじめ設定された結果だけでなく、極めて汎用性の高い画像処理ツールおよび生成ツールとして使用されます。

結果は、単純な白黒パターンや、他の画像でのみ実行され、それ自体ではコンテンツを生成しないフィルター、または複数のチャンネルを持つ本格的なマテリアルの形で作成できます。

グラフは[最も広くサポートされている種類のグラフ](../getting-started/overview/overview.md)であり、さまざまなワークフローでエクスポートおよび使用できます。

</td>
</tr>
</table>

## 例

一般的な使用例を以下に示します。

+++シンプルなシェイプ
![グラフのシンプルなシェイプ](substance-compositing-graphs.resources/simpleshape.png "Substanceグラフのシンプルなシェイプ"){width="512px"}



デカールの単純なマスクシェイプは、[テキストの一部](../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)と[ディスクシェイプ](../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape/shape.md)を生成し、[ディスクからエッジを抽出](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)し、最後に[これらをブレンド](../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)してから、最終的な[出力](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)として設定することで作成されます。

数字を含むテキストまたはエッジのThicknessを外部に表示して、よりダイナミックなグラフにすることができます。

+++

+++調整フィルター
![グラフの調整フィルター](substance-compositing-graphs.resources/simplefilter.png "Substanceグラフの調整フィルター"){width="512px"}



フィルターグラフでは、法線マップを[入力](../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md) （カスタムプレビュー付き）として指定し、[曲率に変換](../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/curvature-smooth/curvature-smooth.md)して、[コントラストを調整](../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)して、最終的な[出力](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)として凸型のエッジのマスクを作成します。

ヒストグラムに設定されたコントラスト値を表示できるため、これはダイナミック入力スロットと組み合わせたシンプルで便利なフィルターになります。

+++

+++フルマテリアル
![グラフの完全なマテリアル](substance-compositing-graphs.resources/simplematerial.png "Substanceグラフの完全なマテリアル"){width="512px"}



より複雑なグラフ[は2つのベースマテリアルをブレンドします](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-blend/material-blend.md)。 一方の[ベースマテリアル](../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)はシンプルに保たれ、もう一方は趣を加えるためにカスタム入力を使用します。 マスクを使用して、最後の[出力](../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)として設定される前に2つのマテリアルのどちらが表示されるかを判断します。

この例では、[リンク作成モード](../interface/the-graph-view/link-creation-modes/link-creation-modes.md)を使用して、複数のリンクの使用を簡略化します。

+++
