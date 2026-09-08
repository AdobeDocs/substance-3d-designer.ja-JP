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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 1%

---


# PBRベースカラー/メタリックの検証

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/pbr-basecolor-metallic-validate.png){width="128px"}

<b>イン：</b> マテリアルフィルター > PBRユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

PBR標準に従って正しい値または正しくない値を持つ、正しい値から悪い値への「ヒートマップ」を生成するユーティリティノード。

これは、PBRの学習ツールとして非常に便利です。エラーの内容と場所を視覚的に明確にフィードバックできます。

これはツールの最終段階で使用するのではなく、このツールで強調される可能性のあるルールを違反する理由を常に明確に理解していることを確認してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>検証モード</b> <i>アルベド、メタル、組み合わせ</i> | アルベド、メタル、またはその両方をオーバービューモードとして組み合わせてチェックするかどうかを設定します。 |
| <b>アルベドの暗い範囲のしきい値</b> <i>50 sRGB, 30 sRGB</i> | アルベドの下限を50または30 sRGBに設定します。 赤色の領域の許容値を増減できます。 |
| <b>金属の反射率範囲</b> <i>70 ～ 100%反射、60 ～ 100%反射</i> | メタリック範囲が正しいと見なされるように変更します。 赤色の領域の許容値を増減できます。 |
| <b>オーバーレイマップ</b> <i>False/True</i> | クイックデバッグモードを使用して入力マップをオーバーレイすると、問題のある領域をすばやくトラッキングできます。 |
