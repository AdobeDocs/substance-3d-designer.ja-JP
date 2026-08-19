---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: サーフェスブラシノードを使用して、サーフェスの方向に基づいてマスクを生成し、ディレクショナルウェザリングおよび摩耗効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表面ブラシ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 1%

---


# 表面ブラシ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/surface-brush.png){width="128px"}

## 表面ブラシ

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、オブジェクトのジオメトリとAOによって隠された、オブジェクトのサーフェスに対する金属ブラシの興味深い効果を表します。

## パラメーター

### 入力

* **ワールドスペース標準**: *カラー入力*
* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **位置**: *グレースケール入力*
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  グローバル効果レベルを設定し、徐々に表示します。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **Scratchesの長さ**: *0.0 ～ 8.0*&#x200B;傷の長さを設定します。 小さい値を指定すると点に近くなり、大きい値を指定すると長い筋になります。
* **閉塞軸**: *X、Y、Z、なし*&#x200B;傷を受けるオブジェクトの軸。 傷の方向は変わりません。
* **閉塞軸の強度**: *0.0 ～ 1.0*&#x200B;軸オクルージョン効果の強度。
* **オクルージョン**: *0.0 ～ 1.0*&#x200B;咬合傷のAOの強さ。
* **シャープの適用度**: *0.0 ～ 1.0*&#x200B;傷に適用するシャープ処理の適用量を設定します。

## サンプル画像

![](../../../../../../assets/surface-brush-ex.gif)

</td>
</tr>
</table>
