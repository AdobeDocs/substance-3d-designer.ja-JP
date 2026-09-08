---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blending/switch.html"
breadcrumb-title: ''
description: 「切り替え」ノードを使用して、条件付きテクスチャ選択用のマスクに基づいて2つの入力テクスチャを切り替えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blending > Switch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スイッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 4%

---


# スイッチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/switch-1.png){width="128px"}

![](../../../../../../assets/switch-grayscale.png){width="128px"}

## 切り替え（グレースケール）

**イン：** *フィルター/描画*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

単純な2位置スイッチノードです。 Switchパラメーターの設定に基づいて、入力1または入力2を返します。 結果は変更されません。 詳細なバージョンについては、[マルチスイッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)を参照してください。

グラフでブール値(True/False)の選択を表示する場合に非常に便利です。この場合、ボタンは1つだけで済み、オプションの選択範囲全体に対する複雑なドロップダウンリストは必要ありません。

重要：入力に適したバージョンを使用してください。 カラー入力には「切り替え」、グレースケール入力には「グレースケールを切り替え」を使用します。

## パラメーター

### 入力

* **入力1 (True)**: *カラーまたはグレースケールの入力*
* **入力2 (False)**: *カラーまたはグレースケールの入力*

### パラメーター

* **スイッチ**: *False/True*&#x200B;入力1 (True)と2 (False)を切り替えます。

## サンプル画像

</td>
</tr>
</table>
