---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/uv-mapper-color.html"
breadcrumb-title: ''
description: UVマッパーの色ノードを使用して、プロシージャテクスチャ生成用のカラーテクスチャをスプラインに沿ってマップします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > UV Mapper Color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: UVマッパーカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 1%

---


# UVマッパーカラー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/uv-mapper-color-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

UV入力で指定された座標を使用して、入力カラーイメージをマッピングします。

</td>
</tr>
</table>

>[!NOTE]
>
> [UVマッパーグレースケール](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/uv-mapper-grayscale/uv-mapper-grayscale.md)も参照。

## 入力コネクタ

<b>UV</b> *カラー*&#x200B;カラー画像の赤(U)チャンネルと緑(V)チャンネルでエンコードされた画像座標。

<b>入力</b> *カラー* UV入力で指定された座標にマップする必要があるカラー画像です。

## 出力コネクタ

<b>出力</b> *カラー*&#x200B;入力UV座標を使用して入力イメージをカラー画像としてマッピングした結果。

## パラメーター

<b>背景色</b> *Float4*&#x200B;出力画像の背景色です。\
背景は、UVが定義されていない画像領域に表示されます(つまり、値は(0, 0, 0, 0)です)。

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
      <img src="../../../../../../assets/UVMapper-Variant1-After.jpg" alt="UVMapper-Variant1-After">
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
      <img src="../../../../../../assets/UVMapperColor-Variant2-After.jpg" alt="UVMapperColor-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

![グラフのノード](../../../../../../assets/UVMapperColor-Graph.jpg "グラフのノード")

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
