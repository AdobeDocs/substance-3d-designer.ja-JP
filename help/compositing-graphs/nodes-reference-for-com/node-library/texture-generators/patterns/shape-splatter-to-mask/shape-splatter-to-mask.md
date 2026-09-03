---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter-to-mask.html"
breadcrumb-title: ''
description: 「シェイプスプラッタをマスクに」ノードを使用して、シェイプスプラッターパターンをマスクに変換し、マテリアルのブレンドと効果を実現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter to Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マスクにスプラッタをシェイプ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '169'
ht-degree: 4%

---


# マスクにスプラッタをシェイプ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter-to-mask.resources/shape-splatter-to-mask-01.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[シェイプスプラッタ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)データを、パターンIDに基づいて白黒のマスクに変換します。 例えば、特定の種類のパターンのみのマスクを作成できます。 パターンIDの範囲を選択したり、一部のシェイプをランダムに非表示にしたりするための追加オプションがあります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>パターンIDの開始範囲</b> <i>1 - 8</i> | 選択する範囲の最初のパターンIDを設定します。 |
| <b>パターンIDの終了範囲</b> <i>1 - 8</i> | 選択する範囲内の最後のパターンIDを設定します。 |
| <b>ランダムマスク</b> <i>0.0 - 1.0</i> | パターンの比率をランダムにマスクアウトに設定します。 |
| <b>出力</b> <i>バイナリマスク、整数マスク、グレースケール値</i> | 出力値の種類を特定します。 バイナリマスクは白黒、0または1の値のみを返します。整数マスクウィルは、HDR形式の各パターンに対して8までの高い値をエンコードします。グレースケール値は0と1の間で比例的に範囲を広げます。 |
