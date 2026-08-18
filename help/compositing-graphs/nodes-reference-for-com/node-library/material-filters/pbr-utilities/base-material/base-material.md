---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/pbr-utilities/base-material.html"
breadcrumb-title: ''
description: ベースマテリアルノードを使用して、物理的なベースのマテリアルをゼロから構築するためのベースマテリアルプロパティを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > PBR Utilities > Base Material
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベースマテリアル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
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

[Adobe Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)でマルチチャンネルマテリアルを作成する最も簡単で迅速な方法です。 このノードは、単純な単色の設定と値に基づいて、バンドルされたFullマテリアルを返します。 これをプレースホルダーとして使用したり、複雑なマテリアルに調整したりすることができます。

このノードは、完全なプロップをテクスチャリングして複数のマテリアルをブレンドする場合に非常に便利です。 実際、複雑なマテリアルベースを必要とせずに、このノードからすべてのマテリアルを開始することができます。

## パラメーター

### 入力

* 「User Defined Inputs」のスイッチで切り替え可能な各チャンネルのオプション入力。

### パラメーター

* **PBRワークフロー**: *金属 – 粗さ、Specular – 光沢*&#x200B;使用するPBRモデルを設定します。
* **マテリアルプリセット**: *カスタム、誘電体、金、銀、アルミニウム、鉄、銅、チタン、ニッケル、コバルト、プラチナ*&#x200B;特定の金属を作成するための簡単なショートカット。 無関係なオプションを無効にします。
* **基本色**: *（色値）*基本色に単色が使用されています。
* **メタリック**: *（グレースケール値）*メタリックに使用される実数値。
* **拡散反射光カラー**: *（カラー値）*拡散反射光に使用される単色。
* **Specular**: *（カラー値）*Specularに単色が使用されています。
* **Specularプリセット**: *プラスチック、木、石、レンガ、砂、コンクリート、布地、錆びた金属、水、氷、ガラス* PBR補正Specular値を設定するオプションのクイックプリセット。
* **Specular範囲**: *0.0 ～ 1.0* Specular範囲を調整します。
* **粗さ – 光沢**
  * **粗さの値**: *（グレースケール値）*チャンネルがアクティブな場合は、グローバルなベースの粗さの値を設定します。
  * **光沢度値**: *（グレースケール値）*チャンネルがアクティブな場合に光沢に使用される単色。
  * **経年劣化量**: *0.0 ～ 1.0*&#x200B;オプションの経年劣化マップ入力をグロスまたは粗さに合成する範囲。
  * **経年劣化の並べ替え**: *1 - 16*&#x200B;オプションの経年劣化マップを並べ替える範囲。
  * **カスタム経年劣化入力**: *False/True*&#x200B;オプションのカスタム経年劣化マップを有効または無効にします。
* **標準**
  * **Heightの強さから法線**: *0.0 ～ 16.0*&#x200B;必要に応じて、カスタムHeightmapを法線に変換し、マテリアルの法線マップとして返します。
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
