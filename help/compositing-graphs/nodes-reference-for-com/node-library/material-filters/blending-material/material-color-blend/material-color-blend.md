---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: マテリアルの色のブレンドノードを使用して、マテリアル間のカラーチャンネルをブレンドし、合成マテリアル効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルカラーブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---


# マテリアルカラーブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-color-blend.png){width="128px"}

## マテリアルカラーブレンド

**イン：** *マテリアルフィルター/描画*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードを使用すると、その上に単色をブレンドして、マルチチャンネル、フルマテリアルに調整することができます。 これは、[マテリアル調整ブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)との主な違いです。このブレンドでは、チャンネルに対して[レベル](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)の種類の調整のみが可能ですが、このノードでは、単色の[ブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)の種類の調整を使用しています。

このノードは、拡散反射光またはベースカラーにフラットカラーのヒントを導入する場合、または設定されたソリッドカラー値を使用して他のチャンネルを「フラット」にする場合に最も便利です。

## パラメーター

### 入力

* **ColorID**: *カラー入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。
* **グレースケールマスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **チャネル**
  * この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用します。
* **拡散**
  * **カラー**: *（カラー値）*拡散チャンネルの上でブレンドするカラー値。
  * **不透明度**: *0.0 ～ 1.0*\
    前景と背景の間のブレンド不透明度。
  * **描画モード**: *通常、加算、減算、乗算、加算/減算、最大、最小、切り替え*&#x200B;描画モードを操作で使用します。
* **基本色**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **標準**
  * **ソース**: *Height、マスク*
  * **描画モード** : *結合、ブレンド*
  * **Heightの強さ**: *0.0 ～ 1.0*
  * **Heightの不透明度**: *0.0 ～ 1.0*
  * **形式**: *DirectX、OpenGL*
* **Specular**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **放射体**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **光沢**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **粗さ**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **メタリック**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **Specular level**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **環境オクルージョン**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **Height**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **不透明度**
  * このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。
* **カラー ID マスク**: *False/True*&#x200B;グレースケールマスクの代わりにカラー ID マスクを使用します。 これは1つのカラーのみに適用されることに注意してください。\
  以下のすべてのオプションを有効にします。
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
