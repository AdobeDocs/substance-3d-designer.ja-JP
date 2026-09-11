---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
breadcrumb-title: ''
description: スプラインブリッジマッパーの色ノードを使用して、カラーマッピングを使用して2つのスプライン間でテクスチャをブリッジします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインブリッジマッパーの色
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 1%

---


# スプラインブリッジマッパーの色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-bridge-mapper-color.resources/spline-bridge-mapper-color-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

カラー画像を入力スプラインのリスト全体にマッピングし、画像が順番にスプラインを横切るようにします。

</td>
</tr>
</table>

>[!TIP]
>
> マッピングは、リストの最初のスプラインから最後のスプラインに進み、リスト内のこれらのスプラインの順序に厳密に従って中間スプラインを横断します。
> 
> したがって、事前にスプラインを追加する順序に注意する必要があります。

>[!NOTE]
>
> [スプラインブリッジマッパーグレースケール](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-gra/spline-bridge-mapper-grayscale.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |
| <b>カラーマップ</b> <i>色</i> | 入力スプラインにマッピングする入力カラーイメージ。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>色</b> <i>グレースケール</i> | バックグラウンド上のスプラインに入力カラー画像をカラー画像としてマッピングした結果。 |
| <b>Height</b> <i>グレースケール</i> | グレースケールイメージとして、スプラインにマッピングされたスプラインのHeight。 |
| <b>UV</b> <i>色</i> | カラー画像の赤(U)チャンネルと緑(V)チャンネルでエンコードされた、マッピングされた画像のUV（座標）。 |
| <b>マスク</b> <i>グレースケール</i> | スプライン間のマッピングのマスク。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>セグメント数</b> <i>整数</i> | スプラインは、イメージ座標が通過する前にセグメントに簡略化されます。 セグメントの数が多いほど、曲線に沿ったマッピングがスムーズになります。 |
| <b>UVの伸縮を縮小</b> <i>ブール値</i> | 1つのスプラインから次のスプラインへのイメージ座標の補間方法を調整し、スプライン間の距離が不均等な場合の伸縮を最小限に抑えます。 |
| <b>UV スケール</b> <i>浮動小数点2</i> | 画像座標の尺度を調整します。 値を大きくすると、画像がより密集してタイルされます。 |
| <b>UV回転</b> <i>フロート</i> | イメージ座標を中心を基準に回転します。 |
| <b>背景色</b> <i>浮動小数点4</i> | 出力画像の背景色です。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-mapper-color.resources/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Demo.gif "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Variant1-After1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-bridge-mapper-color.resources/SplineBridgeMapperColor-Graph.jpg "ノードの例2")

</td>
</tr>
</table>
