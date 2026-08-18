---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/exposure-preview.html"
breadcrumb-title: ''
description: 最終レンダリングの前に、露光量プレビューノードを使用して、HDRI環境での露光量調整をプレビューします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Exposure Preview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 露光量プレビュー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '102'
ht-degree: 1%

---


# 露光量プレビュー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/hdr-exposure-preview.png){width="200px"}

## 露光量プレビュー

**イン：** *3Dビュー/HDRI ツール*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

露出ステップをプレビューするためのヘルパーノード。 ユーザが最小値と最大値を設定すると、ノードはオリジナルの入力の公開されたバージョンが異なるより大きなイメージを生成します。 異なるバージョンは常に水平方向に積み重ねられます。量はノードまたはグラフの解像度によって異なります。

## パラメーター

* **最大露光量(EV)**: *-8.0 - 8.0*\
  一番上の最も明るい画像の最大露光量。
* **最小露光量(EV)**: *-8.0 ～ 8.0*&#x200B;最下部の最も暗い画像の最小露光量。

## サンプル画像

![](../../../../../../assets/exp-preview-ex.png)

</td>
</tr>
</table>
