---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-mapper.html"
breadcrumb-title: ''
description: シェイプマッパーノードを使用して、カスタマイズ可能なトランスフォームと配置を使用して、シェイプをテクスチャにマッピングします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプマッパー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 3%

---


# シェイプマッパー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![シェイプマッパー – アイコン](../../../../../../assets/shape_mapper.png "シェイプマッパー – アイコン"){width="200px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

円または多角形に沿って入力画像を投影します。

投影によって画像がシェイプのアウトラインに合わせて変形され、指定した時間、隙間なく正確に画像にフィットします。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 入力

</td>
<td style="border: 0;" valign="top">

### 出力

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## 入力

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール* | 図形に沿って配置するパターンを指定します。 |

## 出力

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | シェイプに沿ってパターンを投影した結果をグレースケールビットマップで表します。 |

## パラメーター

|  |  |
| --- | --- |
| <b>図形</b>整数 | パターンを配置するシェイプのタイプを設定します。<ul data-preserve-html="true"> <li data-preserve-html="true">円</li> <li data-preserve-html="true">多角形ツール</li> </ul> |
| <b>パターン適用量</b>整数 | 選択した図形に配置するパターンの量です。 |
| <b>パターンの量でセグメントをリンク</b>ブール値&#x200B;*&#39;図形&#39;が&#39;多角形&#39;に設定されている場合に使用できます* | <b>パターンの量</b>を<b>セグメント</b>の数として使用します。   これにより、パターンが角に回り込むことがなくなり、直線的で一貫した外観が得られます。 |
| <b>セグメント</b>整数&#x200B;*&#39;Shape&#39;が&#39;Polygon&#39;に設定され、&#39;Link segments with pattern amount&#39;が&#39;False&#39;に設定されている場合に使用できます* | パターンが配置されるポリゴンのセグメントの量。   セグメントは&#x200B;*均等なサイズ*、すべての頂点は&#x200B;*中心から等距離*&#x200B;です。セグメントの数を増やすと、多角形が円に向かって収束します。 |
| <b>半径</b>浮動小数点 | シェイプの半径の乗数。1.0はイメージの最も短い側の長さの半分です。 |
| <b>幅</b>実数 | シェイプに沿ったパターンの幅の乗数。1.0はイメージの最も短い側の長さの半分です。 |
| <b>回転</b>浮動小数点 | 図形に適用する回転角度を、水平方向の右から時計回りに回転する回数で指定します。 |
| <b>2つ一方を反転</b>ブール値 | 1つおきに図形を垂直方向に反転します。 |
| <b>フィルターモード</b>整数 | シェイプに沿って配置されたパターンに適用されるフィルターの方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>最も近い：</i>最も近い投影ピクセルの値をそのまま適用し、より鮮明で、エイリアスされた外観を実現します。</li> <li data-preserve-html="true"><i>バイリニア：</i>バイリニアフィルターを適用して、投影されたピクセルを隣接するピクセルと補間し、より滑らかで、ぼやけた外観にします。</li> </ul> |
| <b>非正方形の展開</b>ブール値 | 非正方形の画像では、生成されたシェイプが正方形のまま維持され、画像の生成が画像の境界まで拡張されます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
