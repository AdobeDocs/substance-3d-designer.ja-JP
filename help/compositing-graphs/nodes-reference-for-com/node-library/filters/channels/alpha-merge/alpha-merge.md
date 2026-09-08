---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/channels/alpha-merge.html"
breadcrumb-title: ''
description: Alphaマージノードを使用して、RGBテクスチャをアルファチャンネルと組み合わせ、RGBAテクスチャを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Channels > Alpha Merge
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Alpha結合
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '89'
ht-degree: 2%

---


# Alpha結合

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/rgb-a-merge.png)

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
| <b>A</b> <i>グレースケール入力</i> | 結果のアルファとして使用されるグレースケール画像。 |
