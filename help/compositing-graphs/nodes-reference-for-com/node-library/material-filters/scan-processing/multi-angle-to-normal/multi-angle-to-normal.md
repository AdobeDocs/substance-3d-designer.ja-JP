---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-angle-to-normal.html"
breadcrumb-title: ''
description: '[マルチアングルから法線]ノードを使用すると、マルチアングルスキャンイメージから法線マップを生成して、正確なサーフェスの詳細を取得できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi-Angle to Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチアングルから標準
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '245'
ht-degree: 3%

---


# マルチアングルから標準

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-angle-to-normal.resources/multi-angle-to-normal.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、異なる照明条件で作成された写真/スキャンのセットからノーマルマップを構築します。 これにより、1つのアルベドイメージから法線を抽出する場合よりも、より正確な法線マップ変換が可能になります。

入力に対して一定の正確な照明角度を使用する必要があるため、[アルベドに対するマルチアングル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)よりも複雑です。 各サンプルの照明角度は均等に配置する必要があり、サンプルは順番に入力する必要があります。 したがって、3つのサンプルの場合、照明角度は0、120、240、またはそれらの均一オフセット（90、210、330など）で指定する必要があります。

>[!NOTE]
>
> このノードのアルベドバージョンについては、[アルベドへのマルチアングル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)を参照してください。 入力されたデータをあらかじめ処理する場合は、[複数Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-color-equalizer/multi-color-equalizer.md)、[複数の切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-crop/multi-crop.md)および[複数コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)を使用します。これらのノードと組み合わせることが想定されているためです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力1-8</b> <i>カラー入力</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>サンプル量</b> <i>2 - 8</i> | 処理するサンプル（入力）の量を設定します。 |
| <b>適用度</b> <i>0.0 - 1.0</i> | 法線マップ強度を設定します。 |
| <b>最初のサンプルの光源の角度</b> <i>0.0 - 360.0</i> | 最初の入力の照明角度方向を設定します。 |
| <b>次のサンプルライト角度</b> <i>反時計回り、時計回り</i> | 次のサンプルのライトが移動する方向を設定します。 |
