---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/blend/blending-modes-description.html"
breadcrumb-title: ''
description: Substance 3D Designerで、テクスチャを様々な合成エフェクトと組み合わせる際に使用できる描画モードについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Blend > Blending modes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 描画モード
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '555'
ht-degree: 2%

---


# 描画モード

[ブレンド](../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)ノードには、次の描画モードがあります。

## コピー

*コピー*&#x200B;描画モードでは、前景が背景の上に配置されるだけです。

![描画モード：コピー](../../../../../assets/image2015-8-20-9-38-0.png "描画モード：コピー"){zoomable="yes"}

カラー画像の場合、アルファチャンネルは不透明度のデフォルトで考慮されます。

これは、「Alphaブレンド」パラメーターを使用して変更できます。

![描画モード：コピー(2)](../../../../../assets/image2015-8-20-14-15-29.png "描画モード：コピー(2)"){zoomable="yes"}

## 追加(覆い焼き（リニア）)

*追加*&#x200B;描画モードでは、前景入力値が背景の対応する各ピクセルに追加されます。

![描画モード：追加(覆い焼き（リニア）](../../../../../assets/image2015-8-20-9-38-19.png "描画モード：追加(覆い焼き（リニア）)"){zoomable="yes"}

## 減算

*減算*&#x200B;描画モードは、背景内の対応する各ピクセルから前景入力値を減算します。

減算の結果が0より小さい場合、値は0に制限され、純粋なブラックになります。

![描画モード：減算](../../../../../assets/image2015-8-20-9-38-35.png "描画モード：減算"){zoomable="yes"}

## 乗算

*乗算*&#x200B;描画モードでは、背景入力値に前景の対応する各ピクセルが乗算されます。

各ピクセルの値は0 ～ 1の間で構成されるので、結果は常に元のピクセルと同じか、それよりも低く（暗く）なります。

![描画モード：乗算](../../../../../assets/image2015-8-20-9-38-53.png "描画モード：乗算"){zoomable="yes"}

## 加減算

*サブの追加*&#x200B;描画モードは次のように機能します。

* 0.5より大きい値を持つ前景ピクセルは、それぞれの背景ピクセルに追加されます。
* 0.5より小さい値を持つ前景ピクセルは、それぞれの背景ピクセルから減算されます。

![描画モード：サブを追加](../../../../../assets/image2015-8-20-9-39-11.png "描画モード：サブを追加"){zoomable="yes"}

## 最大 (明)

*最大*&#x200B;描画モードでは、背景と前景の間のより高い値が選択されます。

![描画モード：最大（明）](../../../../../assets/image2015-8-20-9-40-12.png "描画モード：最大（明）"){zoomable="yes"}

## 最小 (暗)

*分*&#x200B;描画モードでは、背景と前景の間の低い方の値が選択されます。

![描画モード：最小（暗）](../../../../../assets/image2015-8-20-9-40-31.png "描画モード：最小（暗）"){zoomable="yes"}

## スイッチ

*切り替え*&#x200B;描画モードはコピーモードに似ていますが、*重要*&#x200B;の違いが1つあります。

* &#39;Opacity&#39;を0に設定しました： &#39;Foreground&#39;入力&#x200B;*に接続されたノードのストリームは計算されません*。
* &#39;Opacity&#39;が1に設定されています： &#39;Background&#39;入力&#x200B;*に接続されたノードのストリームは計算されません*。

そのため、このモードはグラフのパフォーマンスを向上させるために使用できます。

[スイッチ](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)および[グレースケールの切り替え](../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)ノードは、これらの特定の構成のブレンドノードを使用するように設定されています。

![描画モード：スイッチ](../../../../../assets/image2015-8-20-9-38-0.png "描画モード：スイッチ"){zoomable="yes"}

## 除算

*除算*&#x200B;描画モードは、背景入力ピクセルの値を前景の対応する各ピクセルで除算します。

![描画モード：除算](../../../../../assets/image2015-8-20-9-41-32.png "描画モード：除算"){zoomable="yes"}

## オーバーレイ

*オーバーレイ*&#x200B;描画モードは、乗算とスクリーンの描画モードを組み合わせたものです。

* &#x200B;
  * 下のレイヤーのピクセルの値が0.5未満の場合は、*乗算*&#x200B;型の描画が適用されます
  * 下のレイヤーのピクセルの値が0.5より大きい場合は、*スクリーン*&#x200B;の種類の描画が適用されます

![描画モード：オーバーレイ](../../../../../assets/image2015-8-20-9-41-50.png "描画モード：オーバーレイ"){zoomable="yes"}

## スクリーン

スクリーン描画モードでは、2つの入力のピクセルの値が反転され、乗算されてから再度反転されます。

結果は乗算とは逆の効果になり、元の画像と常に同じか、それよりも高く（明るく）なります。

![描画モード：スクリーン](../../../../../assets/image2015-8-20-9-42-11.png "描画モード：スクリーン"){zoomable="yes"}

## ソフトライト

ソフトライト描画モードでは、描画色の明るさに応じて、淡い明るさまたは暗い色の結果が作成されます。

明るさが50%を超えるブレンドカラーは背景ピクセルを明るくし、明るさが50%未満のカラーは背景ピクセルを暗くします。

![描画モード：ソフトライト](../../../../../assets/image2015-8-20-9-42-32.png "描画モード：ソフトライト"){zoomable="yes"}
