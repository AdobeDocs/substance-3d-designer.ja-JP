---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic-validate.html"
breadcrumb-title: ''
description: PBR BaseColor Metallic検証ノードを使用して、PBRマテリアルのベースカラーとメタリック値を検証し、修正します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR BaseColor  Metallic Validate
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBRベースカラーメタリックの検証
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---


# PBRベースカラー/メタリックの検証

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

## PBRベースカラー/メタリックの検証

**場所：** *マテリアルフィルター/PBRユーティリティ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

PBR標準に従って正しい値または正しくない値を持つ、正しい値から悪い値への「ヒートマップ」を生成するユーティリティノード。

これは、PBRの学習ツールとして非常に便利です。エラーの内容と場所を視覚的に明確にフィードバックできます。

これはツールの最終段階で使用するのではなく、このツールで強調される可能性のあるルールを違反する理由を常に明確に理解していることを確認してください。

## パラメーター

* **入力規則モード**: *アルベド、メタル、組み合わせ*&#x200B;アルベド、メタル、組み合わせ両方のみをオーバービューモードとしてチェックするように設定します。
* **アルベドの暗い範囲のしきい値**: *50 sRGB, 30 sRGB*&#x200B;アルベドの下限を50または30 sRGBに設定します。 赤色の領域の許容値を増減できます。
* **金属の反射率範囲**: *70 ～ 100%反射、60 ～ 100%反射*&#x200B;金属の範囲を変更して正しいと見なします。 赤色の領域の許容値を増減できます。
* **オーバーレイマップ**: *False/True*&#x200B;入力マップをオーバーレイするクイックデバッグモードで、問題のある領域をすばやく追跡できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
