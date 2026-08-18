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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '300'
ht-degree: 1%

---


# カラーマッチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-match-3.png){width="128px"}

## カラーマッチ

**イン：** *フィルター/調整*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

定義された&#x200B;*ソースカラー*&#x200B;の範囲と&#x200B;*ターゲットカラー*&#x200B;の範囲の一致を試みます。ソースとターゲットを定義する入力スロットがサポートされます。

より単純なバージョンについては、[色の範囲の置き換え](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color-range/replace-color-range.md)または[色の置き換え](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/replace-color/replace-color.md)を参照してください。

## パラメーター

### 入力

* **入力**: *色*&#x200B;入力\
  結果を変更するメイン入力。
* **ソースカラー**: *カラー入力*\
  ソースカラーの入力スロット。「ソースカラーモード」が&#x200B;*Input*&#x200B;に設定されている場合にのみ使用されます。
* **ターゲットの色**: *色の入力*&#x200B;ターゲットの色の入力スロットです。&#39;ターゲットの色モード&#39;が&#x200B;*入力*&#x200B;に設定されている場合にのみ使用されます。

### パラメーター

* **ソースカラーモード**: *平均、パラメータ、入力*&#x200B;入力画像の平均、パラメータの設定、または入力スロットを使用して、ソースカラーを定義するかどうかを設定します。
* **ソースカラー**: *（カラー値）*&#x200B;ソースカラーモードが*パラメーター*に設定されている場合、このパラメーターがソースカラーを決定します。
* **ターゲットカラーモード**: *パラメータ、イメージ入力*&#x200B;ソースカラーを定義する方法（入力イメージの平均、パラメータの設定、入力スロットの使用）を指定します。
* **ターゲットの色**: *（色の値）*&#x200B;ターゲットの色モードが*パラメーター*に設定されている場合、このパラメーターがターゲットの色を決定します。
* **カスタムカラーバリエーション**: False/True\
  追加のカラーバリエーションを有効にします。
* **カラーバリエーション**\
  色相、クロミナンスまたは輝度のバリエーションを有効にすると、結果に設定します。
* **マスクを使用**: *False/True*\
  以下のマスクモードに応じて、マスク入力または出力の使用を切り替えます。
* **マスクモード**: *パラメーター、入力*&#x200B;パラメーターのモードでは、色がどのように変更されたかを詳細に示すマスクが出力されます。 入力モードを使用すると、マスクでカラーマッチングエフェクトの強度を制御できます。
* **マスク**\
  「カラーマッチング」エフェクトが適用された場所を示すマスクを出力します。このマスクには、スムージングやぼかしを行うための追加コントロールがあります。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
