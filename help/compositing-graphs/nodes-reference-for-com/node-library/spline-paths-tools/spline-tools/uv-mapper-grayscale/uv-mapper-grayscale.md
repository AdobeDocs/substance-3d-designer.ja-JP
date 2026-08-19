---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale.html"
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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 1%

---


# UVマッパーグレースケール

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/uv-mapper-grayscale-icon.png "ノードアイコン")

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

## 入力コネクタ

<b>UV</b> *カラー*&#x200B;カラー画像の赤(U)チャンネルと緑(V)チャンネルでエンコードされた画像座標。

<b>入力</b> *色* UV入力で指定された座標にマップする必要があるグレースケールイメージです。

## 出力コネクタ

<b>出力</b> *色*&#x200B;入力UV座標を使用して入力イメージをグレースケールイメージとしてマッピングした結果です。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant1-Before.jpg" alt="UVMapper-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapperGrayscale-Variant1-After.jpg" alt="UVMapperGrayscale-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-Before.jpg" alt="UVMapper-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/UVMapper-Variant2-After.jpg" alt="UVMapper-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![ノードの例1](../../../../../../assets/UVMapper-Graph.jpg "ノードの例1")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
