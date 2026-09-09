---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: ambient occlusion(RTAO)ノードを使用して、リアルなシェーディングを行うために高さマップからリアルタイムambient occlusionマップを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Ambient occlusion(RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 132a27ad47b0272a877b913eaa7957ccf8b549fd
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# Ambient occlusion(RTAO)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RTAOノードアイコン](ambient-occlusion-rtao.resources/rt-ao.png "RTAOノードアイコン")

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高さマップ入力に基づいてAmbient occlusionマップを生成します。

このフィルターは、HBAOと比較してより正確な結果が得られますが、計算時間があるため、CPU(SSE)エンジンと組み合わせて使用しないでください。

[Ambient occlusion (HBAO) (フィルターノード)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md)を参照して、より高速で単純な代替手段を使用してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>物理サイズを使用</b> <i>ブーリアン</i> | 切り替えると、物理サイズ設定を使用してHeightスケールを指定できます。 |
| <b>物理サイズ</b> <i>浮動小数3</i> <i>（<b>物理サイズを使用</b>が<i>真</i>に設定されている場合に利用可能）</i> | サーフェスの実際の物理サイズに基づいてHeightスケールを調整します |
| <b>サンプル</b> <i>整数</i> | ambient occlusionの計算に使用されるレイの数です。<br>値を大きくすると、パフォーマンスが低下しますが、より滑らかで正確な結果が得られます。 |
| <b>Heightスケール</b> <i>浮動小数</i> <i>（<b>物理サイズを使用</b>が<i>偽</i>に設定されている場合に利用可能）</i> | 高さマップ入力の強度の乗数。 |
| <b>配布</b> <i>整数</i> | 分布方法を設定します。 影の領域に向かって減衰します。 |
| <b>最大距離</b> <i>浮動小数</i> | 光線が遮断される最大距離を設定します。 |
| <b>広がり角度</b> <i>浮動小数</i> | 光線を照射する広がり角度を設定します。 値1は半球全体です。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-7-48.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="ambient-occlusion-rtao.resources/image2021-6-18-11-9-0-1.png" />
        </td>
    </tr>
</table>
