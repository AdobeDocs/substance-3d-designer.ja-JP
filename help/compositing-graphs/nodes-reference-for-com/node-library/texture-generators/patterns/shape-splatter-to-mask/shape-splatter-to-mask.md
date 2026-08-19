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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---


# マスクにスプラッタをシェイプ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-splatter-to-mask.png){width="128px"}

## マスクにスプラッタをシェイプ

**イン：** *テクスチャジェネレーター**/パターン*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

[シェイプスプラッタ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter/shape-splatter.md)データを、パターンIDに基づいて白黒のマスクに変換します。 例えば、特定の種類のパターンのみのマスクを作成できます。 パターンIDの範囲を選択したり、一部のシェイプをランダムに非表示にしたりするための追加オプションがあります。

## パラメーター

### パラメーター

* **パターンIDの開始範囲**: *1 ～ 8*&#x200B;選択する範囲内の最初のパターンIDを設定します。
* **パターンIDの終了範囲**: *1 ～ 8*&#x200B;選択する範囲内の最後のパターンIDを設定します。
* **ランダムマスク**: *0.0 ～ 1.0*&#x200B;パターンの割合をランダムにマスクアウトするように設定します。
* **出力**: *バイナリマスク、整数マスク、グレースケール値*&#x200B;出力値の種類を決定します。 バイナリマスクは白黒、0または1の値のみを返します。整数マスクウィルは、HDR形式の各パターンに対して8までの高い値をエンコードします。グレースケール値は0と1の間で比例的に範囲を広げます。

</td>
</tr>
</table>
