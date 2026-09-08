---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/1-click/bitmap-to-material-light.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '503'
ht-degree: 0%

---


# ビットマップからマテリアルライト

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/b2m-light.png)

## ビットマップからマテリアルライト

**イン：** *マテリアルフィルター/ワンクリック*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、1つのDiffuse/ベースカラー入力をフルマテリアルに変換します。 個別に購入できる[Allegorithmicの本格的なBitmap2マテリアル](https://www.allegorithmic.com/products/bitmap2material)のシンプルな「軽い」バージョンは、完全版の味わいを少し醸し出しています。 単純な場合にも適切に機能します。

完全なPBR正しいマテリアルが得られることは保証されていませんが、画像が1つしかなく、完全なマテリアルが必要な場合は、開始するのに適した迅速な方法です。

## パラメーター

* **チャネル**
  * この領域のマテリアルチャンネルのオン/オフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合などです。
* **グローバル**
  * **深度バランス**: *-1.0 - 1.0* Heightmapのバイアス/シフトを設定します。
* **拡散**
  * **シャープ**: *0.0 ～ 1.0*&#x200B;拡散の結果にシャープを追加します。
  * **色相**: *0.0 ～ 1.0*&#x200B;ユーザーが選択した色相シフトで拡散する色合い。
  * **彩度**: *0.0 ～ 1.0* Diffuse結果の彩度を変更します。
  * **明るさ**: *0.0 ～ 1.0* Diffuse結果の明るさを調整します。
  * **コントラスト**: *-1.0 - 1.0*\
    結果のコントラストを調整します。
* **リリーフ**\
  リリーフグループは、通常およびHeight出力の両方を制御します。
  * **標準形式**: *DirectX、OpenGL*&#x200B;標準形式を切り替えます（緑に反転）。
  * **生成されたリリーフを反転**: *偽/真* Heightの解釈を反転します。
  * **法線の強度**: *0.0 ～ 20.0*&#x200B;生成された法線マップの強度を設定します。
  * **リリーフイコライザー**: *0.0 ～ 1.0*&#x200B;さまざまな詳細スケールのコンバージョンバランスを設定します。
  * **ピンチの強さ**: *0.0 ～ 1.0*&#x200B;通常のトランジションをよりシャープにします。 シャープのフィルターを効果的に追加した後に、通常の画像に変換します。これにより、エッジがより鮮明になります。
  * **通常のシャープ**: *0.0 ～ 1.0*&#x200B;変換後に通常のマップをシャープにして、ディテールを際立たせます。
  * **法線をソフト**: *0.0 ～ 1.0*&#x200B;変換後に法線マップをソフトにしてディテールを隠します。
* **Specular**
  * **Specular拡散反射光の影響**: *0.0 ～ 1.0* Specularに対する拡散反射光の影響を設定します。 光沢と粗さの出力にも影響します。
  * **Specular彩度**: *0.0 ～ 1.0* Specular出力の彩度を変更します。
  * **Specularシャープ**: *0.0 ～ 1.0* Specular出力をシャープにします。
  * **Specular level**: *0.0 ～ 1.0* Specular変換の入力レベルを設定します。
  * **Specular levelアウト**: *0.0 ～ 1.0* Specularの出力レベルを変更します。
  * **Specularの影響**: *0.0 ～ 1.0* Specularマップに対するオプションのメタリック入力の影響を決定します。
* **光沢**
  * **光沢度レベル**: *0.0 ～ 1.0*&#x200B;光沢度変換の入力レベルを設定します。
  * **光沢度レベルアウト**: *0.0 ～ 1.0*&#x200B;光沢度の出力レベルを変更します。
  * **光沢に対するメタリックの影響**: *0.0 - 1.0*&#x200B;オプションのメタリック入力が光沢マップに与える影響を決定します。
* **粗さ**
  * **粗さのレベル**: *0.0 ～ 1.0*&#x200B;粗さの解釈に使用する入力レベルを設定します。
  * **粗さのレベルアウト**: *0.0 ～ 1.0*&#x200B;粗さの出力レベルを変更します。
  * **メタリックの粗さの影響**: *0.0 - 1.0*&#x200B;光沢マップに対するオプションのメタリック入力の影響を決定します。
* **環境オクルージョン**
  * **DiffuseのAmbient occlusion**: *0.0 ～ 1.0*&#x200B;生成されたAOのDiffuse出力へのブレンド。
  * **Ambient occlusionスプレッド**: *0.0 ～ 1.0*&#x200B;生成されたAOスプレッドの範囲を設定します。
  * **Ambient occlusion光の距離**: *0.0 ～ 1.0* AOの「深度」変換を設定します。 スプレッドが大きい場合は影響が小さくなります。
  * **Ambient occlusionの光源の角度**: *0.0 ～ 1.0*&#x200B;偽の光源のAOキャスト角度を設定します。 反対の角度に設定されている場合、Diffuse内の既に存在する方向AOを補正するために使用できます。
  * **Ambient occlusionレベル**: *0.0 ～ 1.0* AO出力レベルを変更します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
