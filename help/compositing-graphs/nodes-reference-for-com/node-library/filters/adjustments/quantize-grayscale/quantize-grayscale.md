---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/quantize-grayscale.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 1%

---


# グレースケールの量子化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![グレースケールのクオンタイズアイコン](../../../../../../assets/quantize-grayscale.png "グレースケールのクオンタイズアイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

円のシェイプの単一のスプラインを生成します。

</td>
</tr>
</table>

## パラメーター

<b>手順</b> *整数*&#x200B;入力範囲に近似する個別の値の数です。

<b>オフセット</b> *浮動小数*&#x200B;入力範囲にオフセットを適用します。このオフセットは、範囲に沿って結果を&#x200B;*シフト*&#x200B;します。

<b>勾配</b> *浮動小数*&#x200B;近似値の間の&#x200B;*トランジション*&#x200B;に対して、ステップの&#x200B;*フルスパン*&#x200B;までの勾配グラデーションを適用します。

<b>勾配曲線</b> *整数*<b>勾配</b>パラメーターで設定された勾配のカーブの取得方法を設定します：
* *直線*：直線の曲線を適用し、直線の勾配を作成します
* *スムーズ化*:スムーズ化された曲線を適用し、勾配を滑らかにします
* *カーブ入力*: <b>カーブ入力</b> 入力マップで記述されたカーブを適用します。 [曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)ノードを使用すると、この曲線を詳細に表現できます。

## 例

![例1](../../../../../../assets/quantizegrayscale.gif "例1")

![例2](../../../../../../assets/quantizegrayscale.png "例2")
