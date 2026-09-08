---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/levels.html"
breadcrumb-title: ''
description: 「レベル」ノードを使用して、カラー補正と補正の明るさ、コントラスト、階調範囲のテクスチャを調整します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Levels
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レベル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 4%

---


# レベル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![アトミックノード:レベル](../../../../assets/comp_levels_1.png "アトミックノード:レベル"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

画像のシャドウ、中間調、ハイライトの全体的な階調範囲とカラーバランスを調整します。

レベルノードを使用すると、他の2D画像エディターで使い慣れたヒストグラムインターフェイスに表示される入出力再マップ係数を設定することで、入力のトーンを再マップできます。

</td>
</tr>
</table>

このノードは、Substance 3D Designerの中心的で最も便利なノードの1つです。このノードは、値を変更するための最も正確で正確なインターフェイスを提供するため、グラフの値をリマップおよび調整するために非常によく使用されます。

これは重要なノードですが、一部のユースケースではインターフェイスが少し面倒になる場合があるため、[自動レベル](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/auto-levels/auto-levels.md)、[コントラスト/輝度](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)および[ヒストグラムスキャン](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)で代替策を確認してください。

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

## 例

## パラメーター

このノードには、値を調整するための2つのインターフェイス（ヒストグラムとスライダー）があります。 「特定のパラメーター」ヘッダーバーの右端のボタンを使用して、これらのパラメーターを切り替えることができます。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

ハイライト表示された黄色のボタンで、ヒストグラム（上）の値スライダー（下）のインターフェイスを切り替える

</td>
<td width="66.67%" style="border: 0;" valign="top">

![](../../../../assets/levels-2-1.png)

![](../../../../assets/levels-1-1.png)

</td>
</tr>
</table>

|  |  |
| --- | --- |
| <b>低レベル</b> *浮動小数/浮動小数4* | 入力画像の低照度レベルを指定します。 入力レベルの低い値をブラックにリマップします。 |
| <b>高レベル</b> *浮動小数/浮動小数4* | 入力画像のハイライトレベルを定義します。  入力の高い値を白にリマップします。 |
| <b>中レベル</b> *浮動小数/浮動小数4* | 入力画像の中間調レベルを指定します。  入力Mid値をミッドグレーに再マップします。 |
| <b>低いレベルへ移動</b> *浮動小数/浮動小数4* | 出力画像の低光量を定義します。  黒出力レベルをクランプして限界値を設定します。 |
| <b>レベルアウト高</b> *フロート/フロート4* | 出力画像のハイライトレベルを定義します。  白出力レベルをクランプしてリミットを設定します。 |
| <b>中間クランプ</b> *ブール値* | 出力レベルを計算する前に、変形入力値を[0, 1]にクランプするかどうかを指定します。 |

## 使用方法ガイド

レベルノードとそのヒストグラムエディターの概要については、次のビデオをご覧ください。

### クイックアクション

「特定のパラメーター」ヘッダーバーには、ヒストグラムの便利な機能にアクセスするためのボタンがあります。

![ノードのクイックアクションのレベルを設定する](../../../../assets/levels-2.png "ノードのクイックアクションのレベルを設定する")

<b>1 – 反転：</b> &#39;Level out low&#39;パラメーターと&#39;レベルアウト高&#39;パラメーターの値を入れ替えます。

<b>2 – 自動レベル：</b> &#39;低レベル&#39;パラメーターと&#39;高レベル&#39;パラメーターの値を、それぞれイメージに存在する最小値と最大値に自動で調整します。

<b>3 – インターフェイスの切り替え：</b>ヒストグラムエディターとスライダーエディターを切り替えます。

### ヒストグラム

ヒストグラムエディターは、正確な値があまり必要なく、パラメーターの表示が重要ではない視覚的ですばやく調整できるように設計されています。 レベル補正を使用するには、通常、最も速く簡単な方法です。

![](../../../../assets/levels-histo.gif)

入力タイプ（カラーまたはグレースケール）に応じて、ヒストグラムの上にあるドロップダウンを使用して、変更するチャンネルを選択できます。

### スライダー

スライダーエディターはビジュアルエディターとは連動せず、数値スライダーのみを表示します。これは、非常に正確な値に固定または再マップする場合、または[これらのパラメーターのいずれかを表示](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)する場合などに便利です。スライダーエディターでこれが可能になるのは機能するためです。

スライダーは、カラー入力またはグレースケール入力によって変わります。カラー入力では、RGBAチャンネルごとに4つのスライダーが個別に作成されます。グレースケールには1つのスライダーしかないため、操作が簡単です。 各スライダーの説明については、上記のパラメーターリストを参照してください。

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー*&#x200B;プライマリ | 処理する画像。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
