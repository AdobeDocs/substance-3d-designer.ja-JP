---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-color-equalizer.html"
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
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 7%

---


# マルチColor Equalizer

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-color-equalizer.resources/color-equalizer-multi.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)の複数入力バージョンです。 これにより、カラーの違いが強調され、ユーザーが選択した倍率で不要な色合いが除去されます。 主に、マルチアングルの写真での使用が意図されています。この写真を[マルチアングルからアルベド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)または[マルチアングルから標準](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)と組み合わせます。

>[!NOTE]
>
> 詳細については、元の[Color Equalizer](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/color-equalizer/color-equalizer.md)を参照してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力1-8</b> <i>カラー入力</i> | 処理への複数の入力。 |
| <b>マスク入力</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>入力数</b> <i>1 - 8</i> | 並列処理する入力数を設定します。 |
| <b>タイルされた入力</b> <i>False/True</i> | 必要に応じて、エッジのタイリングを保持します。 |
| <b>半径</b> <i>0.0 - 50.0</i> | イコライズ半径を設定します。 半径を大きくすると、カラーの差が大きくなるだけです。 これには、すべての画像に対して微調整が必要です。 |
| <b>明るい/暗いバランス</b> <i>0.0 - 1.0</i> | 暗い色合いを残したり取り除いたりするためのバイアス設定。 |
| <b>カスタムカラーバリエーション</b> <i>False/True</i> | 効果をユーザー指定のカラーに向かって変化させることができます。 |
| <b>カラーバリエーション</b> | カスタムカラーバリエーションが有効になっている場合にのみアクティブです。 設定では、均等化の対象とする濃淡オフセットを選択できます。 |
| <b>色相</b> <i>0.0 - 360.0</i> |  |
| <b>彩度</b> <i>0.0 - 1.0</i> |  |
| <b>ルミナンス</b> <i>0.0 - 1.0</i> |  |
| <b>マスクソース</b> <i>なし、画像平均、色パラメーター、入力</i> | マスキングを実行するかどうかを設定します。 カラーパラメーターを使用すると、以下の追加設定が可能になります。入力はユーザー定義のマスク入力に切り替わります。 |
| <b>マスク</b> | カラーパラメーターマスクでのみアクティブです。 画像自体に基づいてマスクを決定する追加のマスクパラメーターが含まれています。 次のパラメーターを使用すると、イコライゼーションを適用するバイナリマスクに濃淡を正確に変換できます。 これらの設定を使用すると、半径パラメーターの効果がずっと目立たなくなることに注意してください。 |
| <b>色</b> <i>（カラー値）</i> |  |
| <b>色相範囲</b> <i>0.0 - 360.0</i> |  |
| <b>クロマ範囲</b> <i>0.0 - 1.0</i> |  |
| <b>ルミナンス範囲</b> <i>0.0 - 1.0</i> |  |
| <b>ぼかし</b> <i>0.0 - 2.0</i> |  |
| <b>Smoothness</b> <i>0.0 - 2.0</i> |  |
