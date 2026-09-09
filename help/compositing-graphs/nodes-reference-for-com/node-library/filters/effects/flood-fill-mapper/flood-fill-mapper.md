---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/flood-fill-mapper.html"
breadcrumb-title: ''
description: Flood Fillマッパーノードを使用して、テクスチャ処理にflood fillアルゴリズムを使用して、コネクトされたリージョン間で値をマッピングします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Flood Fill Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Flood Fillマッパー
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '666'
ht-degree: 6%

---


# Flood Fillマッパー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/floodfill-mapper-gray.png)![](../../../../../../assets/floodfill-mapper-color.png)

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

Flood Fillマッパーを使用すると、[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)から各セルに既存のパターンまたはテクスチャを再マッピングできます。 [ランダムグレースケール](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-random-gra/flood-fill-to-random-grayscale.md)や[グラデーション](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill-to-gradient/flood-fill-to-gradient.md)などの他のFlood Fill変換とは異なり、単色や値は生成されませんが、独自の入力マップを使用できます。 [Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)と[タイルSampler](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)または[シェイプマッパー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-mapper/shape-mapper.md)の組み合わせのようなものとみなすことができます。これは、非常に多くの同様のコントロールやインターフェイスを提供するためです。

Colorバージョンには、法線マップを操作するための追加のコントロールがあります。このコントロールでは、[接線空間のノーマップ回転を補正](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-vector-rotation/normal-vector-rotation.md)できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Flood Fillボックス</b> <i>カラー入力</i> | 標準のFlood Fill入力です。必須。 |
| <b>パターン入力1-8</b> <i>グレースケール/カラー入力</i> | カスタムパターンの画像入力。 |
| <b>パターン配布マップ</b> <i>グレースケール入力</i> | ID マップを使用して、どのパターンがどのセルに送られるかを判断します。 Flood Fillから索引など、他のFlood Fillマップから取り込むことができます。 |
| <b>地図の縮尺</b> <i>グレースケール入力</i> | セルごとのスケールを決定するためのマップ。 |
| <b>回転マップ</b> <i>グレースケール入力</i> | セルごとの回転を決定するためにマップします。 |
| <b>輝度オフセットマップ</b> <i>グレースケール入力</i> | セルごとの輝度を設定するマップ |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>タイリングモード</b> <i>タイリングなし、H+V</i> | タイリングを使用するかどうかを設定します。 サイズまたはスケールが1より小さく設定されている場合にのみ表示されます。 |
| <b>パターン</b> |  |
| <b>パターンの入力番号</b> <i>1 - 8</i> | 使用するカスタムパターン入力の量を設定します。 |
| <b>パターン配布モード</b> <i>ランダム、図形のサイズ、分布マップの入力</i> | セルに表示するパターンを決定する方法を設定します。 |
| <b>パターン分布のジッター</b> <i>0.0 - 1.0</i> | ランダムシードを使用してすべてを変更することなく、パターン分布にわずかな変化またはオフセットを適用できます。 |
| <b>サイズ</b> |  |
| <b>サイズモード</b> <i>テクスチャを基準にする、図形の頂点を基準にする、最も大きい図形を基準にする、最も小さい図形を基準にする、図形の幅に合わせる</i> | 各セルのパターンサイズの決定方法を設定します。 |
| <b>サイズ</b> <i>0.0 - 1.0</i> | パターンの不均等なスケーリングを可能にします。 |
| <b>スケール</b> <i>0.0 - 1.0</i> | エフェクトのグローバル（同一）スケールを設定します。 |
| <b>マップマルチプライヤーの拡大/縮小</b> <i>0.0 - 1.0</i> | オプションのスケールマップのインフルエンスを設定します。 |
| <b>ランダムに拡大・縮小</b> <i>-1.0 - 1.0</i> | パターンスケール内でランダムに変動する量を設定します。 |
| <b>回転</b> |  |
| <b>回転</b> <i>0.0 - 1.0</i> | すべてのセルに対してグローバルで均一な回転を設定します。 |
| <b>マルチプライヤーの回転マップ</b> <i>0.0 - 1.0</i> | オプションの回転マップのインフルエンスを設定します。 |
| <b>ランダムな回転</b> <i>0.0 - 1.0</i> | 各セルにランダムな回転の量を設定します。 |
| <b>回転の自動スケール</b> <i>False/True</i> | パターンを回転したときに、セル内に収まるようにパターンの拡大・縮小を調整するかどうかを設定します。 |
| <b>位置</b> |  |
| <b>位置のオフセット</b> <i>0.0 - 1.0</i> | すべてのセルに対してグローバル位置オフセットを設定します。 |
| <b>位置のオフセットアラインメント</b> <i>テクスチャ、パターン</i> | オフセット0点を[パターン]セルまたはテクスチャに位置合わせするように設定します。 |
| <b>位置オフセットランダム</b> <i>0.0 - 1.0</i> | セルごとの位置オフセットのランダム化の量を設定します。 |
| <b>色（グレースケールバージョンのみ）</b> |  |
| <b>輝度範囲</b> <i>0.0 - 1.0</i> | テクスチャの全体的なコントラストを設定します。0は中間のグレーになります。 |
| <b>輝度範囲ランダム</b> <i>0.0 - 1.0</i> | 輝度範囲のランダム化の量を設定します。 |
| <b>輝度オフセット</b> <i>-1.0 - 1.0</i> | 輝度のオフセットを設定します。値は明るさコントロールとして機能します。 |
| <b>輝度オフセットランダム</b> <i>0.0 - 1.0</i> | 輝度オフセットのランダム化の量を設定します。 |
| <b>輝度オフセットマップマルチプライア</b> <i>0.0 - 1.0</i> | オプションの輝度オフセットマップの影響を設定します。 |
| <b>背景色</b> <i>（グレースケール値）</i> | テクスチャをブレンドする背景色を設定します。 |
| <b>色（カラーバージョンのみ）</b> |  |
| <b>法線マップ</b> <i>False/True</i> | パターン入力を法線マップとして解釈するように設定します。 標準正接空間の回転を補正して修正します。 |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 法線マップ形式を切り替えます（グリーンチャンネルを反転します）。 Is 法線マップがTrueの場合にのみアクティブになります。 |
| <b>HSL調整</b> <i>-1.0 - 1.0</i> | HSLをグローバルに調整 |
| <b>HSLランダム</b> <i>-1.0 - 1.0</i> | セルごとにHSLのランダム化を設定します。 |
| <b>Alpha調整</b> <i>-1.0 - 1.0</i> | 全体的なAlphaを調整して、Alphaのコントラストを下げます。 |
| <b>Alphaランダム</b> <i>-1.0 - 1.0</i> | セルごとにAlpha調整のランダム化を設定します。 |
| <b>背景色</b> <i>（カラー値）</i> | テクスチャをブレンドする背景色を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/floodfill-mapper-ex01.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/floodfill-mapper-ex02.jpg" />
        </td>
    </tr>
</table>
