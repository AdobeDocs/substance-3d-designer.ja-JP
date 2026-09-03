---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: Alphaマージノードを使用して、RGBテクスチャをRGBA テクスチャ作成用のアルファチャンネルと組み合わせます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alpha結合
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# Alpha結合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](alpha-merge.resources/alpha-merge-01.png)

<b>イン：</b>フィルター/チャネル

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

アルファチャンネルを含まない入力に、アルファチャンネルを追加します。 [RGBAマージ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)と混同しないように、このノードははるかに単純で、アルファのみを追加します。

単純ですが便利なノードで、何かをマスクするだけの場合や、結果にアルファが必要な場合に使用します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>RGB</b> <i>カラー入力</i> | アルファなしのカラー画像 |
| <b>A</b> <i>グレースケール入力</i> | 結果のアルファとして使用されるグレースケールイメージ。 |
