---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-crop.html"
breadcrumb-title: ''
description: 「複数の切り抜き」ノードを使用すると、複数のテクスチャチャンネルを同時に切り抜いて、スキャンしたマテリアルを効率的に処理できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 複数の切り抜き
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 4%

---


# 複数の切り抜き

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/crop-multi.png){width="128px"}

![](../../../../../../assets/crop-multi-grayscale.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

マルチチャンネル版の切り抜きです。 画像から領域を切り抜きます。主に、マルチアングルの写真での使用が意図されています。この写真を[マルチアングルからアルベド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)または[マルチアングルから標準](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)と組み合わせます。

>[!NOTE]
>
> 詳細については、元の[切り抜き](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>入力数</b> <i>1 - 8</i> | 並列処理する入力数を設定します。 |
| <b>入力サイズ</b> <i>0 - 8192</i> | 入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。 |
| <b>背景</b> <i>（カラー値） / （グレースケール値）</i> | 切り抜きによってカバーされない領域の背景の均一値。 |
| <b>変形</b> <i>（変換行列）</i> | 結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。 |
| <b>標準（カラーバージョンのみ）</b> <i>False/True</i> | 入力をNormalmapとして扱うかどうかを指定します。 |
