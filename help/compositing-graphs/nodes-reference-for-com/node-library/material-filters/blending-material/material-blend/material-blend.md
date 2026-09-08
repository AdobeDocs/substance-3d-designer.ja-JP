---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: ブレンドノードを使用すると、合成マテリアルエフェクトを作成するためのマスクを使用して、マテリアル全体をブレンドすることができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 0%

---


# ブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-blend.png){width="128px"}

## ブレンド

**イン:** *マテリアルフィルター/ブレンド*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

ブレンドは、[アトミックブレンド マテリアル](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)に相当するマルチチャネルフルノードです。 グレースケールマスクに基づいて、またはオプションでカラー ID マスクの1つのカラーに基づいて、2つの完全なマテリアル（可能なすべてのチャンネル）をブレンドします。

このノードは、2つのマテリアルをブレンドし、グレースケールマップはあるがフルカラーID 烘焙がない場合に便利です。 カラーID 烘焙があり、3つ以上のマテリアルをブレンドする場合は、[マルチマテリアルブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)を使用することをお勧めします。

## パラメーター

### 入力

* **ColorID**: *カラー入力*\
  オプションのベイクカラーID マップ。
* **グレースケールマスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **チャネル**
  * メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合など、この領域でマテリアルチャンネルのオン/オフを切り替えます。
* **Diffuse**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、加算、減算、乗算、加算/減算、最大、最小、切り替え*
* **Base color**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、加算、減算、乗算、加算/減算、最大、最小、切り替え*
* **標準**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
* **Specular**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **放射体**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **光沢**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **粗さ**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **メタリック**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **Specular level**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **環境オクルージョン**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **Height**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **不透明度**
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景のブレンドの不透明度
  * **描画モード**: *通常、追加、減算、乗算、加算/減算、最大、最小、切り替え*
* **カラー ID マスク**: *False/True*&#x200B;グレースケールマスクの代わりにカラー ID マスクを使用します。 これは1つのカラーのみに適用されることに注意してください。
* **カラー**: *（カラー値）*選択して白に変換するカラー。
* **許容量**: *0.01 ～ 1.0*&#x200B;選択した色が周囲の色とブレンドされる度合いです。
* **パディング**: *0.0 ～ 1.0*&#x200B;選択した色のトランジションのコントラスト。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
