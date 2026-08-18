---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: マテリアル調整描画ノードを使用して、マテリアル間のマテリアル調整をブレンドし、コンポジット効果を微調整します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアル調整ブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# マテリアル調整ブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

## マテリアル調整ブレンド

**イン：** *マテリアルフィルター/描画*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードを使用すると、マスクに基づいて、マテリアル全体の任意のチャンネルとすべてのチャンネルを調整できます。 これは、完全なマテリアルワークフローをより簡単かつ迅速にすることを目的としています。

このエフェクトは、同じマスクに基づいてマテリアルのいくつかのチャンネルを調整する（拡散反射光を明るくしたり粗さを暗くするなど）場合に便利です。

## パラメーター

### 入力

* **カラー ID マスク**: *カラー入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。
* **グレースケールマスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **チャネル**\
  この領域のマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/粗さの代わりにSpecular/光沢マップを使用する場合などです。\
  これにより、チャンネルの関連するグループの表示も有効または無効になります。
* **拡散**\
  マスクによって定義された領域の拡散チャンネルに対して調整操作を実行します。
* **基本色**\
  マスクによって定義された領域のベースカラーチャンネルに対して調整操作を実行します。
* **標準**
  * **適用度**: *0.0 ～ 1.0*&#x200B;通常の適用度を下げます
* **Specular**\
  マスクによって定義された領域のSpecularチャンネルに対して調整処理を行います。
* **放射体**\
  マスクによって定義された領域のエミッシブチャンネルに対して調整操作を実行します。
* **光沢**\
  マスクによって定義された領域の光沢チャンネルに調整操作を実行します。
* **粗さ**\
  マスクによって定義される領域の粗さチャンネルに対して調整操作を実行します。
* **メタリック**\
  マスクによって定義された領域のメタリックチャンネルに対して調整操作を実行します。
* **Specular level**\
  マスクによって定義された領域のSpecular levelチャンネルに対して調整が行われます。
* **環境オクルージョン**\
  マスクによって定義された領域のアンビエントオクルージョンチャンネルに対して調整処理を行います。
* **Height**\
  マスクによって定義された領域のHeightチャンネルに対して調整が行われます。
* **不透明度**\
  マスクによって定義された領域の不透明度チャンネルに対して調整操作を実行します。
* **カラー ID マスク**: *False/True*&#x200B;グレースケールマスクの代わりにカラー ID マスクを使用するように設定します。
* **許容量**: *0.01 - 1.0*&#x200B;カラー ID マスクが有効になっている場合、色IDの選択範囲の色の範囲が決まります。
* **カラー**: *（カラー値）*カラーIDマップとマスクから選択する色を設定します。
* **パディング**: *0.0 ～ 1.0*&#x200B;カラーIDマスクの描画コントラストとトランジションを決定します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
