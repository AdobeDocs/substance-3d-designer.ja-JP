---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: '[レンガジェネレータ]ノードを使用して、カスタマイズ可能なサイズ、オフセット、モルタルのプロパティを使用してプロシージャルのレンガパターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レンガジェネレータ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 0%

---


# レンガジェネレータ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

## レンガジェネレータ

**イン：** *テクスチャジェネレーター**/パターン*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

高度なレンガパターンジェネレーター。 人工的なレンガパターンを作成するためのオプションが多数あります

その他のオプションについては、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)を参照してください。

## パラメーター

* **レンガ**: *1 - 64* X方向とY軸の両方のレンガの量を設定します。
* **ベベル**: *0.0 ～ 1.0*&#x200B;レンガのベベルプロファイルを変更します。2方向に変更したり、フォールオフのプロファイルや角の丸みを設定したりできます。
* **縦横比を維持**: *偽/真*&#x200B;ベベルプロファイルをレンガサイズに関連付けるかどうかを指定します。
* **間隔**: *0.0 ～ 1.0*&#x200B;レンガ間の間隔を空けます。 ベベルもギャップを発生させることに注意してください。したがって、ベベルも設定すると、このパラメーターで補正する必要があります。
* **中央のサイズ**: *0.0 ～ 1.0*&#x200B;レンガパターンのオフセット。1列または1行おきにサイズを変更します。
* **Height**: *-1.0 - 1.0* Heightプロファイルを変更します。 輝度のバリエーションやあらゆる種類のランダム化が可能です。
* **勾配**: *-1.0 - 1.0*&#x200B;特定のレンガが斜めに横たわったかのように、レンガごとに勾配を導入します。
* **オフセット**: *0.0 - 1.0*\
  行単位でレンガをオフセットし、行ごとの間隔に影響します。
* **非正方形拡張**: *False/True*\
  スカッシュとストレッチを非正方形の比率で補正できます。

## サンプル画像

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
