---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: 季節フィルターノードを使用して季節の効果をマテリアルに適用し、春、夏、秋、冬のバリエーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 季節フィルター
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '428'
ht-degree: 0%

---


# 季節フィルター

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

## 季節フィルター

**内：** *マテリアルフィルター/効果*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、アニメートされた水位、雪、氷、コケなどの効果を追加します。

これは、完全なPBR補正を目的としていない古いフィルターであることに注意してください。 これはレガシー/互換性の理由で保存されることが多いですが、場合によっては引き続き有用です。 最新のPBR補正版は、[Snowカバー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)と[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)で確認できます。

このノードでは、主に詳細なHeightmapまたはNormalmapを使用して、マテリアル入力の適切なセットが必要です。

## パラメーター

### 入力

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
  * **光の強さ**: *0.0 ～ 1.0*\
    （偽装された）ライトの強度。
  * **光源の角度**: *0.0 ～ 1.0*\
    （偽）光の入射角
* **効果**
  * **Heightまたは標準からの効果**: *Height、標準*&#x200B;効果を制御する入力マップを選択します。
  * **水位**: *0.0 ～ 1.0* Height/標準情報に基づいて水位を上げたり下げたりします。
  * **水のディテール**: *0.0 ～ 1.0*&#x200B;水のディテールの量を設定します。
  * **屈折**: *0.0 ～ 1.0*&#x200B;効果のフェイク屈折の量を設定します。
  * **リフレクション**: *0.0 ～ 1.0*&#x200B;効果のフェイクリフレクションの量を設定します。
  * **反射距離**: *0.0 ～ 1.0*&#x200B;反射のビジュアルを制御します。
  * **反射角**: *0.0 ～ 1.0*&#x200B;反射のビジュアルを制御します。
  * **流れの向き**: *0.0 ～ 1.0*&#x200B;アニメーションの流れを制御します（Substance Playerを使用して表示します）。
  * **氷**: *0.0 ～ 1.0*&#x200B;水の凍り具合を設定します。
  * **氷のディテール**: *0.0 ～ 1.0*&#x200B;氷のディテールの量を設定します。
  * **Snow**: *0.0 ～ 1.0*&#x200B;積雪量を設定します。
  * **コケ**: *0.0 ～ 1.0*&#x200B;コケの総量を設定します。
  * **コケのスケール**: *1 ～ 4*&#x200B;生成されたコケのテクスチャのスケールを設定します。
  * **コケのカラー**: *（カラー値）*コケのカラーを設定します。
  * **水のカラー**: *（カラー値）*アルファ/不透明度を含む水のカラーを設定します。
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

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
