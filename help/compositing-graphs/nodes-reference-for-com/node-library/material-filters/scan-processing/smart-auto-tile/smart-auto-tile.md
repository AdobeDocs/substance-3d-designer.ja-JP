---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/smart-auto-tile.html"
breadcrumb-title: ''
description: スマート自動タイルノードを使用すると、インテリジェントパターン検出を使用して、スキャンしたマテリアルからシームレスなタイルを自動的に作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Smart Auto Tile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スマート自動タイル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '393'
ht-degree: 5%

---


# スマート自動タイル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](smart-auto-tile.resources/smart-auto-tile-01.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、入力のスマート分析に従って、ベースカラー、法線、およびハイトマップの非タイリングのセットをタイリングのバージョンに変換します。 [写真を並べて表示](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)に似ていますが、すべてのチャンネルの情報を使用して最もスマートにブレンドされるため、より高度です（[クローンパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)と同様です）。 また、タイリング時に使用する領域を判断するための[Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)関数も内蔵しています。この関数を正しく理解するには、[切り抜きノードについて詳しく参照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)してください。

このノードを使用するには、まず切り抜き領域を定義し、次にエッジ設定を使用して、タイリングされたエッジを中心にブレンドする方法を指定します。 Tresholdパラメータはこの点で重要です。 このエフェクトでは、広く均一な領域はあまり効果がありません。ディテールとシェイプが多いほど、多くの作業が必要になることに注意してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスクを使用」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>切り抜き</b> |  |
| <b>入力サイズ</b> <i>0 - 8192</i> | 入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。 |
| <b>変形</b> <i>（変換行列）</i> | 結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。 |
| <b>エッジ</b> |  |
| <b>エッジの検出</b> <i>False/True</i> | 検出された特殊エッジのブレンドのオンとオフを切り替えます。 |
| <b>チャネルごとのしきい値を使用する</b> <i>False/True</i> | グローバルなトレッシュホールド値と、各チャンネルに対して1つのトレッシュホールド値を切り替えます。 |
| <b>しきい値</b> <i>0.0 - 1.0</i> |  |
| <b>しきい値のBase color</b> <i>0.0 - 1.0</i> |  |
| <b>しきい値標準</b> <i>0.0 - 1.0</i> |  |
| <b>しきい値のHeight</b> <i>0.0 - 1.0</i> |  |
| <b>切り取りオフセット</b> <i>0.0 - 0.5</i> | カットを動かすためのメインコントロール、X方向とY軸の両方が分離されます。 |
| <b>ぼかし</b> <i>0.0 - 2.0</i> | ブレンド効果をぼかします。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | エッジ解析結果のジャギーを制御します。 |
| <b>グリッドの解決</b> <i>1 - 11</i> | エッジ解析の品質解像度。 |
| <b>Base colorを使用</b> <i>False/True</i> | base colorの処理を切り替えます（入力および出力）。 |
| <b>標準を使用</b> <i>False/True</i> | 通常の処理（インとアウト）を切り替えます。 |
| <b>Heightを使用</b> <i>False/True</i> | 通常の処理（インとアウト）を切り替えます。 |
| <b>マスクを使用</b> <i>False/True</i> | カスタムスタンプマスクシェイプのマスクマップの使用のオンとオフを切り替えます。 |
