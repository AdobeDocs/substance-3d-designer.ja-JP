---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/sharpen.html"
breadcrumb-title: ''
description: シャープノードを使用して、テクスチャのディテールとエッジを強調し、鮮明でくっきりとした表面のディテールを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Sharpen
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シャープ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 4%

---


# シャープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![シャープノードアイコン](../../../../assets/sharpen-4.png "シャープノードアイコン")

<b>In:</b>個のアトミックノード

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

シャープノードは、入力に対してシャープ処理を実行します。 このノードは、画像に最後の鮮明さを適用するときに便利です。

</td>
</tr>
</table>

名前は異なりますが、数学的にはPhotoshopのアンシャープマスクに非常に似ています。 これはベースカラーマップのような場合に適していますが、通常のマップやメタリックマップのようなマップでは使用しないでください。

## 入力

<b>入力</b> *カラー/グレースケール* （プライマリ）\
シャープにする画像。

## パラメーター

<b>適用度</b> *浮動小数点*\
シャープ効果の強さを設定します。

<b>パンチスルーAlpha</b> *ブール値* （カラー画像が<b>入力</b>に接続されている場合に使用できます）\
画像のアルファチャンネルにシャープを適用するか、変更しないかを指定します。

## 例

![Sharpenノード – 例1](../../../../assets/sharpen-ex.png "Sharpenノード – 例1")
