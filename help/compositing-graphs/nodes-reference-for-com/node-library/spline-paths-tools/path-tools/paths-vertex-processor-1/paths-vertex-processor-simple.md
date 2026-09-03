---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor-simple.html"
breadcrumb-title: ''
description: パスの頂点プロセッサーシンプルノードを使用すると、パスの頂点を簡単な変形オプションで処理できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor Simple
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パス頂点プロセッサシンプル
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '327'
ht-degree: 1%

---


# パス頂点プロセッサシンプル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力<b>パス</b>の頂点位置に変換を適用します。

1. <b>頂点単位関数</b>パラメーター関数を編集します；
1. <b>Get 浮動小数2</b>ノードを&#x200B;*頂点.pos*&#x200B;変数として使用します。
1. この値に対していくつかの操作を行います（例：乗算してパスを拡大・縮小）。
1. 計算結果を出力として設定します。

</td>
</tr>
</table>

入力画像を使用して、関数からサンプルできます。 関数からサンプリングできるようにするには、まず入力を接続する必要があります。 （最初の入力は&#x200B;*画像1*&#x200B;です。）\
*path.corner* (bool)および&#x200B;*頂点.id* (float)変数にアクセスすることもできます。

>[!TIP]
>
> 上級ユーザー向けに、[パス形式の仕様](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)では、パスのデータがカラー画像にエンコードされる方法について説明し、このデータを直接操作するためのヒントを提供します。

>[!NOTE]
>
> [Paths 頂点プロセッサ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。 |
| <b>入力#</b> <i>カラー/グレースケール</i> | <b>頂点単位関数</b>パラメーター関数でサンプリングする必要があるイメージの入力。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | 変換されたパス。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>画像入力数</b> <i>整数</i> | <b>頂点単位関数</b>パラメーター関数でサンプリングする必要があるイメージを接続するための表示可能な<b>入力#</b>入力コネクタの数。<br>必要なサンプルをすべて設定したら、このパラメーターの値を0に戻すことにより、使用されていないピンを非表示にすることができます。<br>入力を増やす場合は、代わりに[Paths 頂点ープロセッサー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)を使用してください。 |
| <b>頂点単位関数</b> <i>浮動小数2</i> | 各頂点に適用される関数。 新しい頂点位置を返す必要があります。<br>ガイダンスについては、このページの<b>説明</b>セクションを参照してください。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例2](paths-vertex-processor-simple.resources/paths-vertex-processor-simple-02.gif "ノードの例2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
