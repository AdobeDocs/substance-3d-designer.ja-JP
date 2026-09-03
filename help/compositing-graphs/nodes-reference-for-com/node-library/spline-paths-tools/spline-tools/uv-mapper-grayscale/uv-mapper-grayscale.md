---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
breadcrumb-title: ''
description: UVマッパーグレースケールノードを使用して、手続き型テクスチャ生成用にスプラインに沿ってグレースケールテクスチャをマップします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UVマッパーグレースケール
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '142'
ht-degree: 2%

---


# UVマッパーグレースケール

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](uv-mapper-grayscale.resources/uv-mapper-grayscale-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

UV入力で指定された座標を使用して、入力グレースケールイメージをマップします。

</td>
</tr>
</table>

>[!NOTE]
>
> [UVマッパーカラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-color/uv-mapper-color.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>UV</b> <i>色</i> | カラー画像の赤(U)チャンネルと緑(V)チャンネルでエンコードされた画像座標。 |
| <b>入力</b> <i>色</i> | UV入力で指定された座標にマップするグレースケールイメージ。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>色</i> | 入力UV座標を使用して入力画像をグレースケールイメージとしてマッピングした結果。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-02.jpg" alt="UVMapper-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-03.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-04.jpg" alt="UVMapper-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="uv-mapper-grayscale.resources/uv-mapper-grayscale-05.jpg" alt="UVMapper-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![ノードの例1](uv-mapper-grayscale.resources/uv-mapper-grayscale-06.jpg "ノードの例1")
