---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/shape-glow.html"
breadcrumb-title: ''
description: シェイプグローノードを使用して、光彩の効果をシェイプやテクスチャに加え、明るく大気のような視覚効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Shape Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Shape Glow
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 4%

---


# Shape Glow

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-glow.resources/shape-glow-grayscale.png){width="128px"}

![](shape-glow.resources/shape-glow.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力マスクの周囲にソフトな光彩を作成するか（グレースケールの場合）、アルファチャンネル付きのシェイプの周囲にソフトな光彩を作成します（カラーの場合）。 [光彩](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/glow/glow.md)と比較すると、この効果は他の2D画像編集ソフトウェアにより似た方法で機能します。これは、より多くのコントロールを備えたより完全な効果です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>モード</b> <i>ソフト、精細</i> | 2つの精度モードを切り替えます。 |
| <b>幅</b> <i>-1.0 - 1.0</i> | グローが届く範囲を制御します。 |
| <b>スプレッド</b> <i>0.0 - 1.0</i> | ぼかし効果のカットオフ/しきい値を設定すると、光彩がシェイプに近い単色になります。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 光彩効果のブレンドの不透明度。 |
| <b> （シャドウ）カラー</b> <i>（カラー値）</i> | 光彩に適用される色かぶり。 |
| <b>マスクの色</b> <i>（カラー値） （グレースケールバージョンのみ）</i> | 透明マップ出力に使用される単色。 |
| <b>入力は事前に乗算されています</b> <i>False/True （カラーバージョンのみ）</i> | 入力を事前に乗算されたものと見なすかどうかを指定します。 |
| <b>乗算前出力</b> <i>False/True</i> | 出力を事前に乗算するかどうかを指定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-glow.resources/shapeglow-ex.png" />
        </td>
    </tr>
</table>
