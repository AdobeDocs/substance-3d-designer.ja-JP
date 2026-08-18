---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: Leather Weatheringノードを使用して、メッシュの曲率に基づいてLeatherマテリアルに磨耗パターンとエージングエフェクトを追加します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レザー風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---


# レザー風化

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

## レザー風化

**イン：** *メッシュベースのジェネレーター**/耐候性*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

これは完全なマテリアル効果で、複数のチャンネルで同時に機能します。 年齢と汚れをコントロールしながら、ランダムなレザーの摩耗効果を追加します。 [ファブリックウェザリング](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)に似ていますが、特に革に合わせて調整されています。\
このエフェクトは、ベイク処理されたAOとワールド空間の適切なノーマルマップを差し込まないと、すべてが適切に計算および生成される必要があるため、うまく機能しません。

すべてのマテリアルを扱う場合は、[リンク作成モード](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)について十分に理解してください。

## パラメーター

### 入力

* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。
* **標準のワールド空間**: *カラー入力*
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
  * **Dust**: *0.0 ～ 1.0*&#x200B;ワールド空間ノーマルマップで上向きの領域に基づいて、暗いDust効果でブレンドします。
  * **汚れ**: *0.0 ～ 1.0*&#x200B;全体的なDirt/指先エフェクトのブレンドです。主に、AOの遮られた（暗い）領域に基づきます。
  * **磨耗したエッジ**: *0.0 ～ 1.0*&#x200B;材料の法線に基づいて、エッジにシャープや強調の効果を追加します。
  * **使用済み**: *0.0 ～ 1.0*&#x200B;全体的に使い古されたレザーのような外観のブレンドです。
  * **年齢**: *0.0 ～ 1.0* AOを基準にした折り目の中で、着用した革にブレンドを加えます。 配置はAge Tresholdに大きく影響されます。
  * **年齢しきい値**: *0.0 ～ 1.0*&#x200B;年齢効果の外観のしきい値を設定します。
  * **亀裂スケール**: *1.0 ～ 16.0*&#x200B;着用した革の深度を使用済みとエイジの効果から設定します。
  * **亀裂のワープの強さ**: *0.0 ～ 1.0*&#x200B;着用した革の強さを、使用済みとエイジの効果から設定します。
  * **シャープエッジScratchesスケール**: *1.0 - 32.0*
  * **シャープなエッジScratchesのワープの強さ**: *0.0 ～ 1.0*
  * **使用されているレザーの彩度を下げる**: *0.0 ～ 1.0*&#x200B;使用されている効果と古い時代のレザーの外観の彩度を設定します。
  * **使用済みレザーの明るさ**: *0.0 ～ 1.0*&#x200B;古い時代の効果や使用済み効果から見た古いレザーの外観の明るさを設定します。
* **ブレンド**
  * **拡散反射光の強度**: *0.0 ～ 1.0*\
    拡散反射光のブレンド強度。
  * **基本色の適用度**: *0.0 - 1.0*\
    ベースカラーのブレンド強度。
  * **法線の強度**: *0.0 ～ 1.0*\
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

![](../../../../../../assets/leather-ex.gif)

![](../../../../../../assets/leather-ex2.png){width="233px"}

</td>
</tr>
</table>
