---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-fill.html"
breadcrumb-title: ''
description: '[スプライン塗り潰し]ノードを使用して、閉じたスプラインによって定義された領域をテクスチャまたは色で塗り潰します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Fill
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン塗り
user-guide-description: ''
user-guide-title: ''
source-git-commit: 86e504c9dfe76516c56a7950f0bf70090270a60c
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 1%

---


# スプライン塗り

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-fill.resources/spline-fill-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力スプラインの内部を白一色で塗りつぶします。 外観は黒の無地で塗りつぶされている。

開いたスプラインは、始点から終点まで直線で閉じられます。 スプライン自体と交差する交点は、これらの交点で線分の内側と外側を反転することによって解決されます。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> [0 ,1]タイル外のスプラインでこのノードを使用することはお勧めしません。 その場合、充填過程は信頼できない。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 入力スプラインを、平坦な黒の背景に対して平坦な白で塗りつぶした結果のイメージ。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-Before.jpg" alt="SplineFill-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-fill.resources/SplineFill-Variant1-After.jpg" alt="SplineFill-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-fill.resources/SplineFill-Demo.gif "ノードの例2")

</td>
</tr>
</table>
