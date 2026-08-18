---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-albedo.html"
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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# マルチアングルからアルベド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-angle-to-albedo.png){width="128px"}

## マルチアングルからアルベド

**イン：** *マテリアルフィルター/スキャン処理*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、異なる照明角度で撮影された入力写真/スキャンのセットから、全照明情報の削除を試みます。 すべてのサンプルを1つの画像にまとめ、照明に影響を与えないように、可能な限りPBR補正をおこないます。

使用するサンプル数が多いほど、また照明角度の差が大きいほど、成功が大きくなることに注意してください。 4つのサンプル以降では、入力画像に応じてほぼ完全な結果が得られるはずです。 入力画像は三脚で撮影する必要があり、角度が異なる照明以外の違いはほとんどないか、理想的には何もありません。

>[!NOTE]
>
> このノードのノーマルマップバージョンについては、[標準に対するマルチアングル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)を参照してください。 入力されたデータをあらかじめ処理する場合は、[複数Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、[複数の切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md)および[複数コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)を使用します。これらのノードと組み合わせることが想定されているためです。
> 
> [ブログ投稿「スマートフォンはマテリアルスキャナーです」は、このプロセスをもう少し良く示しています。](https://www.allegorithmic.com/blog/your-smartphone-material-scanner)

## パラメーター

### 入力

* **入力1-8**: *カラー入力*&#x200B;入力の数は、サンプルの量パラメーターによって決まります。

### パラメーター

* **サンプル量**: *2 - 8*&#x200B;処理に使用するサンプル（入力）の数を設定します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
