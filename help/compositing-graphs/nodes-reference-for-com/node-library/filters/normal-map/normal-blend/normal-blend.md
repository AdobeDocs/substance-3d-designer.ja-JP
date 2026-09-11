---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: 法線ブレンドノードを使用して法線マップをブレンドし、サーフェスのディテール間の滑らかな変化を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 標準ブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 67f8f59bf50387b87e9009b042f269208c665c65
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 3%

---


# 標準ブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](normal-blend.resources/normal-blend.png){width="128px"}

<b>イン：</b>フィルター> 法線マップ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

「法線ブレンド」を使用すると、すべての値を正規化した状態に保ちながら、2つの法線マップをオプションのマスクとブレンドできます。 [アトミックブレンドノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)とほとんど変わりませんが、ノーマルマップの内部計算が追加されました。

法線ブレンドは、法線マップを結合（オーバーレイ）するためのものではありません。法線マップでは、上のマップが下のマップに詳細を追加します。 その場合は、代わりに[通常の結合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md)を使用します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>NormalFG</b> <i>カラー入力</i> | 前景/上法線マップ： |
| <b>NormalBG</b> <i>カラー入力</i> | 背景/下部の法線マップ： |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスクを使用」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>マスクを使用</b> <i>False/True</i> | マスクマップの使用のオン/オフを切り替えます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="normal-blend.resources/normalblend-ex.gif" /><br><i>（.gif形式はディザリングを導入しています。アプリケーション内の結果はスムーズです）</i>
        </td>
    </tr>
</table>
