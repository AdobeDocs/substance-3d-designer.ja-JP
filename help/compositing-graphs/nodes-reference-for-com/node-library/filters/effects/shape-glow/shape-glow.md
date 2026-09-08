---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: シェイプグローノードを使用して、光彩の効果をシェイプやテクスチャに加え、明るく大気のような視覚効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Glow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 1%

---


# Shape Glow

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/shape-glow-grayscale.png){width="128px"}

![](../../../../../../assets/shape-glow.png){width="128px"}

## シェイプグロー（グレースケール）

**場所：** *フィルター/効果*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

入力マスクの周囲にソフトな光彩を作成するか（グレースケールの場合）、アルファチャンネル付きのシェイプの周囲にソフトな光彩を作成します（カラーの場合）。 [光彩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md)と比較すると、この効果は他の2D画像編集ソフトウェアにより似た方法で機能します。これは、より多くのコントロールを備えたより完全な効果です。

## パラメーター

* **モード**: *ソフト、精細* 2つの精度モードを切り替えます。
* **幅**: *-1.0 ～ 1.0*&#x200B;光彩の範囲を制御します。
* **スプレッド**: *0.0 ～ 1.0*&#x200B;ぼかし効果のカットオフまたはトレッシュホールドを行うと、光彩がシェイプに近いソリッドになります。
* **不透明度**: *0.0 ～ 1.0*\
  光彩効果のブレンドの不透明度。
* **（シャドウ）カラー**: *（カラー値）*光彩に適用される色かぶり。
* **マスクカラー**: *（カラー値） *（グレースケールバージョンのみ）**透明度マップされた出力に使用される単色。
* **入力は事前に乗算されています**: *False/True *（カラーバージョンのみ）**入力を事前に乗算されたものと見なすかどうかを指定します。
* **Pre-Multiply Output**: *False/True*&#x200B;出力を事前に乗算するかどうかを指定します。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell1_position-par_dx_table_row-r0-column-c0_image" src="../../../../../../assets/shapeglow-ex.png" width="300px"/></div> |
| --- |
|  |

</td>
</tr>
</table>
