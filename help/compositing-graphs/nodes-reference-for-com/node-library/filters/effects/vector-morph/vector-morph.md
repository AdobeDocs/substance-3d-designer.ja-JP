---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/vector-morph.html"
breadcrumb-title: ''
description: ベクトルモーフノードは、ベクトルフィールドを使用して2つの入力間のテクスチャをスムーズなトランジションにモーフィングする場合に使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Vector Morph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベクターモーフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '188'
ht-degree: 2%

---


# ベクターモーフ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](vector-morph.resources/vector-morph-01.png)![](vector-morph.resources/vector-morph-02.png)

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベクトルマップを使用して入力画像を変形します。 このエフェクトは、ゆがみでNormalmapを使用する場合や、ビデオゲームシェーダで「フローマップ」を使用する場合に似ています。 入力ピクセルは、ベクトルマップの赤と緑の値で定義されたベクトルによって移動されます。

このノード自体は最も使いにくいものではありませんが、適切なベクターマップを作成する際には注意が必要です。 モーフィング時の精度を確保するために、最高のビット深度を使用することをお勧めします。

ベクターモーフは[ベクターワープ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/vector-warp/vector-warp.md)と非常によく似ています。主な違いは、このモーフノードがキャンバスの境界の外に押し出されたときに結果を「ループ」または「タイリング」しないことです。 代わりに、クランプしてエッジを繰り返します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>カラー/グレースケール入力</i> | ワープのターゲットにするソース入力。 |
| <b>ベクターフィールド</b> <i>カラー入力</i> | ワープの駆動に使用するベクターマップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>金額</b> <i>0.0 - 1.0</i> | ワープ効果の強度を設定します。これは、ベクトルマップの乗数として機能します。 |
