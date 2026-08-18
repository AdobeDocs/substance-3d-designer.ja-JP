---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/using-the-sampler-nodes.html"
breadcrumb-title: ''
description: FXMapでsamplerノードを使用してテクスチャをサンプリングし、プロシージャマテリアルのバリエーションを作成する方法を学習します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Using the Sampler nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Samplerノードの使用
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Samplerノードの使用

![](../../../../assets/sampler-graph.jpg)

サンプラーノードは、fx-mapノードに接続された画像入力のピクセル値をサンプリングするために使用できる。 サンプルされた値は、関数を使用してパラメーターを操作するために使用できます。

## 簡単な例

この例では、パターンのグリッドを生成するために、四半円点ノードのチェーンが作成されています。 最後の象限の[不透明度/輝度]パラメータに関数が作成されます。

![](../../../../assets/sampler-function.jpg){width="300px"}![](../../../../assets/sampler-result-1.jpg){width="300px"}

Sampleノードは、サンプル座標(x, y)としてfloat2入力を取ります。 この例では$pos変数を使用しました。各パターンについて、ピクセル値はFxMapノードに接続された最初の画像入力のパターン位置でサンプリングされます。

Sample Grayノードは、0, 1の範囲のfloat1値を返します。

Sample Colorノードは、0、1の範囲のfloat4(rgba)値を返します。

## 詳細な例

ここでは、サンプル値を定数(0.3)と比較します。 サンプル値が0.3より大きい場合は1が返され、それ以外の場合は0が返されます。

![](../../../../assets/sampler-function-advanced.jpg){width="300px"}![](../../../../assets/sampler-result-advanced.jpg){width="300px"}

## サンプルをダウンロード

[![SBSファイルアイコン](../../../../assets/sbs-1_1.png){width="64px"}](https://shared-assets.adobe.com/link/d5f9adf3-0bb5-49a1-4eb9-a0506d4f3f32)
