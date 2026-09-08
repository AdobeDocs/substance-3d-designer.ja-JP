---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
breadcrumb-title: ''
description: 「ビットマップをマテリアルに変換」ノードを使用すると、ビットマップ画像を高速なワークフロー用に最適化された照明のマテリアルにすばやく変換できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > 1-Click > Bitmap to Material Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ビットマップからマテリアルライト
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 11%

---


# ビットマップからマテリアルライト

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

<b>イン：</b> マテリアルフィルター > ワンクリック

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、1つのDiffuse/ベースカラー入力をフルマテリアルに変換します。 個別に購入できる[Allegorithmicの本格的なBitmap2マテリアル](https://www.allegorithmic.com/products/bitmap2material)のシンプルな「軽い」バージョンは、完全版の味わいを少し醸し出しています。 単純な場合にも適切に機能します。

完全なPBR正しいマテリアルが得られることは保証されていませんが、画像が1つしかなく、完全なマテリアルが必要な場合は、開始するのに適した迅速な方法です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域のマテリアルチャンネルのオン/オフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合などです。 |
| <b>グローバル</b> |  |
| <b>深度残高</b> <i>-1.0 - 1.0</i> | ハイトマップのバイアス/シフトを設定します。 |
| <b>拡散</b> |  |
| <b>シャープ</b> <i>0.0 - 1.0</i> | 拡散の結果にシャープを追加します。 |
| <b>色相</b> <i>0.0 - 1.0</i> | 選択した色相シフトで拡散する色合い。 |
| <b>彩度</b> <i>0.0 - 1.0</i> | Diffuse結果の彩度を変更します。 |
| <b>明るさ</b> <i>0.0 - 1.0</i> | Diffuse結果の明るさを調整します。 |
| <b>コントラスト</b> <i>-1.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>リリーフ</b> | リリーフグループは、通常およびHeight出力の両方を制御します。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 標準の書式を切り替えます（緑を反転）。 |
| <b>生成されたリリーフを反転する</b> <i>False/True</i> | Heightの解釈を反転します。 |
| <b>通常の強さ</b> <i>0.0 - 20.0</i> | 生成されたNormalmapの強さを設定します。 |
| <b>リリーフイコライザー</b> <i>0.0 - 1.0</i> | 異なる詳細尺度の変換残高を設定します。 |
| <b>ピンチの強さ</b> <i>0.0 - 1.0</i> | 標準トランジションをよりシャープにします。 シャープのフィルターを効果的に追加した後に、通常の画像に変換します。これにより、エッジがより鮮明になります。 |
| <b>標準のシャープ</b> <i>0.0 - 1.0</i> | 変換後の法線マップをシャープにして、ディテールを際立たせます。 |
| <b>通常のソフト</b> <i>0.0 - 1.0</i> | 変換後に法線マップをソフトにし、ディテールを隠します。 |
| <b>Specular</b> |  |
| <b>Specular Diffuseの影響</b> <i>0.0 - 1.0</i> | Specularに対する拡散反射光の影響を設定します。 光沢と粗さの出力にも影響します。 |
| <b>Specularの彩度</b> <i>0.0 - 1.0</i> | Specular出力の彩度を変更します。 |
| <b>Specularシャープ</b> <i>0.0 - 1.0</i> | Specular出力をシャープにします。 |
| </b>の<b>Specular level <i>0.0 - 1.0</i> | Specular変換の入力レベルを設定します。 |
| <b>Specular levelアウト</b> <i>0.0 - 1.0</i> | Specularの出力レベルを変更します。 |
| <b>Specularの影響</b> <i>0.0 - 1.0</i> | オプションのメタリック入力がSpecularマップに与える影響を指定します。 |
| <b>光沢</b> |  |
| <b>光沢度レベル</b> <i>0.0 - 1.0</i> | 光沢度変換の入力レベルを設定します。 |
| <b>光沢度レベルアウト</b> <i>0.0 - 1.0</i> | 光沢度出力レベルを変更します。 |
| <b>光沢度の影響</b> <i>0.0 - 1.0</i> | オプションのメタリック入力が光沢度マップに与える影響を指定します。 |
| <b>粗さ</b> |  |
| <b>ラフネスレベル</b> <i>0.0 - 1.0</i> | ラフネス変換の入力レベルを設定します。 |
| <b>ラフネスレベルアウト</b> <i>0.0 - 1.0</i> | ラフネス出力レベルを変更します。 |
| <b>メタリックラフネスの影響</b> <i>0.0 - 1.0</i> | オプションのメタリック入力が光沢度マップに与える影響を指定します。 |
| <b>環境オクルージョン</b> |  |
| <b>DiffuseのAmbient occlusion</b> <i>0.0 - 1.0</i> | 生成されたAOのDiffuse出力のブレンド。 |
| <b>Ambient occlusionスプレッド</b> <i>0.0 - 1.0</i> | 生成されたAOの広がりの範囲を設定します。 |
| <b>Ambient occlusion光の距離</b> <i>0.0 - 1.0</i> | AO 「深度」変換を設定します。 スプレッドが大きい場合は影響が小さくなります。 |
| <b>Ambient occlusion光角</b> <i>0.0 - 1.0</i> | フェイクライティングAOキャスト角度を設定します。 反対の角度に設定されている場合は、拡散反射光に既にある方向AOを補正するために使用できます。 |
| <b>Ambient occlusionレベル</b> <i>0.0 - 1.0</i> | AO出力レベルを変更します。 |
