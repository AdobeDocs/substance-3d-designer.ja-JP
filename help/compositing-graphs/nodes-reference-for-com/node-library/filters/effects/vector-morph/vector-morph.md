---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: ベクトルモーフノードを使用すると、ベクトルフィールドを使用して2つの入力間でテクスチャをモーフィングし、滑らかなトランジションを実現できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベクターモーフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 2%

---


# ベクターモーフ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/vector-morph-grayscale.png)![](../../../../../../assets/vector-morph.png)

## ベクターモーフ（グレースケール）

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

入力画像をベクトルマップで変形します。 このエフェクトは、Normalmapを使用したUVゆがみや、ビデオゲームシェーダで「フローマップ」を使用した場合と同様です。 入力ピクセルは、ベクトルマップの赤と緑の値で定義されたベクトルによって移動されます。

このノード自体は最も使いにくいものではありませんが、適切なベクターマップを作成する際には注意が必要です。 モーフィング時の精度を確保するために、最高のビット深度を使用することをお勧めします。

ベクターモーフは[ベクターワープ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)と非常によく似ています。主な違いは、このモーフノードがキャンバスの境界の外に押し出されたときに結果を「ループ」または「タイリング」しないことです。 代わりに、クランプしてエッジを繰り返します。

## パラメーター

### 入力

* **入力**: *カラー/グレースケール入力*&#x200B;ワープのターゲットにするソース入力です。
* **ベクターフィールド**: *カラー入力*&#x200B;ワープの駆動に使用されたベクターマップです。

### パラメーター

* **量**: *0.0 ～ 1.0*&#x200B;ワープ効果の強さを設定します。この値は、ベクトルマップの乗数として機能します。

## サンプル画像

</td>
</tr>
</table>
