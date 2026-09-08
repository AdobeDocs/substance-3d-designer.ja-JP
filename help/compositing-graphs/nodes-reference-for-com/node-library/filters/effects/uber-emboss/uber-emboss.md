---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Uber Embossノードを使用すると、カスタマイズ可能な深度、角度、照明のコントロールを使用して高度なエンボス効果を作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber Emboss
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 2%

---


# Uber Emboss

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

## Uber Emboss

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

[エンボス](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)の機能豊富な高度なバージョンです。 ハイトマップに基づいて精巧な2Dのフェイクライティングエフェクトを実行します。

多くの制御が必要な場合に、特定のテクスチャリングスタイル用にベイクイン照明を作成するときに便利です。

## パラメーター

### 入力

* **カラー**: *カラー入力*\
  変更するベースイメージ。
* **Height**: *グレースケール入力*\
  エフェクトのドライバーとして使用されるHeightmap。

### パラメーター

* **周囲光カラー**: *（カラー値）*影のある領域で使用されるカラー。
* **拡散反射光カラー**: *（カラー値）*明るい領域で使用されるカラー。
* **Specularの色**: *（色の値）*Specularの反射に使用される色
* **光の強さ**: *0.0 ～ 1.0*\
  （偽装された）ライトの強度。
* **光源の角度**: *0.0 ～ 1.0*\
  （偽）光の入射角
* **Specularの強さ**: *0.0 ～ 1.0* Specular反射の強さ。
* **Specular 光沢度**: *0.0 ～ 1.0* Specularハイライトのサイズ。
* **ラフネス**: *0.0 ～ 1.0*&#x200B;拡散反射光の照明の計算に使用されたラフネス。
* **シャドウの不透明度**: *0.0 ～ 1.0*&#x200B;シャドウが適用された領域のブレンド不透明度。

## サンプル画像

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/uberemboss-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
