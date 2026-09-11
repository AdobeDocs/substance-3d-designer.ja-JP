---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-to-gradient.html"
breadcrumb-title: ''
description: 「Flood Fillからグラデーションへ」ノードを使用すると、滑らかなカラー効果を作成するために、領域をグラデーション値で塗りつぶすことができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill to Gradient
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fillからグラデーション
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '206'
ht-degree: 7%

---


# Flood Fillからグラデーション

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](flood-fill-to-gradient.resources/floodfill-to-gradient.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)のベースを（ランダムな方向の）グラデーションに変形します。 タイルがランダムに傾いたり傾斜したりしているハイトマップを作成するのに非常に便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Flood Fill</b> <i>カラー入力</i> | 基本Flood Fillデータ。 |
| <b>角度入力</b> <i>グレースケール入力</i> | 外部マップを使用してセルごとの角度を決定するオプションマップ。 |
| <b>勾配入力</b> <i>グレースケール入力</i> | セルごとのグラデーションの強さを決定するオプションのマップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>角度</b> <i>0.0 - 1.0</i> | すべてのタイルに対して均等なグローバル角度/方向を設定します。 |
| <b>角度のバリエーション</b> <i>0.0 - 1.0</i> | 各タイルの角度を個別にランダム化します。 これは最も便利で強力なパラメーターです。 |
| <b>バウンディングボックスのサイズで乗算</b> <i>0.0 - 1.0</i> | タイルの個々のバウンディングボックスサイズに合わせて、線形効果全体のサイズを調整します。 つまり、小さなタイルは大きなタイルよりも暗くなります。 |
| <b>角度画像入力乗数</b> <i>0.0 - 1.0</i> | 生成されるグラデーション方向に対するオプションの角度入力マップの影響を設定 |
| <b>勾配イメージ入力マルチプライヤ</b> <i>0.0 - 1.0</i> | 生成されるグラデーションの勾配強度に対する、オプションの勾配入力マップの影響を設定します。 |
| <b>勾配の適用度で乗算</b> <i>0.0 - 1.0</i> |  |
| <b>平坦な勾配の色</b> <i>（グレースケール値）</i> | フラット勾配のソリッド値を設定できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex2.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="flood-fill-to-gradient.resources/floodgradient-ex1.png" />
        </td>
    </tr>
</table>
