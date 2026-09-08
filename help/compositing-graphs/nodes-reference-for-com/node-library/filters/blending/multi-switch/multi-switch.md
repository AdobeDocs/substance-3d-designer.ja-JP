---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Multi Switchノードを使用すると、条件付きテクスチャ選択用のセレクターに基づいて複数の入力テクスチャを切り替えることができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチスイッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: f25074f2fc4bb66ad781ad2510fdf43ba8aaae69
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 4%

---


# マルチスイッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

<b>イン:</b>フィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

スイッチボックスとして機能し、&#39;Input Selection&#39;パラメーターで定義された入力のみを通過します。 したがって、2つの入力が接続されている場合、ユーザーの選択に応じて、そのうちの1つだけが返されます（変更されません）。

グラフに様々なオプションを追加する場合に非常に便利です。 [表示](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) （ドロップダウンリストとして推奨）と組み合わせると、多くのカスタマイズが可能です。

重要：入力に適したバージョンを使用してください。 カラー入力には「マルチスイッチ」、グレースケール入力には「マルチスイッチグレースケール」を使用します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力1-20</b> <i>カラー入力</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>入力番号</b> <i>2 - 20</i> | 表示する入力の量。 重要：数を減らしても、接続を削除しないでください。 |
| <b>選択範囲の入力</b> <i>1 - 20</i> | 結果として返す入力です。 |
