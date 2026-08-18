---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/auto-crop.html"
breadcrumb-title: ''
description: 「自動切り抜き」ノードを使用すると、テクスチャを自動的に切り抜いて、空の境界線を削除し、テクスチャの寸法を最適化することができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Auto Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 自動切り抜き
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# 自動切り抜き

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocropcolor.png){width="200px"}

</td>
</tr>
</table>

**イン：**&#x200B;フィルター*/変換*

**単純**

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**自動切り抜き**&#x200B;ノードは、コンテンツがサイズ変更されずに画像の&#x200B;*中央*&#x200B;に配置されるか、または画像の範囲&#x200B;*に合わせて*&#x200B;サイズが変更されるように、**入力**&#x200B;を調整します。

画像の内容は、**X**&#x200B;および&#x200B;**Y**&#x200B;の&#x200B;*最初と最後のピクセル*&#x200B;に適合するボックスで定義され、その値は0 *より*&#x200B;高い（つまり黒以外）値です。 **カラー**&#x200B;のバージョンでは、ボックスを定義するRGBチャンネルとAlphaチャンネルを選択できます。

</td>
</tr>
</table>

## パラメーター

* **モード** *整数*&#x200B;適用する切り抜き方法を設定します：
  * *正方形の切り抜き*：画像を完全に含めることができる最も小さい&#x200B;*正方形*&#x200B;画像の中心にシェイプが配置されるように、画像が切り抜かれます
  * *自動で切り抜く*：画像を完全に含めることができる最も小さい&#x200B;*正方形または非正方形*&#x200B;画像の中心に画像が切り抜かれます
  * *全体表示（縦横比を維持）*：画像は、*縦横比* （幅と長さの比率）を維持しながら、画像の&#x200B;*フルスパン*&#x200B;にサイズ変更されます
  * *塗りつぶし（伸縮）*：画像は、画像の&#x200B;*全角*&#x200B;に合わせてサイズが変更されます
* **アルファを使用** *ブール値&#x200B;***入力**&#x200B;のアルファチャンネルを使用して、切り抜きのための画像コンテンツの&#x200B;*境界*&#x200B;を決定します。 *False*&#x200B;に設定すると、代わりに黒のピクセルが使用されます。\
  *注意*：このパラメーターは、ノードの&#x200B;**Color**&#x200B;バージョンでのみ使用できます。
* **フィルターモード** *整数*&#x200B;ピクセル間の&#x200B;*補間*&#x200B;でサンプリングされた結果を処理する方法を定義します：
  * *最も近い*: *同じ*&#x200B;値を正確にサンプリングします（高速）
  * *バイリニア*：結果にバイリニアフィルターを適用して、*より滑らかな*&#x200B;外観にします
  * *自動*：選択した&#x200B;**モード**&#x200B;に応じて、上の2つのモードのうち最も適切なモードを切り抜きに使用します

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-demo-01-resized.gif){width="768px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant2.jpg){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant.jpg){width="128px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant4.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-variant3.png){width="256px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../../../assets/autocrop-node.png){width="420px"}

</td>
</tr>
</table>
