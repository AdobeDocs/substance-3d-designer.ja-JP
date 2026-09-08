---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-to-height.html"
breadcrumb-title: ''
description: '[法線からHeight]ノードを使用して、サーフェスの深度情報を抽出するために法線マップをHeightマップに変換します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal to Height
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Heightに垂直
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '184'
ht-degree: 3%

---


# Heightに垂直

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/normal-to-height.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

接線空間の法線マップを再び高さマップに変換しようとする逆変換ノード。 これは少しシンプルなバージョンです。[Height本部への通常](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-to-height-hq/normal-to-height-hq.md)には、他のオプションがあります。

ノーマルマップソースしかなくても、ハイトマップと組み合わせて操作を実行したい場合に便利です。 Heightを通常に変換すると情報が失われるため、100%正しい結果を得ることはできないことに注意してください。 必要に応じて設定を調整すると、この非HQバージョンでは単純なディテールを適切に変換できます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>リリーフ残高</b> <i>0.0 - 1.0</i> | 異なる周波数が最終結果に影響する範囲を調整します。 これは入力マップに大きく依存し、かなりの微調整が必要です。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>グローバル不透明度</b> <i>0.0 - 1.0</i> | エフェクトの不透明度をグローバルに調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/normal2heightex.png" />
        </td>
    </tr>
</table>
