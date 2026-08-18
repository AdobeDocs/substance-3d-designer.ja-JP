---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/multi-switch.html"
breadcrumb-title: ''
description: Multi Switchノードを使用すると、条件付きテクスチャ選択用のセレクターに基づいて、複数の入力テクスチャを切り替えることができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Multi Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチスイッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '152'
ht-degree: 2%

---


# マルチスイッチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-switch-greyscale.png){width="128px"}

![](../../../../../../assets/multi-switch.png){width="128px"}

## マルチスイッチ（グレースケール）

**イン：** *フィルター/描画*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

スイッチボックスとして機能し、&#39;Input Selection&#39;パラメーターで定義された入力のみを通過します。 したがって、2つの入力が接続されている場合、ユーザーの選択に応じて、そのうちの1つだけが返されます（変更されません）。

グラフに様々なオプションを追加する場合に非常に便利です。 [公開](../../../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) （ドロップダウンリストとして表示することが望ましい）と組み合わせると、多くのカスタマイズが可能です。

重要：入力に適したバージョンを使用してください。 カラー入力には「マルチスイッチ」、グレースケール入力には「マルチスイッチグレースケール」を使用します。

## パラメーター

### 入力

* **入力1-20**: *カラー入力*

### パラメーター

* **入力番号**: *2 - 20*&#x200B;公開する入力数。 重要：数を減らしても、接続を削除しないでください。
* **入力選択**: *1 - 20*&#x200B;結果として返される入力。

## サンプル画像

</td>
</tr>
</table>
