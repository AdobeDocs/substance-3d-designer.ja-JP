---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-albedo-safe-color.html"
breadcrumb-title: ''
description: PBR アルベドセーフカラーノードを使用して、アルベドのカラーがPBRマテリアルに適した物理的な範囲内であることを確認します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Albedo Safe Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR アルベドセーフカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '140'
ht-degree: 2%

---


# PBR アルベドセーフカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-albedo-safe-color.resources/pbr-albedo-safe-color.png){width="128px"}

<b>イン：</b> マテリアルフィルター > PBRユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これは、ベースカラーまたは拡散反射光の値が許容されるPBR補正範囲外の場合に補正を行うユーティリティノードです。 Metallicに設定すると、ノードはMetallic強度に基づいてベースカラー値の補正も試みます。

また、どの領域が間違っている可能性があるかについて、視覚的なフィードバックについては、[PBR BaseColor / Metallic Validate](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-basecolor-metallic/pbr-basecolor-metallic-validate.md)を参照してください。

これは簡単な修正ツールとして便利です。特に、まだPBRを学習しているが、常に正しいはずの絶対的な測定として意図されていない場合に便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>PBRワークフロー</b> <i>Base color -メタリック、Diffuse - Specular</i> | 2つの異なるPBRワークフローを切り替えます。 |
| <b>許容範囲</b> <i>0.0 - 1.0</i> | 範囲外の値に対する許容値です。 |
