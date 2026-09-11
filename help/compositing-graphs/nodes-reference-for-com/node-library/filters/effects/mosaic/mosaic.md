---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/mosaic.html"
breadcrumb-title: ''
description: モザイクノードを使用して、テクスチャをピクセル化されたブロックとパターンに分割することで、モザイク状のタイル効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Mosaic
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: モザイク
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 7%

---


# モザイク

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](mosaic.resources/mosaic-1.png){width="128px"}

![](mosaic.resources/mosaic-grayscale.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

マルチパス[ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/warp/warp.md)効果を実行して、既存の滑らかな傾斜したグラデーションマップを「多面的に」します。 両方の入力に同じマップを使用すると、基本的に明るい領域が大きくなり、強調されます。

これは、Heightmapなどのグレースケールマップに多くの定義を追加する場合に便利です。シェイプにさらなる定義を加えることができます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>色</b> <i>カラー/グレースケール入力</i> |  |
| <b>モザイク地図</b> <i>グレースケール入力</i> | ワープドライバーマップ。 最初の入力と同じにすることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>サンプル</b> <i>0 - 16</i> | マルチサンプルの画質を指定します。 |
| <b>適用度</b> <i>0.0 - 1.0</i> | 効果の強さ。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="mosaic.resources/mosaci-ex.png" />
        </td>
    </tr>
</table>
