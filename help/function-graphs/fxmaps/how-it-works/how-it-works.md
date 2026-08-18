---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/how-it-works.html"
breadcrumb-title: ''
description: Substance 3D DesignerでFXMapを使用して関数グラフをテクスチャに適用し、プロシージャエフェクトを作成する方法について説明します。
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

この強力な機能をマスターするには、FX-Mapグラフの機能を理解することが重要です。

FX-Mapグラフには、Quadrant、Iterate、Switchという3つのFX-Mapノードタイプのうち1つまたは複数を含めることができます。 これらのノードのうち、最も頻繁に使用するのはクアドラントで、反復ノードは非常に短い時間です。

パラメーターセットノードは、FX-Mapsの原動機です。 コア領域のクアッドツリーグラフFX-Mapsに依存するグラフが作成されますが、1つとして表示されません。 視覚的には、四分木グラフはマルコフチェーンの形式で表示されます。

FX-Mapをレンダリングする際、単純化されたFX-Mapグラフは大きな木のようなグラフに見えるように「アンラップ」されます。 エンジンはクアッドツリー全体を「ウォーク」し、上から下、左から右へと進みます。

FX-Mapノードでは、イメージのコピーと貼り付けは不要です。 各イメージがレンダリングされると、そのイメージに含まれるダイナミック関数が実行されます。 この関数は、ノードによってレンダリングされる各イメージに影響を与えます。 このため、個々の画像にランダムな回転やスケール係数を設定したり、その他の調整を多数行うことができます。
