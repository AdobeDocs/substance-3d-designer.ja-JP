---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: '[水面]ノードを使用すると、水面のHeightに基づいてマテリアルをブレンドして、リアルな水面の効果を作成できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水レベル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 1%

---


# 水レベル

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/water-level.png){width="128px"}

## 水レベル

**内：** *マテリアルフィルター/効果*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

材料の全量に水分レベルを追加するオールインワンエフェクトです。 効果を適用するには、入力マテリアルに高画質のハイトマップが必要です。 結果はPBR-correctです。

## パラメーター

### 入力

* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **チャネル**\
  この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。
* **水位**: *0.0 ～ 1.0*&#x200B;水位を上げたり下げたりするためのメインコントロールです。
* **水の暗さ**: *0.0 ～ 1.0*&#x200B;水の一般的な「透明度」を設定します。
* **エッジの濡れ具合**: *0.0 ～ 1.0*&#x200B;水のエッジが濡れている外観をどの程度にするかを指定します。
* **エッジの濡れ距離**: *0.0 ～ 1.0*&#x200B;濡れたエッジの到達距離を設定します。
* **深度のぼかし量**: *0.0 ～ 1.0*&#x200B;水の下の深度に基づいてぼかしの量を設定します。 ぼかしの半径を変更します。
* **深度ぼかしの不透明度**: *0.0 ～ 1.0*&#x200B;深度ぼかしのブレンド量を指定し、ぼかしの効果を下げることができます。
* **スラッジの色**: *（カラー値）*スラッジ効果の色を設定します。
* **スラッジの深度**: *0.0 ～ 1.0*&#x200B;スラッジが出現し始める深度を水面に対して設定します。
* **スラッジの不透明度**: *0.0 ～ 1.0*&#x200B;スラッジ効果のグローバル不透明度を設定します。
* **霜**: *0.0 ～ 1.0*&#x200B;霜の量を設定します。 外側のエッジから表示を開始し、内側に移動します。
* **霜の強さ**: *0.0 ～ 1.0*&#x200B;霜の強さを設定し、効果の「不透明度」を制御します。
* **フロスト亀裂**: *0.0 ～ 1.0*&#x200B;凍結から液体への移行における亀裂の量を設定します。
* **フロスト法線フォーマット**: *DirectX/OpenGL*&#x200B;フロスト法線マップ効果グリーンチャンネルを切り替えます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
