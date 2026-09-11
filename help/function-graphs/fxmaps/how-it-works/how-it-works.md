---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Substance 3D DesignerでFXMapを使用して、プロシージャルのエフェクトのテクスチャに関数グラフを適用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > How it works
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 使用方法
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 2%

---


# 使用方法

この強力な機能を習得するには、FX-Map グラフの仕組みを理解することが重要です。

FX-Map グラフには、Quadrant、Iterate、Switchという3つのFX-Mapノードタイプのうち1つまたは複数を含めることができます。 これらのノードのうち、最も頻繁に使用するのはクアドラントで、反復ノードは非常に短い時間です。

パラメーターセットノードは、FX-Mapsの原動機です。 コア領域のクアッドツリーグラフFX-Mapsが依存する領域を作成しますが、1つとして表示されません。 視覚的には、クワッドツリーグラフはマルコフ鎖の形で示される。

FX-Mapをレンダリングする際、シンプルなFX-Mapのグラフがラップ解除され、大きな木のようなグラフのように見えます。 エンジンは、上から下、左から右へとクアッドツリー全体を「歩く」ように見えます。

FX-Mapノードでは、画像のコピー&amp;ペーストは盲目的には行われません。 各イメージがレンダリングされると、そのイメージに含まれるダイナミック関数が実行されます。 この関数は、ノードによってレンダリングされる各イメージに影響を与えます。 このため、個々の画像にランダムな回転やスケール係数を設定したり、その他の調整を多数行うことができます。
