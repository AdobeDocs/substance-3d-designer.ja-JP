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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 1%

---


# スマート自動タイル

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/smart-auto-tile.png){width="128px"}

## スマート自動タイル

**イン：** *マテリアルフィルター/スキャン処理*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、入力のスマート分析に従って、ベースカラー、法線、およびハイトマップの非タイリングセットをタイリングバージョンに変換します。 [タイル写真の作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)と似ていますが、すべてのチャンネルの情報を使用して最もスマートにブレンドされるため、より高度です（[コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)と同様です）。 また、タイル分割に使用する領域を決定するための[Crop](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)関数も内蔵しています。この関数を正しく理解するには、[切り抜きノードについて詳しく参照](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/crop/crop.md)してください。

このノードを使用するには、まず切り抜き領域を定義し、次にエッジ設定を使用して、タイリングされたエッジを中心にブレンドする方法を指定します。 Tresholdパラメータはこの点で重要です。 このエフェクトでは、広く均一な領域はあまり効果がありません。ディテールとシェイプが多いほど、多くの作業が必要になることに注意してください。

## パラメーター

### 入力

* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。 「マスクを使用」パラメーターで切り替えることができます。

### パラメーター

* **切り抜き**
  * **入力サイズ**: *0 - 8192*&#x200B;入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。
  * **変換**: *（変換行列）*\
    結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。
  * **オフセット**: *0.0 - 1.0*\
    結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。
* **エッジ**
  * **エッジの検出**: *偽/真*&#x200B;検出された特別なエッジのブレンドのオンとオフを切り替えます。
  * **チャネルごとのしきい値を使用**: *False/True*&#x200B;グローバルなtreshold値、または各チャネルごとに1つの値を切り替えます。
  * **しきい値**: *0.0 ～ 1.0*
  * **しきい値の基本色**: *0.0 - 1.0*
  * **しきい値標準**: *0.0 ～ 1.0*
  * **しきい値のHeight**: *0.0 - 1.0*
  * **カットのオフセット**: *0.0 ～ 0.5*&#x200B;カットを移動するためのメインコントロールです。X軸とY軸の両方が分離されています。
  * **ぼかし**: *0.0 ～ 2.0*&#x200B;描画トランジションをぼかします。
  * **Smoothness**: *0.0 ～ 2.0*&#x200B;エッジ分析結果のジャギーを制御します。
  * **グリッド解像度**: *1 - 11*&#x200B;エッジ分析の品質解像度。
  * **基本色を使用**: *False/True*&#x200B;基本色の処理（インとアウト）を切り替えます。
  * **標準を使用**: *False/True*&#x200B;標準の処理（インとアウト）を切り替えます。
  * **Heightを使用**: *False/True*&#x200B;通常の処理（インとアウト）を切り替えます。
  * **マスクを使用**: *False/True*\
    カスタムスタンプマスクシェイプのマスクマップの使用のオンとオフを切り替えます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
