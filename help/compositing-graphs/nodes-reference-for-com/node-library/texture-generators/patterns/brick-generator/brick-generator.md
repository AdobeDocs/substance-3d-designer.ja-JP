---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: '[レンガジェネレータ]ノードを使用して、サイズ、オフセット、モルタルのプロパティをカスタマイズ可能な手続き型のレンガパターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レンガジェネレータ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
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

高度なレンガパターンジェネレータ。 人工的なレンガのパターンを生成するためのオプションが多数あります

その他のオプションについては、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)を参照してください。

## パラメーター

* **レンガ**: *1 ～ 64* X軸とY軸の両方でレンガの量を設定します。
* **ベベル**: *0.0 ～ 1.0*&#x200B;れんがのベベルプロファイルを変更します。2方向に変更したり、フォールオフプロファイルや角の丸みを設定したりできます。
* **縦横比を維持**: *偽/真*&#x200B;ベベルプロファイルをブリックサイズに関連付けるかどうかを指定します。
* **間隔**: *0.0 ～ 1.0*&#x200B;レンガの間に残す間隔。 ベベルもギャップを発生させることに注意してください。したがって、ベベルも設定すると、このパラメーターで補正する必要があります。
* **中央のサイズ**: *0.0 ～ 1.0*&#x200B;レンガのパターンのオフセット。1列または1行おきにサイズを変更します。
* **Height**: *-1.0 - 1.0* Heightプロファイルを変更します。 輝度のバリエーションやあらゆる種類のランダム化を導入できます。
* **勾配**: *-1.0 - 1.0*&#x200B;特定のレンガが斜めに並んでいるかのように、レンガごとに勾配を設定します。
* **オフセット**: *0.0 - 1.0*\
  れんがを行単位でオフセットし、行ごとの間隔に影響します。
* **非正方形拡張**: *False/True*\
  スカッシュとストレッチを非正方形の比率で補正できます。

## サンプル画像

![](../../../../../../assets/brick-generator-ex-01.gif)

![](../../../../../../assets/brick-generator-ex-02.gif)

</td>
</tr>
</table>
