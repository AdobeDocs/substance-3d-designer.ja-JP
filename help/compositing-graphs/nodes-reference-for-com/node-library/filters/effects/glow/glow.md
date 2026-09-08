---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: 「光彩」ノードを使用して、テクスチャに光彩効果を加え、明るさとemissiveマテリアルのアピアランスを作り出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光彩
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 1%

---


# 光彩

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

## 光彩

**場所：** *フィルター/効果*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

他の一般的な画像編集ソフトウェアに見られるように、「光彩（外側）」タイプの効果を実行します。 基本的に、入力の周りにフェードグラデーションのアウトラインを追加します。

この機能は、アルファチャンネルを含む画像に対しては適用されません。 カラー版でも、入力としてバイナリ、黒、白のマスクのみを必要とします。色付きの光彩を使用することのみが可能です。 透明度のある画像で動作するバージョンを使用している場合は、[シェイプグロー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)を参照してください。

重要：入力に適したバージョンを使用してください。 カラー入力には「グロー」を、グレースケール入力には「グローのグレースケール」を使用します。

## パラメーター

* **グローの量**: *0.0 ～ 1.0*&#x200B;グロー効果のグローバル不透明度。
* **量をクリア**: *0.0 ～ 1.0*&#x200B;光彩効果をカットするタイミングの閾値です。 半透明領域に便利です。
* **光彩のサイズ**: *0.0 ～ 20.0*&#x200B;光彩効果が届く範囲を制御します。
* **光彩カラー**: *（カラー値） （カラーバージョンのみ）*光彩効果のカラーを設定します。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/glow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
