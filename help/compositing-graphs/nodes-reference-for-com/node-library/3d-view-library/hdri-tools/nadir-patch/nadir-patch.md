---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Nadir Patchノードを使用して、HDRIパノラマの最下部のアーティファクトを修正するために最下部の領域にパッチを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

## Nadir Patch

**イン：** *3D ビュー/HDRI ツール*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、球状にマッピングされたイメージの中央のグラウンドポイント（床面）にパッチを適用する機能を提供します。 汚い床面や、目に見えるカメラや三脚を非表示または「クローン作成」するために使用できます。 [コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)のように機能しますが、球面にマップされた画像に調整を適用します。 画像内の別の場所でポイントを選択します。つまり、コピーして元のディレクトリでブレンドしたポイントです。 1つのHDRI以外に処理に他の外部入力は必要ありませんが、外部マスクをパッチエフェクトのアルファとして使用することができます。

[Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)を使用すると、効果をすばやく確認して検証できます。

## 入力

* **入力**: *カラー入力*
* **マスク入力**: *グレースケール入力*\
  パッチのマスクに使用するオプションのマスクスロット。 アルファのように機能します。

## パラメーター

* **有効**: *False/True*\
  パッチ適用エフェクトを有効または無効にします。
* **フレームの表示ヘルパー**: *False/True*\
  デバッグ用にヘルパー行を表示または非表示にします。
* **Thickness**: *0.0 ～ 1.0*\
  ヘルパー行のThickness。
* **パッチスケール**: *0.0 ～ 1.0*\
  パッチのグローバルな均一スケール。 ソースとターゲットの両方に影響します。
* **パッチサイズ**: *0.0 - 1.0*\
  パッチのサイズが均一ではありません。
* **パッチの回転**: *0.0 - 1.0*\
  パッチの回転。 ソースとターゲットに影響します。
* **パッチAlpha**: *正方形の滑らかさ、ガウス、マスク入力*\
  パッチを背景とブレンドするときに使用するアルファを設定します。
* **パッチ硬さ**: *0.0 - 1.0*\
  アルファの硬さ/コントラストを設定します。
* **ソースの回転オフセット**: *0.0 - 1.0*\
  パッチのソースの回転のみ。
* **位置の座標**
  * **ソースの位置**:\
    ソースの位置。 2D ビューにハンドルがあります。
  * **パッチの位置**:\
    ターゲットの位置。 2D ビューにハンドルがあります。

## サンプル画像

![](../../../../../../assets/nadir-patch-ex.gif)

</td>
</tr>
</table>
