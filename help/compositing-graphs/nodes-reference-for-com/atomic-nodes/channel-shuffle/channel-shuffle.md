---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/channel-shuffle.html"
breadcrumb-title: ''
description: チャンネルシャッフルノードを使用して、テクスチャのカラーチャンネルを再配置し、カラーエフェクトやチャンネルの入れ替えを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Channels shuffle
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: チャンネルシャッフル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 7%

---


# チャンネルシャッフル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![アトミックノード：チャンネルの移動](channel-shuffle.resources/channel-shuffle-01.png "アトミックノード：チャンネルの移動"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

1 つまたは 2 つの入力画像のカラーチャンネルを出力画像に再配置します。

つまり、2つの入力を受け取り、赤、緑、青、Alphaのチャンネルが入れ替えられたり、入力のチャンネルのいずれかにセットされた場合、出力を返すことができます。

基本的には、RGBチャンネルをパックしたり、可能な方法で入れ替えたりすることができます。 グレースケール入力は、カラー（赤、緑、青、Alpha）と同様に扱われ、すべて同じ値を返します。

</td>
</tr>
</table>

チャンネルの移動には基本的なオプションがありますが、チャンネルパッキングまたは取り消しおよびAlphaチャンネルの設定では、ほとんどの場合、[RGBAマージ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-merge/rgba-merge.md)、[RGBAスプリット](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/rgba-split/rgba-split.md)、[Alphaの結合](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-merge/alpha-merge.md)および[Alphaの分割](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)を使用する方が簡単です。 これらは、複数のパラメーターを変更したり、後でグレースケールに変換したりする必要のないデフォルトのアクションを実行するように設定されています。 より高度なバージョンと、より多くの描画オプションをお探しの場合は、[チャンネルミキサー](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/channel-mixer/channel-mixer.md)をご覧ください。

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
| <b>レッドチャンネル</b> *整数* | 出力画像の赤チャンネルに挿入するソースチャンネルを選択します。 |
| <b>グリーンチャンネル</b> *整数* | 出力画像のグリーンチャンネルに挿入するソースチャンネルを選択します。 |
| <b>ブルーチャンネル</b> *整数* | 出力画像の青チャンネルに挿入するソースチャンネルを選択します。 |
| <b>Alphaチャンネル</b> *整数* | 出力画像のAlphaチャンネルに挿入するソースチャンネルを選択します。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力1</b> *カラー/グレースケール*&#x200B;プライマリ | プライマリ入力画像。 |
| <b>入力2</b> *カラー/グレースケール* | セカンダリ入力イメージ： |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
