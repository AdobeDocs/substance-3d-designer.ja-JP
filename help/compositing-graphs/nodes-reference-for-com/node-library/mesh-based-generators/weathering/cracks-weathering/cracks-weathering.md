---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: メッシュの曲率と応力ポイントに基づいてマテリアルに亀裂パターンを追加するには、[亀裂の風化]ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 亀裂風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 1%

---


# 亀裂風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/cracks-weathering.png){width="128px"}

## 亀裂風化

**イン：** *メッシュベースのジェネレーター**/耐候性*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

これは完全なマテリアル効果で、複数のチャンネルで同時に機能します。 拡散と深度を制御して、ランダムな亀裂パターンを追加します。

完全なマテリアルを扱う場合は、[リンク作成モード](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)を正しく理解してください。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  ベイク処理または生成されたマップで、内部エフェクトおよびマスキングに使用されます。
* **Height** : *グレースケール入力*\
  ベイク処理または生成されたマップで、内部エフェクトおよびマスキングに使用されます。
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
  * **亀裂の伝達**: *0.0 ～ 1.0*&#x200B;亀裂の範囲。 このエフェクトのメインコントロールです。
  * **亀裂の深度**: *0.0 ～ 1.0*&#x200B;ひび割れ効果の深度。 主にHeightに生じ、わずかに腟のThicknessにも生じる。
* **ブレンド**
  * 生成される各チャンネルにエフェクトをブレンドする強さを制御します。

## サンプル画像

![](../../../../../../assets/cracks-ex.gif)

</td>
</tr>
</table>
