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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 1%

---


# シェイプマッパー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![シェイプマッパー – アイコン](shape-mapper.resources/shape-mapper-01.png "シェイプマッパー – アイコン"){width="200px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

円または多角形に沿って入力画像を投影します。

投影によって画像がシェイプのアウトラインに合わせて変形され、指定した時間、隙間なく正確に画像にフィットします。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール</i> | 図形に沿って配置するパターンを指定します。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | シェイプに沿ってパターンを投影した結果をグレースケールビットマップで表します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>図形</b> <i>整数</i> | パターンを配置するシェイプのタイプを設定します。<ul data-preserve-html="true"> <li data-preserve-html="true">円</li> <li data-preserve-html="true">多角形ツール</li> </ul> |
| <b>パターン適用量</b> <i>整数</i> | 選択した図形に配置するパターンの量です。 |
| <b>パターンの量でセグメントをリンクする</b> <i>ブール値</i>   *&#39;図形&#39;が&#39;多角形&#39;に設定されている場合に使用できます* | <b>パターンの量</b>を<b>セグメント</b>の数として使用します。   これにより、パターンが角に回り込むことがなくなり、直線的で一貫した外観が得られます。 |
| <b>セグメント</b> <i>整数</i>   *&#39;Shape&#39;が&#39;Polygon&#39;に設定され、&#39;Link segements with pattern amount&#39;が&#39;False&#39;に設定されている場合に使用できます* | パターンが配置されるポリゴンのセグメントの量。   セグメントは&#x200B;*均等なサイズ*、すべての頂点は&#x200B;*中心から等距離*&#x200B;です。セグメントの数を増やすと、多角形が円に向かって収束します。 |
| <b>半径</b> <i>フロート</i> | シェイプの半径の乗数。1.0はイメージの最も短い側の長さの半分です。 |
| <b>幅</b> <i>フロート</i> | シェイプに沿ったパターンの幅の乗数。1.0はイメージの最も短い側の長さの半分です。 |
| <b>回転</b> <i>フロート</i> | 図形に適用する回転角度を、水平方向の右から時計回りに回転する回数で指定します。 |
| <b>1を2つに反転</b> <i>ブール値</i> | 1つおきに図形を垂直方向に反転します。 |
| <b>フィルターリングモード</b> <i>整数</i> | シェイプに沿って配置されたパターンに適用されるフィルターの方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><i>最も近い：</i>最も近い投影ピクセルの値をそのまま適用し、より鮮明で、エイリアスされた外観を実現します。</li> <li data-preserve-html="true"><i>バイリニア：</i>バイリニアフィルターを適用して、投影されたピクセルを隣接するピクセルと補間し、より滑らかで、ぼやけた外観にします。</li> </ul> |
| <b>非正方形の拡張</b> <i>ブール値</i> | 非正方形の画像では、生成されたシェイプが正方形のまま維持され、画像の生成が画像の境界まで拡張されます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
