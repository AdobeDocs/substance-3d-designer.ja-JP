---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ''
description: テキストノードを使用して、テキストベースのパターンを作成するためのカスタマイズ可能なフォントおよびスタイルを持つテキストテクスチャを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: テキスト
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '271'
ht-degree: 1%

---


# テキスト

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomicノード： Text](text.resources/comp_text_1.png "Atomicノード： Text"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

テキストノードを使用すると、ユーザーが作成したテキストをグラフに配置できます。 ユーザーは、フォント、整列、回転などの設定を選択して、テキストの配置をカスタマイズすることもできます。

テキストノードは非常に強力で、テキストを簡単に配置する唯一の方法です。 配置は常に限られた正方形のカンバス上で行われ、フォントはシステム定義の外部リストによって決定されるため、使用するのは少し難しい場合があります。

</td>
</tr>
</table>

Truetype(.ttf)および特定のOpentypeフォントのみがサポートされています。 リストにないフォントがある場合は、それが原因である可能性があります。 <b>フォントをパラメーターとして公開することはできません。</b>

テキストを使用したグラフがsbsarに公開されると、フォントはビットマップやその他のリソースと同様にパッケージに埋め込まれ、すべてのシステムおよびアプリケーションで動作するようになります。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | グレースケールとカラー出力画像を切り替えます。 |
| <b>テキスト</b> *文字列* | テキストの説明を指定します。 |
| <b>フォント</b> *文字列* | テキストのレンダリングに使用するフォントリソース。 |
| <b>フォントサイズ</b> *フロート* | テキストのフォントサイズをポイントで指定します。 |
| <b>整列</b> *整数* | テキストの左揃え、中央揃え（デフォルト）、右揃えを設定します。 |
| <b>変換</b> *浮動小数点4* | レンダリングされたテキストに適用される2 x 2の変換行列。 |
| <b>位置</b> *浮動小数点2* | 出力画像でのテキストの位置。 |
| <b>背景</b> *フロート/フロート4* | 出力画像の背景色です。 |
| <b>フォントの色</b> *フロート/フロート4* | テキストの色。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>背景</b> *グレースケール/カラー*&#x200B;プライマリ | 出力画像の背景色です。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
