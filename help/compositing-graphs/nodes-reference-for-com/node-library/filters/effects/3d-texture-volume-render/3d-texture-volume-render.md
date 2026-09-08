---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-volume-render.html"
breadcrumb-title: ''
description: 3D テクスチャボリュームレンダーノードを使用して、雲やフォグのエフェクトを作成するために3Dデータからボリュームテクスチャをレンダーします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Volume Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D テクスチャボリュームレンダリング
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---


# 3D テクスチャボリュームレンダリング

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender.png){width="200px"}

**イン：** *フィルター/効果*

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**3D テクスチャボリュームレンダリング**&#x200B;ノードは、**3D 符号付き距離場**&#x200B;の画像入力からの対応する&#x200B;*signed distanceフィールド*&#x200B;を使用して、*3D テクスチャ*&#x200B;によって記述された図形のボリュームをレンダリングします。

体積は&#x200B;*単位キューブ*&#x200B;の境界内で表されます。 照明は、*指向性ライト*&#x200B;と&#x200B;*半球スカイライト*&#x200B;を使用して計算されます。

>[!NOTE]
>
> 署名付き距離フィールドは、256スライスの&#x200B;**16x16**&#x200B;テクスチャを持つ図形を表す&#x200B;**4096x4096**&#x200B;グリッドである必要があります。\
> [3D テクスチャ SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)ノードを使用して、256スライスの3D テクスチャの署名付き距離フィールドを計算できます。

</td>
</tr>
</table>

## パラメーター

### 入力

* **3D 符号付き距離場** *グレースケール*\
  図形の&#x200B;*符号付きディスタンスフィールド*&#x200B;の256 *スライス*&#x200B;を表す4096 x 4096の画像は、16 x 16グリッドに配置されました。\
  [3D テクスチャ SDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)ノードを使用して、256スライスの3D テクスチャの署名付き距離フィールドを計算できます。
* **密度** *グレースケール*\
  図形の&#x200B;*密度*&#x200B;の256 *スライス*&#x200B;を表す4096 x 4096の画像は、16 x 16グリッドに配置されています。 密度は、0（完全に透明）から1（完全に不透明）のグレースケール値を使用してマップされます。\
  [3Dボリュームマスク](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/3d-volume-mask/3d-volume-mask.md)または3D ノイズノード（[3Dパーリンノイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-perlin-noise/3d-perlin-noise.md)、[3Dボロノイ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-voronoi/3d-voronoi.md)、[3Dリッジノイズフラクタル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/3d-ridged-noise-fractal/3d-ridged-noise-fractal.md)など）を、[3D テクスチャポジション](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-position/3d-texture-position.md)ノードと組み合わせて、256スライスの3D テクスチャとしてボリュームマスクを作成できます。

### パラメーター

* **出力解像度** *整数2*\
  **X**&#x200B;と&#x200B;**Y**&#x200B;の出力画像の解像度です。*2*&#x200B;の累乗で表されます。
* **カメラの位置** *浮動小数2*\
  シェイプの周囲のカメラの位置です。\
  ノードが選択されている場合は、**2D ビュー**&#x200B;のポジションギズモを使用して、カメラを&#x200B;*軌道*&#x200B;できます。
* **明るい位置** *浮動小数2*\
  図形の周囲の&#x200B;*指向性ライト*&#x200B;の位置です。\
  ノードを選択した場合は、**2D ビュー**&#x200B;の位置ギズモを使用して、光源を&#x200B;*軌道*&#x200B;できます。
* **カメラの距離** *浮動小数*\
  カメラから図形までの距離を指定します。
* **カメラの視野** *浮動小数*\
  *度*&#x200B;のカメラの視野です。
* **吸収** *浮動小数*\
  ボリュームの&#x200B;*を通過*&#x200B;する際に吸収される光の量を調整します。
* **ぼかし** *浮動小数*\
  **Density**&#x200B;入力で指定された値と&#x200B;*inner*&#x200B;距離フィールド値を乗算します。\
  これにより、ボリュームの外側の境界から内側に&#x200B;*フェードするグラデーション*&#x200B;の幅が効果的に調整されます。
* **明るいカラーモード** *整数*\
  ディレクショナルライトのカラーの取得方法を設定します。
  * *温度（ケルビン）*：色は光温度から得られます。*低い*&#x200B;値では&#x200B;*暖色*&#x200B;になります
  * *RGBの色*: RGB値を使用して色を定義します
* **光温（ケルビン）** *浮動小数*\
  指向性ライトの温度。これは&#x200B;*色*&#x200B;に影響します。 *低い*&#x200B;値を指定すると、*暖色*&#x200B;の色になります。\
  有用な値：\
  1800 K – キャンドルライト\
  2800 K – 白熱球\
  5500 K – 昼光\
  6200 K – ナチュラルホワイト\
  7000 K – 曇天\
  *注意*：このパラメーターは、**Light Color Mode**&#x200B;パラメーターが&#x200B;*Temperature (Kelvin)*&#x200B;に設定されている場合にのみ使用できます。
* **明るい色** *浮動小数3*\
  指向性ライトのカラー。\
  *注意*：このパラメーターは、**明るい色モード**&#x200B;パラメーターが&#x200B;*RGB色*&#x200B;に設定されている場合にのみ使用できます。
* **光の強さ** *浮動小数*\
  指向性ライトの強度。
* **環境色** *浮動小数3*\
  環境光の色。
* **周辺光度** *浮動小数*\
  環境光の強度。
* **アルベド** *浮動小数3*\
  ボリュームのアルベドカラー。
* **背景モード** *整数*\
  **背景色**&#x200B;に基づいて、レンダリングされたシーンの背景にシェーディングを付ける方法：
  * *影*：色は、指向性ライトの&#x200B;*色*&#x200B;および&#x200B;*強度*- *一定の色*&#x200B;の影響を受けます。色は、指向性ライトの&#x200B;*に関係なく*&#x200B;均一に適用されます
* **背景色** *浮動小数点4*\
  レンダリングされたシーンの背景を塗りつぶすために使用される色です。
* **ディザリング** *浮動小数*\
  シェーディングを滑らかにするために使用する&#x200B;*ブルーのノイズディザリング*&#x200B;の適用度を調整します。
* **グリッドを有効にする** *ブール値*\
  *真*&#x200B;の場合、*無限*&#x200B;のグリッドをレンダリングします。 図形を囲む&#x200B;*単位立方体*&#x200B;はこの平面上にあります。
* **無限平面** *ブーリアン*\
  グリッドを&#x200B;*無限に*&#x200B;延長するように設定します。\
  *注意*：このパラメーターは、**グリッドを有効にする**&#x200B;パラメーターが&#x200B;*True*&#x200B;に設定されている場合にのみ使用できます。
* **グリッドのサイズ** *浮動小数2*&#x200B;グリッドのサイズを調整します。\
  *注意*：このパラメーターは、**グリッドを有効にする**&#x200B;パラメーターが&#x200B;*True*&#x200B;に設定され、**Infinite Plane**&#x200B;パラメーターが&#x200B;*False*&#x200B;に設定されている場合にのみ使用できます。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant5.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturevolumerender-node.png){width="512px"}

</td>
</tr>
</table>
