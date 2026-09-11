---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: '[曲げ法線]ノードを使用して、ambient occlusionおよび間接照明を考慮した曲げ法線マップを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線を曲げる
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '249'
ht-degree: 2%

---


# 法線を曲げる

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![曲がった法線ノードアイコン](bent-normal.resources/rt-bent-normal.png "曲がった法線ノードアイコン")

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高さマップ入力に基づいて曲げ法線マップを生成します。 曲がった法線マップは、[通常](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)および[Ambient occlusion(RTAO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)の特殊なバージョンで、ambient occlusionが埋め込まれた法線マップを生成します。\
これをリアルタイムエンジンで使用して、Ambient occlusionをノーマルマップにベイクし、例えば金属のより正確なオクルージョン反射を実現できます。

計算時間が長いため、このノードをCPU(SSE)エンジンと組み合わせて使用しないでください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>物理サイズを使用</b> <i>ブール値</i> | 切り替えると、物理サイズ設定を使用してHeightスケールを指定できます。 |
| <b>物理サイズ</b> <i>浮動小数点3</i> | （<b>物理サイズを使用</b>が<i>真</i>に設定されている場合に使用可能）サーフェスの実際の物理サイズに基づいてHeightスケールを調整します。 |
| <b>サンプル</b> <i>整数</i> | 曲がった法線の計算に使用される光線の数。<br>高い値を指定すると、パフォーマンスが低下しますが、よりスムーズで正確な結果が得られます。 |
| <b>Heightスケール</b> <i>フロート</i> | （[物理サイズを使用]が[いいえ]に設定されている場合に使用可能）高さマップ入力の強度の乗数。 |
| <b>配布</b> <i>整数</i> | 分布方法を設定します。 影の領域に向かって減衰します。 |
| <b>最大距離</b> <i>フロート</i> | 光線が遮断される最大距離を設定します。 |
| <b>広がり角度</b> <i>フロート</i> | 光線を照射する広がり角度を設定します。 値1は半球全体です。 |
| <b>標準の形式</b> <i>整数</i> | 出力のグリーンチャンネルを反転します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bent-normal.resources/bent-normal-ex-1.jpg" />
        </td>
    </tr>
</table>
