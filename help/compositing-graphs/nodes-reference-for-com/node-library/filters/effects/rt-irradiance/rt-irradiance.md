---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-irradiance.html"
breadcrumb-title: ''
description: RT放射ノードを使用して、ジオメトリからリアルタイムの放射照度情報を計算し、リアルなライティングを計算します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Irradiance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RT放射
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 4%

---


# RT放射

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](rt-irradiance.resources/rt-irradiance-01.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

環境マップと放射マップから生成されたHeightマップ入力に対してレイトレース放射照度を生成します。 グラフ内のテクスチャにライティングを「ベイク処理」する場合に使用します。 偽物のグローバルイルミネーションとグローに使用します。計算時間が長いため、このノードをCPU(SSE)エンジンと組み合わせて使用しないでください。 2つのマップを返します。1つは放射がマテリアル入力に適用される放射照度出力、もう1つは計算された放射照度値のみを含む未処理の放射照度マップです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Height</b> <i>グレースケール入力</i> | Heightは、マテリアルスロットからの唯一の必須入力です。 これがないと、ノードが正常に機能しません。 |
| <b>放射体</b> <i>カラー入力</i> | Emissiveは、純粋な黒は光を放たず、その他の色の値は光を放つフォーマットにする必要があります。 Alphaは無視されます。 結果を確認するには、このスロットへの接続または環境スロットが必要です。 |
| <b>環境</b> <i>カラー入力</i> | 放射を計算するためのHDRライティング環境。 結果を確認するには、このスロットへの接続またはEmissiveスロットが必要です。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>Heightスケール</b> <i>0.0 - 1.0</i> | Heightを変換するスケール。 シーン全体の外観に影響します。 |
| <b>クォリティ</b> <i>32光線、64光線、128光線</i> | 結果の品質を決定しますが、パフォーマンスにも影響します。 光線が少ないほど、ノイズが多くなります。 |
| <b>バウンスの計算</b> <i>False/True</i> | バウンスの計算を切り替えます。 品質と速度に影響します。 |
| <b>環境のローテーション</b> <i>0.0 - 1.0</i> | 環境を回転させます。 |
| <b>環境露出(EV)</b> <i>-4.0 - 4.0</i> | 環境に使用する露光量の値は、エフェクトの合計輝度に影響します。 |
| <b>放射強度</b> <i>0.0 - 20.0</i> | 放射入力の乗数。放射光からの放射光の強度に影響します。 |
| <b>Emissiveカラースペース</b> <i>sRGB、リニア</i> | Enissive入力の解釈に使用されるカラースペース。 |
| <b>未処理の放射照度AlphaのIBLシャドウ</b> <i>False/True</i> | ぼかしを切り替えて、 |
| <b>Emissive LOD バイアス</b> <i>-1.0 - 1.0</i> | emissive放射の精度を調整します。 値が小さいほど、ノイズが多くなります。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-irradiance.resources/rt-irradiance-04.jpg" />
        </td>
    </tr>
</table>
