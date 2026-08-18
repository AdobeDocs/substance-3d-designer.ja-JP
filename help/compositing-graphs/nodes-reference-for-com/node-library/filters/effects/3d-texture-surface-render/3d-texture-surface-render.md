---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/3d-texture-surface-render.html"
breadcrumb-title: ''
description: 3Dテクスチャサーフェスレンダリングノードを使用して、3Dデータからサーフェステクスチャをレンダーし、プロシージャサーフェス効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > 3D Texture Surface Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dテクスチャサーフェスレンダリング
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%

---


# 3Dテクスチャサーフェスレンダリング

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender.png){width="200px"}

**イン：** *フィルター/効果*

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**3Dテクスチャ表面レンダリング**&#x200B;ノードは、**3D距離フィールド**&#x200B;の画像入力から対応する&#x200B;*距離フィールド*&#x200B;を使用して、*3Dテクスチャ*&#x200B;で記述された図形の表面をレンダリングします。

サーフェスは、*単位キューブ*&#x200B;の境界内に表されます。 照明は、無限球にマップされた&#x200B;**環境**&#x200B;入力画像を使用して計算されます。

>[!NOTE]
>
> 距離フィールドは、256スライスの&#x200B;**16x16**&#x200B;グリッドのシェイプを記述する&#x200B;**4096x4096**&#x200B;テクスチャである必要があります。\
> [3DテクスチャSDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)ノードを使用して、256スライスの3Dテクスチャの距離フィールドを計算できます。

</td>
</tr>
</table>

## パラメーター

### 入力

* **3D距離フィールド** *グレースケール*\
  図形の&#x200B;*距離フィールド*&#x200B;の256 *スライス*&#x200B;を表す4096 x 4096の画像は、16 x 16グリッドに配置されています。\
  [3DテクスチャSDF](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-texture-sdf/3d-texture-sdf.md)ノードを使用して、256スライスの3Dテクスチャの距離フィールドを計算できます。
* **環境** *色*\
  レンダリングで無限球にマップされる&#x200B;*環境*&#x200B;を表すイメージです。*照明*&#x200B;の計算に使用されます。\
  この画像は、**背景モード**&#x200B;パラメーターが&#x200B;*環境*&#x200B;または&#x200B;*環境*&#x200B;に設定されている場合に、シーンの背景をレンダリングするためにも使用されます。

### パラメーター

* **出力解像度** *整数2*\
  **X**&#x200B;と&#x200B;**Y**&#x200B;の出力画像の解像度です。*2*&#x200B;の累乗で表されます。
* **カメラ位置** *フロート2*\
  シェイプの周囲のカメラの位置。\
  ノードが選択されている場合は、**2Dビュー**&#x200B;の位置ギズモを使用して、カメラを&#x200B;*軌道*&#x200B;できます。
* **カメラの距離** *浮動小数点*\
  カメラからシェイプまでの距離です。
* **カメラの視野** *浮動小数点*\
  カメラの視野（*度*）。
* **アルベド** *浮動小数点3*\
  図形のサーフェスのアルベド色です。
* **背景モード** *整数*\
  レンダリングされたシーンの背景を表す方法：
  * *接地放射*：計算された接地平面の放射照度
  * *アンビエント*: **環境**&#x200B;画像入力のアンビエントカラーは無限球にマップされます。これは画像の非常にぼやけたバージョンに似ています
  * *均一な色*：指定した色で背景を均一に塗りつぶします
  * *環境*: **環境**&#x200B;の画像入力が無限球にマップされました
* **背景色** *浮動小数点4*\
  レンダリングされたシーンの背景を均一に塗りつぶすために使用される色です。\
  *注意*：このパラメーターは、**背景モード**&#x200B;パラメーターが&#x200B;*均一色*&#x200B;に設定されている場合にのみ使用できます。
* **グリッドを有効にする** *ブール値*\
  *真*&#x200B;の場合、はグリッドをレンダリングします。 図形を囲む&#x200B;*単位立方体*&#x200B;はこの平面上にあります。
* **無限平面** *ブール値*\
  グリッドを&#x200B;*無限に*&#x200B;延長するように設定します。\
  *注意*：このパラメーターは、**グリッドを有効にする**&#x200B;パラメーターが&#x200B;*True*&#x200B;に設定されている場合にのみ使用できます。
* **グリッドのサイズ** *フロート2*&#x200B;グリッドのサイズを調整します。\
  *注意*：このパラメーターは、**グリッドを有効にする**&#x200B;パラメーターが&#x200B;*True*&#x200B;に設定され、**Infinite Plane**&#x200B;パラメーターが&#x200B;*False*&#x200B;に設定されている場合にのみ使用できます。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant3.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-variant4.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/3dtexturesurfacerender-node.png){width="512px"}

</td>
</tr>
</table>
