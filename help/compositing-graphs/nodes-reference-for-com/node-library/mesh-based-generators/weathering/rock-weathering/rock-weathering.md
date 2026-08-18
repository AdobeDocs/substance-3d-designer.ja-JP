---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/rock-weathering.html"
breadcrumb-title: ''
description: 岩石の風化ノードを使用して、メッシュジオメトリに基づいて岩石サーフェスに風化パターンを生成し、リアルな浸食効果を得ることができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Rock Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 岩石風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# 岩石風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/rock-weathering.png){width="128px"}

## 岩石風化

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
* **標準WS**: *色入力*\
  内部エフェクトやマスキングに使用する、ベイク処理されたワールド空間の法線マップ。
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
  * **Dust**: *0.0 ～ 1.0*
  * **汚れ**: *0.0 ～ 1.0*
  * **損耗したエッジ**: *0.0 ～ 1.0*
  * **使用済みロック**: *0.0 ～ 1.0*
  * **亀裂スケール**: *1.0 ～ 60.0*
  * **亀裂の適用度**: *0.0 ～ 1.0*
  * **年齢**: *0.0 ～ 1.0*
  * **年齢しきい値**: *0.0 ～ 1.0*
  * **シャープエッジScratchesスケール**: *1.0 - 32.0*
  * **シャープなエッジScratchesのワープの強さ**: *0.0 ～ 1.0*
  * **岩の彩度低下を使用**: *0.0 ～ 1.0*
  * **使用済みの岩の明るさ**: *0.0 ～ 1.0*
* **ブレンド**
  * **拡散反射光の強度**: *0.0 ～ 1.0*\
    拡散反射光のブレンド強度。
  * **基本色の適用度**: *0.0 - 1.0*\
    ベースカラーのブレンド強度。
  * **法線の強度**: *0.0 ～ 64.0*\
    法線のブレンド強度。
  * **Specularの適用度**: *0.0 ～ 1.0*\
    Specularのブレンド強度。
  * **光沢強度**: *0.0 ～ 1.0*\
    光沢のブレンド強度。
  * **粗さ強度**: *0.0 ～ 1.0*\
    粗さのブレンド強度。
  * **周囲オクルージョンの強さ**: *0.0 ～ 1.0*\
    アンビエントオクルージョンのブレンド強度。
  * **Heightの強さ**: *0.0 ～ 1.0*\
    Heightのブレンド強度。

## サンプル画像

![](../../../../../../assets/rock-ex.gif)

</td>
</tr>
</table>
