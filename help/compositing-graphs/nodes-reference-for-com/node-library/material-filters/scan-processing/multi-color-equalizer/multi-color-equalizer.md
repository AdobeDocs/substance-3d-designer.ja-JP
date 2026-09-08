---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
breadcrumb-title: ''
description: マルチColor Equalizerノードを使用して、複数のテクスチャチャンネルにわたってカラーを平均化し、スキャンされたマテリアルを一貫して処理できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチColor Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 1%

---


# マルチColor Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer-multi.png){width="128px"}

## マルチColor Equalizer

**イン：** *マテリアルフィルター/スキャン処理*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)の複数入力バージョンです。 これにより、カラーの違いが強調され、ユーザーが選択した倍率で不要な色合いが除去されます。 主に、マルチアングルの写真での使用が意図されています。この写真を[マルチアングルからアルベド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)または[マルチアングルから標準](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)と組み合わせます。

>[!NOTE]
>
> 詳細については、元の[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)を参照してください。

## パラメーター

### 入力

* **入力1-8**: *カラー入力*&#x200B;処理に対する複数の入力。
* **マスク入力**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **入力数**: *1 ～ 8*&#x200B;並列に処理する入力数を設定します。
* **タイルされた入力**: *偽/真*&#x200B;オプションでエッジのタイリングを保持します。
* **半径**: *0.0 ～ 50.0*&#x200B;等化半径を設定します。 半径を大きくすると、カラーの差が大きくなるだけです。 これには、すべての画像に対して微調整が必要です。
* **明るい/暗いバランス**: *0.0 ～ 1.0*&#x200B;暗い色合いを残したり取り除いたりするためのバイアス設定。
* **カスタムカラーバリエーション**: *偽/真*&#x200B;ユーザーが指定した色に向かって効果を変化させることができます。
* **カラーバリエーション**\
  カスタムカラーバリエーションが有効になっている場合にのみアクティブです。 設定では、均等化の対象とする濃淡オフセットを選択できます。
  * **色相**: *0.0 - 360.0*
  * **クロマ**: *0.0 - 1.0*
  * **ルミナンス**: *0.0 ～ 1.0*
* **マスクソース**: *なし、画像の平均、色パラメーター、入力*&#x200B;マスクを実行するかどうかを設定します。 カラーパラメーターを使用すると、以下の追加設定が可能になります。入力はユーザー定義のマスク入力に切り替わります。
* **マスク**\
  カラーパラメーターマスクでのみアクティブです。 画像自体に基づいてマスクを決定する追加のマスクパラメーターが含まれています。 次のパラメーターを使用すると、イコライゼーションを適用するバイナリマスクに濃淡を正確に変換できます。 これらの設定を使用すると、半径パラメーターの効果がずっと目立たなくなることに注意してください。
  * **色**: *（色値）*
  * **色相範囲**: *0.0 ～ 360.0*
  * **クロマ範囲**: *0.0 ～ 1.0*
  * **ルミナンス範囲**: *0.0 ～ 1.0*
  * **ぼかし**: *0.0 ～ 2.0*
  * **Smoothness**: *0.0 ～ 2.0*

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
