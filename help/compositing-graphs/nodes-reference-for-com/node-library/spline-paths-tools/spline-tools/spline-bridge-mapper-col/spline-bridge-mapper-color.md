---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-mapper-color.html"
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
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---


# スプラインブリッジマッパーの色

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-bridge-mapper-color-icon.png "ノードアイコン")

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

## 入力コネクタ

<b>スプライン座標</b> *色*&#x200B;入力スプラインの点の座標は、カラー画像のRGBAチャンネルでエンコードされています：\
<b> R</b> - X位置\
<b> G</b> - Y位置\
<b> B</b> - Height\
<b>A</b> – パックされたデータ：\
*記号：スプラインが閉じている（負）か、開いている（正）;\
*絶対値：Thickness + 1。

<b>スプラインデータ</b> *色*&#x200B;カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データです。\
<b> R</b> – 接線X\
<b> G</b> – 接線Y\
<b> B</b> – 未使用\
<b> A</b> – 未使用

<b>スプラインの量</b> *整数*&#x200B;入力スプラインの数です。

<b>カラーマップ&#x200B;</b>*カラー*&#x200B;入力スプライン全体にマップする必要がある入力カラー画像。

## 出力コネクタ

<b>色</b> *グレースケール*&#x200B;入力カラー画像を背景のスプラインにマッピングした結果です。

<b>Height</b> *グレースケール*&#x200B;スプラインにマップされたスプラインのHeightをグレースケールイメージで表したものです。

<b>UV</b> *色*&#x200B;マップされたイメージのUV （座標）で、カラー画像の赤(U)および緑(V)チャンネルでエンコードされます。

<b>マスク</b> *グレースケール*&#x200B;スプライン間のマッピングのマスク。

## パラメーター

<b>セグメント数</b> *整数*&#x200B;スプラインは、イメージ座標が通過する前にセグメントに簡略化されます。\
セグメントの数が多いほど、曲線に沿ったマッピングがスムーズになります。

<b>UVの伸縮を縮小</b> *ブール値*&#x200B;スプライン間の距離が不均等な場合にストレッチを最小限に抑えるために、1つのスプラインから次のスプラインにイメージ座標を補間する方法を調整します。

<b>UV スケール</b> *浮動小数点2*&#x200B;画像座標のスケールを調整します。 値を大きくすると、画像がより密集してタイルされます。

<b>UV回転</b> *フロート*&#x200B;画像の座標を中心に回転します。

<b>背景色</b> *フロート4*&#x200B;出力する画像の背景色です。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperGrayscale-Variant1-Before.jpg" alt="SplineBridgeMapperGrayscale-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineBridgeMapperColor-Variant1-After.jpg" alt="SplineBridgeMapperColor-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineBridgeMapperColor-Demo.gif "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例1](../../../../../../assets/SplineBridgeMapperColor-Variant1-After1.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineBridgeMapperColor-Graph.jpg "ノードの例2")

</td>
</tr>
</table>
