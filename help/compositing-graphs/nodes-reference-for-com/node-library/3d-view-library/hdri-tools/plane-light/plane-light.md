---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/plane-light.html"
breadcrumb-title: ''
description: 平面光源ノードを使用すると、指向性ライトを制御するために平面光源をHDRI環境に追加できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Plane Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 平面ライト
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 4%

---


# 平面ライト

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](plane-light.resources/plane-light-01.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

球面投影された平面形状を生成します。 入力パラメーターを使用して、平面を3Dに配置および方向付けできます。

単純な[シェイプライト](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/shape-light/shape-light.md)とは異なり、単純な原点プロジェクションの外側により高度な配置オプションがあり、[ラインライト](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/line-light/line-light.md)と同様により多くのパターンやマスクを適用できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>背景画像の入力</b> <i>カラー入力</i> | 生成されたライトを構成するオプションの背景。 |
| <b>シェイプ画像の入力</b> <i>カラー入力</i> | ラインライトにマッピングするオプションの画像。 シェイプのカラーモードが画像入力に設定されている場合にのみ使用されます。 |
| <b>パターン画像の入力</b> <i>グレースケール入力</i> | カスタムパターン画像。「Pattern」パラメーターが「Image Input」に設定されている場合に使用されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>位置モード</b> <i>地面/天井、原点、ワールドポジション</i> | 3つの異なる配置モードから選択します。 地面/天井と原点のサポートの操作2Dビューでは、ワールド位置はプロパティを通じてのみ変更できますが、より正確な配置をサポートします。 |
| <b>地面のグリッドを表示</b> <i>False/True</i> | デバッググラウンドグリッドの描画を有効にするヘルパー関数。 スペース内の行の位置の推定に役立ちます。 |
| <b>位置の座標</b> |  |
| <b>上向きベクター</b> <i>Z上、Y上</i> | ワールド位置モードでのみ、座標系の方向を決定します。 |
| <b>平面UVの位置</b> | 地面/天井と原点のみ。 UV空間でのプレーンの位置を設定します。 |
| <b>平面のワールド位置</b> <i>-2.0 - 2.0</i> | ワールド位置モードの場合のみ。 平面の位置ワールド空間を設定します。 2Dビューのインタラクションはサポートされていません。 |
| <b>平面絶対Height</b> <i>0.0 - 1.0</i> | Ground/Ceiling Position Modeでのみ、天井からの絶対Heightを設定します。 [グリッドを表示]を使用して、位置をより正確に推定します。 |
| <b>原点</b> <i>0.0 - 1.0</i> | 原点ポジションモードの場合のみ 両方のポイントのパノラマ中心からの距離を設定します。 |
| <b>図形のカラーモード</b> <i>RGB、色温度（ケルビン）、画像入力</i> | シェイプカラーの設定に使用する方法を選択します。 イメージ入力により、2番目の入力スロットが使用可能になります。 |
| <b>色</b> <i>（カラー値）</i> | シェイプカラーモードを「RGB」に設定した場合のみ シェイプのカラーを選択します。 |
| <b>温度</b> <i>800.0 - 20000.0</i> | Shape Color ModeがTemperatureに設定されている場合のみ シェイプのカラーのケルビン値を設定します。 |
| <b>図形の画像のUVモード</b> <i>伸縮、中央のみ伸縮、繰り返し+間隔</i> | シェイプのカラーモードを画像入力に設定した場合のみ。 イメージをラインシェイプに適用する方法を設定し、UVの繰り返し動作を決定します。 |
| <b>シェイプ画像の繰り返し間隔</b> <i>0.0 - 1.0</i> | シェイプカラーモードを画像入力に設定し、UVモードを繰り返し+間隔に設定した場合のみ。 画像が線に沿って繰り返される際の間隔を設定します。 |
| <b>シェイプ画像のガンマ</b> <i>sRGB、リニア</i> | シェイプのカラーモードを画像入力に設定した場合のみ。 シェイプ画像の入力を解釈する方法を指定します。 |
| <b>露光量(EV)</b> <i>0.0 - 10.0</i> | 生成されたシェイプの露光量値を設定します。背景画像の露光量値と理想的に一致させます。 |
| <b>平面スケール</b> <i>0.0 - 1.0</i> | 平面シェイプの均一スケールを設定します。 |
| <b>平面サイズ</b> <i>0.0 - 1.0</i> | 平面シェイプのサイズを不均等に設定します。 |
| <b>面の回転</b> <i>0.0 - 1.0</i> | 中心軸に沿って平面を回転します。 |
| <b>パターン</b> <i>正方形、シャープな正方形、円錐、半球、画像入力</i> | 使用するパターン形状を選択します。 |
| <b>パターン硬さ</b> <i>0.0 - 1.0</i> | パターンの硬さ/コントラストを設定します。 |
| <b>パターンUVモード</b> <i>伸縮、中央のみ伸縮</i> | シェイプ画像の上に適用される第2パターンマスクの使用方法を設定します。 |
| <b>グラウンドクリッピングを有効にする</b> <i>False/True</i> | Planeがグリッドでクリップできるか、下に移動するときにまだ表示されている場合は、このオプションを有効にします。 [グリッドを表示]を使用して、これを適切に推定します。 |
| <b>地上Height</b> <i>-2.0 - 0.0</i> | クリッピングのグランドHeightを調整します。 |
| <b>バックグラウンド入力を有効にする</b> <i>False/True</i> | オプションの背景画像の使用を切り替え 生成されたライトを背景の上に合成します。 |
| <b>背景色</b> <i>（カラー値）</i> | 背景入力を使用しない場合は、単色の背景色を設定します。 |
| <b>背景ガンマ</b> <i>sRGB、リニア</i> | バックグラウンド入力を使用する場合は、バックグラウンド入力の解釈方法を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="plane-light.resources/plane-light-02.gif" />
        </td>
    </tr>
</table>
