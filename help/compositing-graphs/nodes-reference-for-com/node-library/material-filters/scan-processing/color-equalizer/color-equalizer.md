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
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 6%

---


# Color Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](color-equalizer.resources/color-equalizer.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、色の違いについて高品質の[ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)のように機能します。 通常のハイパスでは、彩度が下がり、不要なシャープが追加される場合がありますが、Color Equalizerでは、カラー差を補正し、ユーザーが選択したスケールで不要な色合いを除去します。

これは、写真やスキャンに不要なカラーの違いがある場合や、除去したい色合いがある場合に非常に便利です。 [ハイパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/highpass/highpass.md)を使用した場合、このノードは使い慣れた感じになるはずです。

マスクオプションは、非常に特定の色合いを削除したり、特定の値の範囲でのみ操作したりすることを目的としています。 効果の範囲が広すぎると感じる場合は、これらを使用してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>カラー入力</i> |  |
| <b>マスク入力</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 マスクが「入力」に設定されている場合にのみアクティブになります。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>タイルされた入力</b> <i>False/True</i> | 必要に応じて、エッジのタイリングを保持します。 |
| <b>半径</b> <i>0.0 - 50.0</i> | イコライズ半径を設定します。 半径を大きくすると、カラーの差が大きくなるだけです。 これには、すべての画像に対して微調整が必要です。 |
| <b>明るい/暗いバランス</b> <i>0.0 - 1.0</i> | 暗い色合いを残したり取り除いたりするためのバイアス設定。 |
| <b>カスタムカラーバリエーション</b> <i>False/True</i> | 効果をユーザー指定の色に向かって変化させることができます。 |
| <b>カラーバリエーション</b> | カスタムカラーバリエーションが有効になっている場合にのみアクティブです。 設定では、均等化の対象とする濃淡オフセットを選択できます。 |
| <b>色相</b> <i>0.0 - 360.0</i> |  |
| <b>彩度</b> <i>0.0 - 1.0</i> |  |
| <b>ルミナンス</b> <i>0.0 - 1.0</i> |  |
| <b>マスクソース</b> <i>なし、画像平均、色パラメーター、入力</i> | 任意の種類のマスクを実行するかどうかを設定します。 カラーパラメーターを使用すると、次の追加設定が有効になり、入力はユーザー定義のマスク入力に切り替わります。 |
| <b>マスク</b> | これは、カラーパラメーターマスクでのみアクティブです。 画像自体に基づいてマスクを決定する追加のマスクパラメーター。 次のパラメーターを使用すると、イコライゼーションを適用したバイナリマスクに濃淡を正確に変換できます。 これらの設定を使用すると、半径パラメーターの効果がずっと目立たなくなることに注意してください。 |
| <b>色</b> <i>（カラー値）</i> |  |
| <b>色相範囲</b> <i>0.0 - 360.0</i> |  |
| <b>クロマ範囲</b> <i>0.0 - 1.0</i> |  |
| <b>ルミナンス範囲</b> <i>0.0 - 1.0</i> |  |
| <b>ぼかし</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
