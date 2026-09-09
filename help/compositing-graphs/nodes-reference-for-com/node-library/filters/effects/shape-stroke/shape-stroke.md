---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-stroke.html"
breadcrumb-title: ''
description: シェイプの線ノードを使用して、線のアウトラインをシェイプに追加し、境界線やエッジ効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Stroke
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプの線
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 4%

---


# シェイプの線

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-stroke.resources/shape-stroke.png){width="128px"}

![](shape-stroke.resources/shape-stroke-grayscale.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

他の2D画像編集アプリケーションで使い慣れている黒と白のマスク（グレースケール版の場合）またはアルファチャンネル付きシェイプ（カラー版の場合）の周囲に、線やアウトラインを追加します。 [エッジ検出](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/edge-detect/edge-detect.md)のより完全なバージョンと見なすことができます。

様々な画像編集効果に非常に便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>幅</b> <i>-1.0 - 1.0</i> | 線の幅です。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | エフェクトのグローバル不透明度。 |
| <b> （アウトライン）カラー</b> <i>（カラー値）</i> | アウトライン効果に使用する色です。 |
| <b>マスクの色</b> <i>（カラー値） （グレースケールバージョンのみ）</i> | 透明マップ出力に使用される単色。 |
| <b>入力は事前に乗算されています</b> <i>False/True （カラーバージョンのみ）</i> | 入力を事前に乗算されたものと見なすかどうかを指定します。 |
| <b>乗算前出力</b> <i>False/True</i> | 出力を事前に乗算するかどうかを指定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-stroke.resources/shapestroke-ex.png" />
        </td>
    </tr>
</table>
