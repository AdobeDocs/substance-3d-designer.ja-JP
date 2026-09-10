---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/3d-planar-projection.html"
breadcrumb-title: ''
description: 3D投影ノードを使用すると、テクスチャマッピング用の平面投影を使用して、テクスチャをメッシュサーフェスに投影できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > 3D Planar Projection
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D投影
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 7%

---


# 3D投影

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-planar-projection.resources/3d-planar-gray.png)![](3d-planar-projection.resources/3d-planar.png)

<b>In:</b> メッシュベースのジェネレータ>ユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイクされたメッシュデータ（位置とワールド法線マップ）に基づいて平面投影を実行します。 元のUVマッピングに関係なく、シーム間でデカールを投影して配置できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>位置マップ</b> <i>カラー入力</i> | ベイク位置マップ |
| <b>ワールド空間法線</b> <i>カラー入力</i> | ワールド空間法線マップ |
| <b>予測されるテクスチャ</b> <i>カラー入力</i> | ターゲットに投影するテクスチャを入力します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>配置</b> |  |
| <b>プロジェクト入力</b> <i>UVポジション、ワールド空間ポジション</i> | 投影位置を2D / UVにするか、3D / ワールド空間にするかを選択します。 |
| <b>ターゲットUVポジション</b> | UV位置入力のみで、位置マップ上の2D ビューの点を選択するのに最適です。 |
| <b>ターゲットの位置</b> <i>（カラー値）</i> | ワールド空間位置入力でのみ、正確な3D座標を定義できます。 |
| <b>ターゲット法線</b> <i>（カラー値）</i> |  |
| <b>回転</b> <i>0.0 - 1.0</i> | 投影されたテクスチャを法線軸に沿って回転させます。 |
| <b>スケール</b> <i>0.0 - 1.0</i> | 投影されるテクスチャのグローバルスケールを設定します。 |
| <b>サイズ</b> <i>0.0 - 2.0</i> | 投影されたテクスチャに対して不均等スケーリングを実行します。 |
| <b>マスク</b> |  |
| <b>最大深度</b> <i>0.0 - 1.0</i> | 投影されたテクスチャがカットオフされるときの深さを制御します。 |
| <b>フェード</b> <i>0.0 - 1.0</i> | カットオフ深度の変化を急な場合や色あせた場合に設定します。 |
| <b>標準しきい値</b> <i>-1.0 - 1.0</i> | 投影法線と正確に位置合わせされていないサーフェスのスレッショルドを設定します。 |
| <b>通常のフェード</b> <i>0.0 - 1.0</i> | サーフェスが突然またはフェードに位置揃えされていない場合は、トランジションを設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-planar-projection.resources/3d-planar-projection-ex.gif" />
        </td>
    </tr>
</table>
