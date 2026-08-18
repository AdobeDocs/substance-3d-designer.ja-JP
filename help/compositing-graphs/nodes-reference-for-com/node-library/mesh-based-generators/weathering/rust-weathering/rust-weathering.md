---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rust-weathering.html"
breadcrumb-title: ''
description: 錆の風化ノードを使用して、メッシュジオメトリに基づいて錆パターンを作成し、リアルな金属腐食効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rust Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 錆風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 1%

---


# 錆風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rust-weathering.png){width="128px"}

## 錆風化

**イン：** *メッシュベースのジェネレーター**/耐候性*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

## パラメーター

### 入力

* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **曲率**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **位置**: *カラー入力*
* **マスク** : *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。

### パラメーター

* **チャネル**
  * この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。
* **詳細**
  * **標準の形式**: *DirectX、OpenGL*\
    異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。
  * **マスク**: *False/True*\
    マスクマップの使用のオン/オフを切り替えます。
* **効果**
  * **錆の分散**: *0.0 - 1.0*
  * **Smoothnessの展開**: *0.0 - 1.0*
  * **西欧のダメージスケール**: *0.0 ～ 1.0*
  * **滴の強さ**: *0.0 ～ 1.0*
  * **滴のサンプル量**: *0 - 32*
  * **Smoothnessの滴り**: *0.0 ～ 1.0*
* **ブレンド**
  * **拡散反射光の強度**: *0.0 ～ 1.0*\
    拡散反射光のブレンド強度。
  * **基本色の適用度**: *0.0 - 1.0*\
    ベースカラーのブレンド強度。
  * **法線の強度**: *0.0 ～ 32.0*\
    法線のブレンド強度。
  * **Specularの適用度**: *0.0 ～ 1.0*\
    Specularのブレンド強度。
  * **光沢強度**: *0.0 ～ 1.0*\
    光沢のブレンド強度。
  * **粗さ強度**: *0.0 ～ 1.0*\
    粗さのブレンド強度。
  * **金属の強度**: *0.0 ～ 1.0*\
    メタリックのブレンド強度。
  * **周囲オクルージョンの強さ**: *0.0 ～ 1.0*\
    アンビエントオクルージョンのブレンド強度。
  * **Heightの強さ**: *0.0 ～ 1.0*\
    Heightのブレンド強度。

## サンプル画像

![](../../../../../../assets/rust-ex.gif)

</td>
</tr>
</table>
