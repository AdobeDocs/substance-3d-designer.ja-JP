---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ""
description: シャープノードを使用して、テクスチャのディテールとエッジを強調し、鮮明でくっきりとしたディテールを浮かび上がらせます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シャープ
user-guide-description: ""
user-guide-title: ""
source-git-commit: 961ee151245fbc3266574676bd535c374bd0e3ad
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 4%
---

# シャープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![シャープノードアイコン](sharpen.resources/sharpen-4.png "シャープノードアイコン")

<b>イン：</b> アトミックノード

</td>
<td style="border: 0;" valign="top">

## 説明

シャープノードは、入力に対してシャープ処理を実行します。 このノードは、画像に最後の鮮明さを適用するときに便利です。

</td>
</tr>
</table>

<div data-preserve-html="true" align="center"><img src="sharpen.resources/sharpen-tooltip.gif" alt="シャープツールヒント" /></div>

名前は異なりますが、数学的にはPhotoshopのアンシャープマスクに非常に似ています。 これはベースカラーマップのような場合に適していますが、法線マップやメタリックマップのようなマップでは使用しないでください。

## 入力

<b>入力</b> *カラー/グレースケール* （プライマリ）\
シャープにする画像。

## パラメーター

<b>適用度</b> *浮動小数*\
シャープ効果の強さを設定します。

<b>パンチスルーAlpha</b> *ブーリアン* （カラー画像が<b>入力</b>に接続されている場合に使用可能）\
画像のアルファチャンネルをシャープにするか、または変更しないかを指定します。

## 例

![Sharpenノード – 例1](sharpen.resources/sharpen-ex.png "Sharpenノード – 例1")
