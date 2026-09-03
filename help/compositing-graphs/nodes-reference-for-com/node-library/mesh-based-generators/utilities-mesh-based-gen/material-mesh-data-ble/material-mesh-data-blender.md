---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-mesh-data-blender.html"
breadcrumb-title: ''
description: メッシュデータブレンダーノードは、マテリアルメッシュデータをブレンドして、異なるマテリアルゾーン間の滑らかなトランジションを作成する場合に使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Mesh Data Blender
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルメッシュデータブレンダー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '572'
ht-degree: 8%

---


# マテリアルメッシュデータブレンダー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-mesh-data-blender.resources/material-mesh-data-blender-01.png){width="128px"}

<b>In:</b> メッシュベースのジェネレータ>ユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、ベイクされたデータに基づいて詳細を簡単に追加できるようにすることを目的としています。 すべてのベイク済みマップを入力として使用し、入力全体のマテリアルを調整するためのスライダーが多数用意されています。 多くの選択肢があるので、試してみてください。

曲率や他のマップに基づいてエッジのハイライトを追加したり、Diffuse/ベースカラーと一部のAOをブレンドしたり、曲率やAOに基づいてSpecularのオクルージョンを追加したりするのに便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>完全なマテリアル入力（グループの「マテリアル」）</b> | マテリアルマップのフルセット。<br><br>これらは、このノードによって変更され、再度出力として返されます。 |
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>曲線</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>Height</b> <i>グレースケール入力</i> |  |
| <b>標準</b> <i>カラー入力</i> |  |
| <b>頂点の色</b> <i>カラー入力</i> |  |
| <b>ワールド空間標準</b> <i>カラー入力</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 以下のパラメーターの可用性に影響します。 |
| <b>ベイク済みマップ</b> | 表示されたベイク済みマップを計算に使用するかどうか。 以下のパラメーターの可用性に影響します。 |
| <b>Diffuse AO</b> <i>0.0 - 1.0</i> | DiffuseにブレンドするAmbient occlusionの量。 |
| <b>Diffuseのシャープエッジ</b> <i>0.0 - 1.0</i> | 拡散にブレンドする曲率マップの量。 |
| <b>頂点色のDiffuse色</b> <i>0.0 - 1.0</i> | 拡散にブレンドする頂点カラーベイク処理の量。 |
| <b>Diffuseのプリライティング</b> <i>0.0 - 1.0</i> | ワールド空間法線に基づく（フェイク）プリライティングの量。 |
| <b>Diffuseアニメの照明バランス</b> <i>0.0 - 1.0</i> | 拡散反射光のリアリスティック照明と漫画照明の間で切り替えます。 |
| <b>Diffuseアニメのプリライティングレイヤー</b> <i>0 - 10</i> | カートゥーンライティングの計算の外観を制御します。 |
| <b>Diffuse漫画のアウトライン</b> <i>0.0 - 1.0</i> | カートゥーンライティングの計算の外観を制御します。 |
| <b>Base color AO</b> <i>0.0 - 1.0</i> | ベースカラーにブレンドするアンビエントオクルージョンの量。 |
| <b>Base colorのシャープなエッジ</b> <i>0.0 - 1.0</i> | ベースカラーにブレンドする曲率マップの量。 |
| <b>頂点の色からのBase color</b> <i>0.0 - 1.0</i> | ベースカラーにブレンドする頂点カラーベイク処理の量。 |
| <b>通常のマテリアルの強さ</b> <i>0.0 - 1.0</i> | ベイク処理された（接線）法線マップのブレンド強度。 |
| <b>鏡面反射光</b> <i>0.0 - 1.0</i> | Specularに対するAOのブレンド強度。 |
| <b>Specularの明るくシャープなエッジ</b> <i>0.0 - 1.0</i> | Specularの曲率のブレンド強度。 |
| <b>Specular漫画のアウトライン</b> <i>0.0 - 1.0</i> | 曲率に基づく、アニメSpecularのエッジからアウトラインへの効果のブレンド強度。 |
| <b>光沢度の濃いシャープなエッジ</b> <i>0.0 - 1.0</i> | 光沢における曲率のブレンド強度。 |
| <b>ラフネスの明るくシャープなエッジ</b> <i>0.0 - 1.0</i> | 粗さの曲率のブレンド強度。 |
| <b>ラフネスアニメのアウトライン</b> <i>0.0 - 1.0</i> | 曲率に基づいたカートゥーンの粗さエッジとアウトラインの効果のブレンド強度。 |
| <b>メタリックの明るくシャープなエッジ</b> <i>0.0 - 1.0</i> | メタリックの曲率のブレンド強度。 |
| <b>メタリックアニメのアウトライン</b> <i>0.0 - 1.0</i> | 曲率に基づいた、アニメのメタリックエッジのアウトラインエフェクトのブレンド強度。 |
| <b>AOマテリアルの適用度</b> <i>0.0 - 1.0</i> | ベイク済みマップAOとマテリアルのブレンド強度 – 生成されたAO、で両方のAOマップを結合する程度。 |
| <b>マテリアルの適用度</b> <i>0.0 - 1.0</i> | Heightの強度とマテリアルで生成されたHeightをブレンドし、両方のハイトマップをどの程度組み合わせるかを指定します。 |
| <b>マテリアルのブレンドの種類</b> <i>強化、補間</i> | 両方のハイトマップを組み合わせるための描画モード。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-mesh-data-blender.resources/material-mesh-data-blender-02.gif" />
        </td>
    </tr>
</table>
