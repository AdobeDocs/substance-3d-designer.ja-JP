---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/color-equalizer.html"
breadcrumb-title: ''
description: Color Equalizerノードを使用して、スキャンしたマテリアルのカラーのバリエーションのバランスを取り、テクスチャの見た目を統一します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Color Equalizer
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Color Equalizer
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 1%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/color-equalizer.png){width="128px"}

## Color Equalizer

**イン：** *マテリアルフィルター/スキャン処理*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、色の違いについて高品質の[ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)のように機能します。 通常のハイパスでは、彩度が下がり、不要なシャープが追加される場合がありますが、Color Equalizerでは、カラー差を補正し、ユーザーが選択したスケールで不要な色合いを除去します。

これは、写真やスキャンに不要なカラーの違いがある場合や、除去したい色合いがある場合に非常に便利です。 [ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)を使用した場合、このノードは使い慣れた感じになるはずです。

マスクオプションは、非常に特定の色合いを削除したり、特定の値の範囲でのみ操作したりすることを目的としています。 効果の範囲が広すぎると感じる場合は、これらを使用してください。

## パラメーター

### 入力

* **入力**: *カラー入力*
* **マスク入力**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。 マスクが「入力」に設定されている場合にのみアクティブになります。

### パラメーター

* **タイルされた入力**: *偽/真*&#x200B;オプションでエッジのタイリングを保持します。
* **半径**: *0.0 ～ 50.0*&#x200B;等化半径を設定します。 半径を大きくすると、カラーの差が大きくなるだけです。 これには、すべての画像に対して微調整が必要です。
* **明るい/暗いバランス**: *0.0 ～ 1.0*&#x200B;暗い色合いを残したり取り除いたりするためのバイアス設定。
* **カスタムカラーバリエーション**: *偽/真*&#x200B;ユーザーが指定したカラーにエフェクトを変化させることができます。
* **カラーバリエーション**\
  カスタムカラーバリエーションが有効になっている場合にのみアクティブです。 設定では、均等化の対象とする濃淡オフセットを選択できます。
  * **色相**: *0.0 - 360.0*
  * **クロマ**: *0.0 - 1.0*
  * **ルミナンス**: *0.0 ～ 1.0*
* **マスクソース**: *なし、画像の平均、色パラメーター、入力*&#x200B;何らかの種類のマスクを実行するかどうかを設定します。 カラーパラメーターを使用すると、次の追加設定が有効になり、入力はユーザー定義のマスク入力に切り替わります。
* **マスク**\
  これは、カラーパラメーターマスクでのみアクティブです。 画像自体に基づいてマスクを決定する追加のマスクパラメーター。 次のパラメーターを使用すると、イコライゼーションを適用したバイナリマスクに濃淡を正確に変換できます。 これらの設定を使用すると、半径パラメーターの効果がずっと目立たなくなることに注意してください。
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
