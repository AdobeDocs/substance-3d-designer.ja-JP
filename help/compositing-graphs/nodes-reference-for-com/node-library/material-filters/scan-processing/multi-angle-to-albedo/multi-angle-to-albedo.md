---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
breadcrumb-title: ''
description: マルチアングルからアルベドへのノードを使用して、マルチアングルでスキャンされたイメージからアルベドマップを抽出し、きれいなマテリアルカラーを得ます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Albedo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチアングルからアルベド
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 2%

---


# マルチアングルからアルベド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-albedo.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、異なる照明角度で撮影された入力写真/スキャンのセットから、全照明情報の削除を試みます。 すべてのサンプルを1つの画像にまとめ、照明に影響を与えないように、可能な限りPBR補正をおこないます。

使用するサンプル数が多いほど、また照明角度の差が大きいほど、成功が大きくなることに注意してください。 4つのサンプル以降では、入力画像に応じてほぼ完全な結果が得られるはずです。 入力画像は三脚で撮影する必要があり、角度が異なる照明以外の違いはほとんどないか、理想的には何もありません。

>[!NOTE]
>
> このノードのノーマルマップバージョンについては、[標準に対するマルチアングル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)を参照してください。 入力されたデータをあらかじめ処理する場合は、[複数Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、[複数の切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md)および[複数コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)を使用します。これらのノードと組み合わせることが想定されているためです。
> 
> [ブログ投稿「スマートフォンはマテリアルスキャナーです」は、このプロセスをもう少し良く示しています。](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力1-8</b> <i>カラー入力</i> | 入力の数は、「サンプル量」パラメーターで決まります。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>サンプル量</b> <i>2 - 8</i> | 処理に使用するサンプル（入力）の数を設定します。 |
