---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/text.html"
breadcrumb-title: ""
description: テキストノードを使用すると、テキストベースのパターンを作成するためのカスタマイズ可能なフォントとスタイルを使用して、テキストテクスチャを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Text
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: テキスト
user-guide-description: ""
user-guide-title: ""
source-git-commit: 11ab41b58a2dfcb6dd048c55f7a6138a003a2833
workflow-type: tm+mt
source-wordcount: '268'
ht-degree: 1%
---

# テキスト

<table>
<tr style="border: 0;">
<td style="border: 0; width:33.33%; vertical-align:top" width="33.33%" valign="top">

![アトミックノード:テキスト](text.resources/comp_text_1.png "アトミックノード:テキスト"){width="100%"}

<b>イン：</b> アトミックノード

</td>
<td style="border: 0; width:66.66%; vertical-align:top" width="66.66%" valign="top">

「テキスト」ノードを使用すると、ユーザーが作成したテキストをグラフに配置できます。 フォント、アラインメント、回転などの設定を選択して、テキストの位置をカスタマイズすることもできます。

テキストノードは非常に強力で、テキストを簡単に配置する唯一の方法です。 配置は常に限られた正方形のカンバス上で行われ、フォントはシステム定義の外部リストによって決定されるため、使用するのは少し難しい場合があります。

</td>
</tr>
</table>

<table>
<tr style="border: 0">
<td style="border: 0; width: 15%" width="15%"></td>
<td style="border: 0; text-align: center" align="center"><img src="text.resources/text-tooltip.gif" alt="テキストツールヒント" /></td>
<td style="border: 0; width: 15%" width="15%"></td>
</tr>
</table>

Truetype(.ttf)および特定のOpentypeフォントのみがサポートされています。 リストにないフォントがある場合は、それが原因である可能性があります。 <b>フォントをパラメーターとして表示できません。</b>

テキストを使用するグラフがsbsarに公開されると、フォントはビットマップやその他のリソースと同様にパッケージに埋め込まれ、すべてのシステムおよびアプリケーションで動作するようになります。



## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブーリアン* | グレースケールとカラー出力画像を切り替えます。 |
| <b>テキスト</b> *文字列* | テキストの説明を指定します。 |
| <b>フォント</b> *文字列* | テキストのレンダリングに使用するフォントリソース。 |
| <b>フォントサイズ</b> *浮動小数* | テキストのフォントサイズをポイントで指定します。 |
| <b>アラインメント</b> *整数* | テキストのアラインメントを左、中央（デフォルト）、または右に設定します。 |
| <b>変換</b> *浮動小数4* | レンダリングされたテキストに適用される2 x 2の変換行列。 |
| <b>位置</b> *浮動小数2* | 出力画像でのテキストの位置。 |
| <b>背景</b> *浮動小数/浮動小数4* | 出力画像の背景色です。 |
| <b>フォントの色</b> *浮動小数/浮動小数4* | テキストの色。 |

## 入力コネクター

|  |  |
| --- | --- |
| <b>背景</b> *グレースケール/カラー*&#x200B;プライマリ | 出力画像の背景色です。 |


## 例

*近日公開。*
