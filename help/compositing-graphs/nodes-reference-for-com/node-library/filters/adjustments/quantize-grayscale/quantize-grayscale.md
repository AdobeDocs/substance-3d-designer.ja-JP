---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
breadcrumb-title: ''
description: ポスタリゼーションエフェクトのグレースケールレベルの数を減らすには、クオンタイズグレースケールノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Quantize Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グレースケールの量子化
user-guide-description: ''
user-guide-title: ''
source-git-commit: fca95f162552b0e651c7b590588b69c2c5f5a0c4
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 1%

---


# グレースケールの量子化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![グレースケールのクオンタイズアイコン](quantize-grayscale.resources/quantize-grayscale.png "グレースケールのクオンタイズアイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

円のシェイプの単一のスプラインを生成します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>手順</b> *整数* | 入力範囲を近似する個別の値の数です。 |
| <b>オフセット</b> *フロート* | 入力範囲にオフセットを適用します。このオフセットは、範囲に沿って結果を&#x200B;*シフト*&#x200B;します。 |
| <b>勾配</b> *フロート* | ステップの&#x200B;*フルスパン*&#x200B;までの近似値の間の&#x200B;*トランジション*&#x200B;に勾配グラデーションを適用します。 |
| <b>勾配曲線</b> *整数* | <b>勾配</b>パラメーターで設定された勾配のカーブの取得方法を設定します：<ul data-preserve-html="true"> <li data-preserve-html="true">*直線*：直線の曲線を適用し、直線の勾配を作成します</li> <li data-preserve-html="true">*スムーズ化*:スムーズ化された曲線を適用し、勾配を滑らかにします</li> <li data-preserve-html="true">*曲線入力*: <b>曲線入力</b>入力マップで記述された曲線を適用します。 [曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)ノードを使用すると、この曲線を詳細に表現できます。</li> </ul> |

## 例

![例1](quantize-grayscale.resources/quantizegrayscale.gif "例1")

![例2](quantize-grayscale.resources/quantizegrayscale.png "例2")
