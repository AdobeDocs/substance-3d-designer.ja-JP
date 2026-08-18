---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
breadcrumb-title: ''
description: '[PBR レンダリングマッピング]ノードを使用して、マテリアル出力を異なるPBR レンダリングマッピング形式に変換します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > PBR Render Mapping
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PBR レンダリングマッピング
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# PBR レンダリングマッピング

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-render-mapping-color.png)![](../../../../../../assets/pbr-render-mapping-grayscale.png)

## PBR レンダリングマッピング（カラー/グレースケール）

**場所：** *マテリアルフィルター/PBRユーティリティ*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

これは[PBR レンダリングノード](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)の拡張ノードで、以前の[PBR レンダリング](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)から別のテクスチャを図形にマップできます。 主な目的は、以下の例のように、個々のチャンネルを[PBR レンダリング](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)からシェイプに再マップして、複合マップチャンネルのブレイクダウンを作成できるようにすることです。 PBR レンダリングマッピングノードをコンポーネントとして使用して、独自の複合メソッドとマスクを自由に作成できます。

拡散反射光マップには色を、粗さ、金属、およびその他のグレースケールマップにはグレースケールを使用という、2種類のデータに対してカラーとグレースケールのバージョンがあります。

### 入力

* **テクスチャ**: *カラー/グレースケール入力*\
  シェイプにマッピングするテクスチャ。
* **UV**: *色入力*[データノードからの必須のUV PBR レンダリング入力。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)

## パラメーター

* **背景色**: *（カラー値）*背景で使用する単色の値を設定します。

## サンプル画像

例は、[線形グラデーション](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)の[ヒストグラム選択](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md)をマスクとして使用した、4つの異なるPBR レンダリングマッピングノードの合成です。

![](../../../../../../assets/pbr-render-mapping-ex.png){width="256px"}

![](../../../../../../assets/pbr-render-mapping-ex-2.png){width="256px"}

</td>
</tr>
</table>
