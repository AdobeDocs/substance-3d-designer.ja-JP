---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: ベースマテリアルノードを使用して、物理ベースのベースマテリアルを最初から構築するためのマテリアルプロパティを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベースマテリアル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '361'
ht-degree: 4%

---


# ベースマテリアル

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/pbr-base-material.png){width="128px"}

## ベースマテリアル

**場所：** *マテリアルフィルター/PBRユーティリティ*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

[Adobe Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)でマルチチャンネルマテリアルをすばやく簡単に作成できます。 このノードは、単純な単色の設定と値に基づいてバンドルされたフルマテリアルを返します。 これをプレースホルダーとして使用したり、複雑なマテリアルに調整したりできます。

このノードは、フルプロップをテクスチャリングして複数のマテリアルをブレンドする場合に非常に便利です。 実際、複雑なマテリアルベースを必要とせずに、このノードからマテリアルを1つずつ開始できます。

## パラメーター

### 入力

* 「User Defined Inputs」のスイッチで切り替え可能な各チャンネルのオプション入力。

### パラメーター

* **PBRワークフロー**: *メタル – ラフネス、Specular - 光沢度*&#x200B;使用するPBRモデルを設定します。
* **マテリアルプリセット**: *カスタム、誘電体、金、銀、アルミニウム、鉄、銅、チタン、ニッケル、コバルト、プラチナ*&#x200B;特定の金属を作成するための迅速なショートカット。 無関係なオプションを無効にします。
* **Base color**: *（カラー値）*Base colorに単色が使用されています。
* **メタリック**: *（グレースケール値）*メタリックに使用される実数値。
* **Diffuseの色**: *（色の値）*Diffuseに使用される単色。
* **Specular**: *（カラー値）*Specularに単色が使用されています。
* **Specularプリセット**: *プラスチック、木、石、レンガ、砂、コンクリート、布地、錆びた金属、水、氷、ガラス* PBR補正Specular値を設定するオプションのクイックプリセット。
* **Specular範囲**: *0.0 ～ 1.0* Specular範囲を調整します。
* **ラフネス- 光沢度**
  * **ラフネス値**: *（グレースケール値）*チャンネルがアクティブな場合は、グローバルの基本ラフネス値を設定します。
  * **光沢度値**: *（グレースケール値）*チャンネルがアクティブな場合に光沢度に使用される単色。
  * **経年劣化量**: *0.0 ～ 1.0*&#x200B;オプションの経年劣化マップ入力をグロスまたはラフネスに合成する範囲。
  * **タイリング**: *1 - 16*&#x200B;オプションの経年劣化マップを並べて表示する範囲。
  * **カスタム経年劣化入力**: *False/True*&#x200B;オプションのカスタム経年劣化マップを有効または無効にします。
* **標準**
  * **Heightの強さから法線**: *0.0 ～ 16.0*&#x200B;オプションで、カスタムの高さマップを法線に変換し、マテリアルの標準マップとして返します。
* **Height**
  * **Heightの位置**: *0.0 ～ 1.0* Height出力に使用される実数値です。
  * **Heightの範囲**: *0.0 ～ 1.0*&#x200B;有効になっている場合は、ユーザー定義のHeightmapの影響を設定します。
* **ユーザー定義マップ**
  * すべてのユーザ定義マップのオンとオフを切り替え、ソリッド値の代わりにこれらのマップを返します。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
