---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-match.html"
breadcrumb-title: ''
description: カラーマッチノードを使用して、テクスチャ間で色を一致させ、一貫したカラーパレットを作成してテクスチャを調和させます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color Match
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラーマッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 029f702d9b6a4d0dfaa83a4ae8447c02f70be355
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# カラーマッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

定義された&#x200B;*ソースカラー*&#x200B;の範囲と&#x200B;*ターゲットカラー*&#x200B;の範囲の一致を試みます。ソースとターゲットを定義する入力スロットがサポートされます。

より単純なバージョンについては、[色の範囲の置き換え](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md)または[色の置き換え](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)を参照してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>カラー入力</i> | 結果を変更するメイン入力。 |
| <b>ソースカラー</b> <i>カラー入力</i> | ソースカラーの入力スロット。「ソースカラーモード」が&#x200B;*Input*&#x200B;に設定されている場合にのみ使用されます。 |
| <b>ターゲットの色</b> <i>カラー入力</i> | ターゲットカラーの入力スロットです。&#39;ターゲットカラーモード&#39;が&#x200B;*入力*&#x200B;に設定されている場合にのみ使用されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ソースカラーモード</b> <i>平均、パラメーター、入力</i> | ソースカラーを定義する方法（入力画像を平均化する、パラメータを設定する、入力スロットを使用する）を指定します。 |
| <b>ソースカラー</b> <i>（カラー値）</i> | ソースカラーモードが&#x200B;*パラメーター*&#x200B;に設定されている場合、このパラメーターによってソースカラーが決定されます。 |
| <b>ターゲットカラーモード</b> <i>パラメーター、画像入力</i> | ソースカラーを定義する方法（入力画像を平均化する、パラメータを設定する、入力スロットを使用する）を指定します。 |
| <b>ターゲットの色</b> <i>（カラー値）</i> | ターゲット色モードが&#x200B;*パラメーター*&#x200B;に設定されている場合、このパラメーターによってターゲット色が決定されます。 |
| <b>カスタムカラーバリエーション</b> <i>False/True</i> | 追加のカラーバリエーションを有効にします。 |
| <b>カラーバリエーション</b> | 色相、クロミナンスまたは輝度のバリエーションを有効にすると、結果に設定します。 |
| <b>マスクを使用</b> <i>False/True</i> | 以下のマスクモードに応じて、マスク入力または出力の使用を切り替えます。 |
| <b>マスクモード</b> <i>パラメーター、入力</i> | パラメーターモードでは、カラーがどのように変更されたかを詳細に示すマスクが出力されます。 入力モードを使用すると、マスクでカラーマッチングエフェクトの強度を制御できます。 |
| <b>マスク</b> | 「カラーマッチング」エフェクトが適用された場所を示すマスクを出力します。このマスクには、スムージングやぼかしを行うための追加コントロールがあります。 |
