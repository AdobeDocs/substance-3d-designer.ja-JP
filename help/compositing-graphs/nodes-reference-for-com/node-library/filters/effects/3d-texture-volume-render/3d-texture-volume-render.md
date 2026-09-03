---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: 3Dテクスチャボリュームレンダーノードを使用して、3Dデータからボリュームテクスチャをレンダーし、雲やフォグのエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dテクスチャボリュームレンダリング
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 0%

---


# 3Dテクスチャボリュームレンダリング

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-texture-volume-render.resources/3d-texture-volume-render-01.png){width="200px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**3Dテクスチャボリュームレンダリング**&#x200B;ノードは、対応する&#x200B;**3D 符号付き距離場**&#x200B;画像入力の&#x200B;*署名付き距離フィールド*&#x200B;を使用して、*3Dテクスチャ*&#x200B;で記述された図形のボリュームをレンダリングします。

体積は&#x200B;*単位キューブ*&#x200B;の境界内で表されます。 照明は、*指向性ライト*&#x200B;と&#x200B;*半球スカイライト*&#x200B;を使用して計算されます。

>[!NOTE]
>
> 署名付き距離フィールドは、256スライスの&#x200B;**16x16**&#x200B;グリッドを持つ図形を記述する&#x200B;**4096x4096**&#x200B;テクスチャである必要があります。\
> [3DテクスチャSDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)ノードを使用して、256スライスの3Dテクスチャの署名付き距離フィールドを計算できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>3D 符号付き距離場</b> <i>グレースケール</i> | 図形の<i>符号付き距離フィールド</i>の256 <i>スライス</i>を表す4096 x 4096の画像は、16 x 16グリッドに配置されました。<br>[3D テクスチャ SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)ノードを使用して、256スライスの3D テクスチャの符号付き距離フィールドを計算できます。 |
| <b>密度</b> <i>グレースケール</i> | 図形の<i>密度</i>の256 <i>スライス</i>を表す4096 x 4096の画像は、16 x 16グリッドに配置されています。 Densityは、グレースケールの値を0 （完全に透明） ～ 1 （完全に不透明）の範囲でマップされます。<br>必要に応じて、[3Dボリュームマスク](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)または3D ノイズノード（[3Dパーリンノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)、[3Dボロノイ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md)、[3Dリッジノイズフラクタル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md)など）を[3D テクスチャ位置](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md)ノードと組み合わせて、256スライスの3D テクスチャとしてボリュームマスクを生成します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>出力解像度</b> <i>整数2</i> | <b>X</b>と<b>Y</b>の出力画像の解像度です。<i>2</i>の累乗で表されます。 |
| <b>カメラの位置</b> <i>浮動小数点2</i> | シェイプの周囲のカメラの位置。<br>ノードを選択した場合は、<b>2D ビュー</b>のポジションギズモを使用して、カメラを<i>軌道</i>できます。 |
| <b>明るい位置</b> <i>浮動小数2</i> | 図形の周囲の<i>指向性ライト</i>の位置です。<br>節点を選択すると、光源の<b>2D ビュー</b>にある位置ギズモを使用して<i>軌道</i>できます。 |
| <b>カメラの距離</b> <i>浮動小数</i> | カメラからシェイプまでの距離です。 |
| <b>カメラの視野</b> <i>浮動小数</i> | <i>度</i>のカメラの視野です。 |
| <b>吸収</b> <i>フロート</i> | ボリュームの<i>を通過</i>する際に吸収される光の量を調整します。 |
| <b>ぼかし</b> <i>フロート</i> | <b>Density</b>入力で指定された値と<i>inner</i>距離フィールド値を乗算します。<br>これにより、ボリュームの外側の境界から内側に<i>フェードグラデーション</i>の幅が効果的に調整されます。 |
| <b>明るいカラーモード</b> <i>整数</i> | 次の指向性ライトの色を取得する方法を設定します。<br>- <i>RGB（ケルビン）</i>：色はライトの温度から得られ、<i>低い</i>値では<i>暖色</i>の色<br>- <i>RGBの色</i>：温度の値を使用して色を定義します |
| <b>光温度（ケルビン）</b> <i>フロート</i> | 指向性ライトの温度。これは<i>色</i>に影響します。 <i>低い</i>値を指定すると、<i>暖色</i>の色になります。<br>有用な値：<br>1800 K – キャンドルライト<br>2800 K – 白熱球<br>5500 K – 自然光<br>6200 K – 自然白<br>7000 K – 曇り空<br><i>注意</i>：このパラメーターは、<b>ライトカラーモード</b>パラメーターが<i>温度（ケルビン）</i>に設定されている場合にのみ使用できます。 |
| <b>明るい色</b> <i>浮動小数3</i> | 指向性ライトの色です。<br><i>注意</i>：このパラメーターは、<b>ライトカラーモード</b>パラメーターが<i>RGBカラー</i>に設定されている場合にのみ使用できます。 |
| <b>光の強さ</b> <i>浮動小数</i> | 指向性ライトの強度。 |
| <b>周囲光の色</b> <i>浮動小数3</i> | 環境光の色。 |
| <b>周辺光度</b> <i>浮動小数</i> | 環境光の強度。 |
| <b>アルベド</b> <i>浮動小数3</i> | ボリュームのアルベドカラー。 |
| <b>背景モード</b> <i>整数</i> | <b>背景色</b>:<br>- <i>影付き</i>に基づいて、レンダリングされたシーンの背景をシェーディングする方式：色は指向性ライトの<i>色</i>および<i>強度</i><br>- <i>一定の色</i>の影響を受けます：色は、指向性ライトの<i>に関係なく</i>均一に適用されます |
| <b>背景色</b> <i>浮動小数4</i> | レンダリングされたシーンの背景を塗りつぶすために使用される色です。 |
| <b>ディザリング</b> <i>浮動小数</i> | シェーディングを滑らかにするために使用する<i>ブルーのノイズディザリング</i>の適用度を調整します。 |
| <b>グリッドを有効にする</b> <i>ブーリアン</i> | <i>真</i>の場合、<i>無限</i>のグリッドをレンダリングします。 図形を囲む<i>単位立方体</i>はこの平面上にあります。 |
| <b>無限平面</b> <i>ブール値</i> | グリッドを<i>無限に</i>延長して地平線に向かうように設定します。<br><i>注意</i>：このパラメーターは、<b>グリッドを有効にする</b>パラメーターが<i>真</i>に設定されている場合にのみ使用できます。 |
| <b>グリッドサイズ</b> <i>浮動小数点2</i> | グリッドのサイズを調整します。<br><i>注意</i>：このパラメーターは、<b>グリッドを有効にする</b>パラメーターが<i>True</i>に設定され、<b>無限平面</b>パラメーターが<i>False</i>に設定されている場合にのみ使用できます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3d-texture-volume-render-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3d-texture-volume-render-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3d-texture-volume-render-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3d-texture-volume-render-05.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3d-texture-volume-render-06.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-texture-volume-render.resources/3d-texture-volume-render-07.png" />
        </td>
    </tr>
</table>
