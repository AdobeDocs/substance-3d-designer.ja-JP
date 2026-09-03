---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/pbr-render-mapping.html"
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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '187'
ht-degree: 2%

---


# PBR レンダリングマッピング

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](pbr-render-mapping.resources/pbr-render-mapping-01.png)![](pbr-render-mapping.resources/pbr-render-mapping-02.png)

<b>イン：</b> マテリアルフィルター > PBRユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これは[PBR レンダリングノード](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)の拡張ノードで、以前の[PBR レンダリング](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)から別のテクスチャを図形にマップできます。 主な目的は、以下の例のように、個々のチャンネルを[PBR レンダリング](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)からシェイプに再マップして、複合マップチャンネルのブレイクダウンを作成できるようにすることです。 PBR レンダリングマッピングノードをコンポーネントとして使用して、独自の複合メソッドとマスクを自由に作成できます。

拡散反射光マップには色を、粗さ、金属、およびその他のグレースケールマップにはグレースケールを使用という、2種類のデータに対してカラーとグレースケールのバージョンがあります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>テクスチャ</b> <i>カラー/グレースケール入力</i> | シェイプにマッピングするテクスチャ。 |
| <b>UV</b> <i>カラー入力</i> | [UVノードからの必須のPBR レンダリングデータ入力。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md) |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>背景色</b> <i>（カラー値）</i> | 背景に使用する単色の値を設定します。 |

## 例

例は、[線形グラデーション](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/gradient-linear-1/gradient-linear-1.md)の[ヒストグラム選択](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-select/histogram-select.md)をマスクとして使用した、4つの異なるPBR レンダリングマッピングノードの合成です。

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="pbr-render-mapping.resources/pbr-render-mapping-04.png" />
        </td>
    </tr>
</table>
