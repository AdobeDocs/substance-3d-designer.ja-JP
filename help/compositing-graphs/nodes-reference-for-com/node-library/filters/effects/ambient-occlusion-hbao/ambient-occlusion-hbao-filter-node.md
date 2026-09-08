---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-hbao-filter-node.html"
breadcrumb-title: ''
description: '[環境オクルージョンHBAO]フィルタノードを使用すると、地平線ベースのアルゴリズムを使用して環境オクルージョンマップを作成し、リアルなシェーディングを実現できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (HBAO) (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境オクルージョン(HBAO)（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 5%

---


# 環境オクルージョン(HBAO)（フィルタノード）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/hbao.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Heightmapを入力として取り、その値から環境オクルージョンマップを生成します。 これは、元々スクリーン空間でリアルタイムにAOを生成することを目的としたオクルージョンであるHorizon-Based Ambient Algorithmを使用しています。 手続き型Heightmapsから手続き型AOマップを作成する場合に非常に便利です。

より高度で低速なAOの別のバージョンについては、[環境オクルージョン(RTO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)を参照してください

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ワールドユニットを使用</b> <i>False/True</i> | ワールド単位またはシーンスペース単位の使用を切り替えます。 より正確な制御を可能にする追加のパラメーターを有効にします。 |
| <b>深度</b> <i>0.0 - 1.0</i> | ワールド単位がFalseに設定されている場合にのみ使用されます。 グローバルなスケーリングを制御します。 |
| <b>表面のサイズ</b> <i>0.0 - 1000.0</i> | ワールド単位がTrueに設定されている場合にのみ使用されます。 グローバルなスケーリングを制御します。 |
| <b>Heightスケール(cm)</b> <i>0.0 - 1000.0</i> | ワールド単位がTrueに設定されている場合にのみ使用されます。 グローバルなスケーリングを制御します。 |
| <b>半径</b> <i>0.0 - 1.0</i> | AOの広がりを制御します。 |
| <b>クォリティ</b> <i>4サンプル、8サンプル、16サンプル</i> | 計算に使用するサンプルの量を決定して品質レベルを設定します。 |
| <b>GPU最適化</b> <i>False/True</i> | 内部GPU最適化を有効にして、処理を高速化します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-11-1.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/image2021-6-18-11-11-22.png" />
        </td>
    </tr>
</table>
