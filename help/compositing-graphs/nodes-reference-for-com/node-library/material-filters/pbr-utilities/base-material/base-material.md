---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: ベースマテリアルノードを使用して、物理的なベースのマテリアルをゼロから構築するためのベースマテリアルプロパティを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベースマテリアル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 6%

---


# ベースマテリアル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](base-material.resources/base-material-01.png){width="128px"}

<b>イン：</b> マテリアルフィルター > PBRユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[Adobe Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)でマルチチャンネルマテリアルを作成する最も簡単で迅速な方法です。 このノードは、単純な単色の設定と値に基づいて、バンドルされたFullマテリアルを返します。 これをプレースホルダーとして使用したり、複雑なマテリアルに調整したりすることができます。

このノードは、完全なプロップをテクスチャリングして複数のマテリアルをブレンドする場合に非常に便利です。 実際、複雑なマテリアルベースを必要とせずに、このノードからすべてのマテリアルを開始することができます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
|  | 「User Defined Inputs」のスイッチで切り替え可能な各チャンネルのオプション入力。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>PBRワークフロー</b> <i>金属 – ラフネス、Specular - 光沢度</i> | 使用するPBRモデルを設定します。 |
| <b>マテリアルプリセット</b> <i>カスタム、誘電体、金、銀、アルミニウム、鉄、銅、チタン、ニッケル、コバルト、プラチナ</i> | 特定の金属を作成するためのクイックショートカット。 無関係なオプションを無効にします。 |
| <b>基本色</b> <i>（カラー値）</i> | base colorに使用される単色です。 |
| <b>メタリック</b> <i>（グレースケール値）</i> | メタリックに使用される実数値。 |
| <b>Diffuseの色</b> <i>（カラー値）</i> | Diffuseに使用される単色です。 |
| <b>Specular</b> <i>（カラー値）</i> | Specularに使用される単色です。 |
| <b>Specularプリセット</b> <i>プラスチック、木、石、レンガ、砂、コンクリート、布地、錆びた金属、水、氷、ガラス</i> | PBR補正Specular値を設定するオプションのクイックプリセット。 |
| <b>Specular範囲</b> <i>0.0 - 1.0</i> | Specular範囲を調整します。 |
| <b>粗さ – 光沢</b> |  |
| <b>ラフネス値</b> <i>（グレースケール値）</i> | チャンネルがアクティブな場合は、グローバルの基本ラフネス値を設定します。 |
| <b>光沢度値</b> <i>（グレースケール値）</i> | チャンネルがアクティブな場合に光沢度に使用される単色。 |
| <b>経年劣化量</b> <i>0.0 - 1.0</i> | オプションの経年劣化マップ入力をグロスまたはラフネスに合成する範囲。 |
| <b>タイリング</b> <i>1 - 16</i> | オプションの経年劣化マップを並べて表示する範囲です。 |
| <b>カスタム経年劣化入力</b> <i>False/True</i> | オプションのカスタム経年劣化マップを有効または無効にします。 |
| <b>標準</b> |  |
| <b>Heightの強さから法線を計算</b> <i>0.0 - 16.0</i> | 必要に応じて、カスタムHeightmapをnormalに変換し、これをマテリアル Normalmapとして返します。 |
| <b>Height</b> |  |
| <b>Heightの位置</b> <i>0.0 - 1.0</i> | Height出力に使用される実数値。 |
| <b>Height範囲</b> <i>0.0 - 1.0</i> | ユーザ定義の高さマップが有効な場合、その影響を設定します。 |
| <b>ユーザー定義マップ</b> | すべてのユーザ定義マップのオンとオフを切り替え、ソリッド値の代わりにこれらのマップを返します。 |
