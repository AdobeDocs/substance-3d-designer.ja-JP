---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/fxmaps/the-iterate-node.html"
breadcrumb-title: ''
description: FXMapの反復ノードを使用して、マテリアルに繰り返しパターンや手続き型のバリエーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > The Iterate Node
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Iterateノード
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '341'
ht-degree: 0%

---


# Iterateノード

反復ノードでは、クアドラントノードのイメージを乗算でき、基本的には「リピータ」ノードです。 深度が1のクアドラントノードは、通常4つのクアドラントを出力します。 反復ノードを使用すると、出力イメージを必要な回数だけ繰り返し、各リピートセットを個別に処理できます。

[反復]ノードには、[反復の方法]パラメータ以外のプロパティはありません。 その結果、新しいイメージは、既定では単に四半円点ノードによって作成されたイメージにオーバーレイされ、ブレンドされます。

Iterateノードは、受け取った入力画像を繰り返します。 反復の数は、Iterationsプロパティで定義します。

Iterateノードを使用する際の重要な点は、各繰り返しイメージにアタッチされたダイナミック関数も処理されるということです。 つまり、各繰り返しには固有の調整セットを指定できます。 IterateノードのRandom Seedプロパティを使用して、この動作を変更できます。 また、動的関数内の&#x200B;*$number*&#x200B;システム変数にアクセスして、現在どの繰り返しがレンダリングされているかを確認し、それに応じて関数の結果を変更できます。

たとえば、象限ノードの各イメージにランダムな回転を適用し、その象限ノードの出力を反復ノードのアクティブな入力に送ると、繰り返される各イメージもそれぞれ独自のランダムな回転を持つようになります。

象限ノードで使用可能な同じダイナミックフィーチャはすべて、反復ノードによって生成される繰り返しイメージにも適用されます。 これは、ノードが別の深度レベルを加えるのではなく、同じレベルでクアドラントノードを複製した場合と同じです。

## パススルーコネクタ

各Iterateノードには、そのベースに沿って2つのコネクタがあります。 左側のコネクタはパススルーコネクタです。 受け取ったイメージはノードの出力コネクタにまっすぐ通され、そこで繰り返されるイメージとブレンドされます。

パススルー画像は、反復パラメータの設定に関係なく、常に処理されずに通過します。

![](../../../assets/iterate.jpg)
