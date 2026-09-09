---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-sdf.html"
breadcrumb-title: ''
description: 3DテクスチャSDFノードを使用して、滑らかな形状と効果を作成するために、3Dデータから署名付き距離フィールドテクスチャを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture SDF
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3DテクスチャSDF
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 2%

---


# 3DテクスチャSDF

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-sdf.resources/3dtexturesdf.png){width="200px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**3DテクスチャSDF**&#x200B;ノードは、図形の&#x200B;*体積*&#x200B;のスライスを表す&#x200B;**入力**&#x200B;の&#x200B;*3Dテクスチャ*&#x200B;マスクから、図形の&#x200B;*署名付き距離フィールド*&#x200B;を生成します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>マスク入力</b> <i>グレースケール</i> | 図形の<i>体積</i>のスライスを表す<i>3Dテクスチャ</i>マスクです。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>しきい値</b> <i>フロート</i> | シェイプのボリュームが<i>フェードグラデーション</i>で記述されている場合、シェイプの<i>サーフェス</i>が<i>検出</i>されるグラデーション値を設定します。 |
| <b>出力</b> <i>整数</i> | 出力する必要がある距離フィールドの種類：<br>- <i>距離フィールド</i>：図形の<i>外側</i>の距離を示す距離フィールドを出力します。<br>- <i>符号付き距離場</i>：図形の<i>外側</i> （正）と<i>内側</i> （負）の距離を示す距離フィールドを出力します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-sdf.resources/3dtexturesdf-node.png" />
        </td>
    </tr>
</table>
