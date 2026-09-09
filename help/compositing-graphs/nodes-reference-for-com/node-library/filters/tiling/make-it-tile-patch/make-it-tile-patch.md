---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/tiling/make-it-tile-patch.html"
breadcrumb-title: ''
description: 「タイルパッチを作成」ノードを使用して、入力画像からシームレスなタイリングテクスチャをパッチして作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Tiling > Make It Tile Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: タイルパッチを作成
user-guide-description: ''
user-guide-title: ''
source-git-commit: f792519db40504d7bb888acf0dc418c6ebfd688a
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 8%

---


# タイルパッチを作成

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](make-it-tile-patch.resources/make-it-tile-patch.png)

![](make-it-tile-patch.resources/make-it-tile-patch-grayscale.png)

<b>イン：</b>フィルター> タイリング

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、グリッドベースのセミランダムタイラーです。 入力パッチを取り込んでスタンプし、設定に基づいて何度も繰り返すことなくタイリング画像に変換しようとします。

テクスチャのパッチが小さく、テクスチャから大きなスケールのタイリングテクスチャを作成する場合に便利です。

これは、主にエッジを修正する[Make-It-Tile Photo](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/tiling/make-it-tile-photo/make-it-tile-photo.md)とは異なることに注意してください。

マテリアル全体でこの操作を行うには、[自動タイルの最適化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/smart-auto-tile/smart-auto-tile.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>マスクサイズ</b> <i>0.0 - 1.0</i> | パッチのスタンプ時に使用される丸いマスクのサイズ。 |
| <b>マスクの精度</b> <i>0.0 - 1.0</i> | マスクのフォールオフ/Smoothness精度。 |
| <b>マスクのワープ</b> <i>-100.0 - 100.0</i> | マスクのエッジにワープを適用します。 パッチ間の滑らかで未定義の遷移を回避するのに適しています。 |
| <b>パターンサイズの幅</b> <i>0.0 - 1000.0</i> | パッチの幅を不均等に変更します。 |
| <b>パターンサイズのHeight</b> <i>0.0 - 1000.0</i> | パッチのHeightを不均等に変更します。 |
| <b>障害</b> <i>0.0 - 1.0</i> | パッチを少しずつずらしながら、トランスレーショナルなランダム性を導入します。 |
| <b>サイズのバリエーション</b> <i>0.0 - 100.0</i> | マスクのサイズ変更を導入します。 |
| <b>オクターブ</b> <i>0 - 6</i> | これは、全体のサイズを決定するメインコントロールです。 |
| <b>回転</b> <i>-360.0 - 360.0</i> | パッチを事前に回転します。 |
| <b>回転バリエーション</b> <i>0.0 - 360.0</i> | パッチスタンプごとにランダムな回転を導入します。 |
| <b>背景色</b> <i>（カラー値）</i> | パッチが表示されない領域の背景色を設定します。 |
| <b>カラーバリエーション</b> <i>0.0 ～ 1.0 （カラーバージョンのみ）</i> | パッチごとのカラーバリエーションを導入します。 |
| <b>輝度のバリエーション</b> <i>（グレースケールバージョンのみ）</i> | パッチごとの輝度のバリエーションを導入します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="make-it-tile-patch.resources/patch-ex.gif" />
        </td>
    </tr>
</table>
