---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/paths-vertex-processor.html"
breadcrumb-title: ''
description: 「パス」頂点プロセッサーノードを使用すると、詳細オプションを使用してパス頂点を変形および操作できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Paths Vertex Processor
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Paths 頂点プロセッサ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '434'
ht-degree: 1%

---


# Paths 頂点プロセッサ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](paths-vertex-processor.resources/paths-vertex-processor-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力<b>パス</b>の頂点位置に変換を適用します。

ノードは次のように使用する必要があります。

1. <b>頂点単位関数 </b>パラメーター関数を編集します；
1. <b>Get Float2</b>ノードを使用して取得します。*vertex.pos*、*prev.pos*&#x200B;および&#x200B;*next.pos*&#x200B;変数
1. これらの値に対していくつかの操作を行います（例：これらの値を乗算してパスを拡大/縮小します）。
1. 計算結果を出力として設定します。

</td>
</tr>
</table>

*prev.pos*&#x200B;または&#x200B;*next.pos*&#x200B;を照会する前に、適切な<b>以前のアクセス頂点</b>と<b>次のアクセス頂点</b>の値を設定してください\
また、入力画像を追加して、関数からサンプルすることもできます。 関数からサンプリングできるようにするには、まず入力を接続する必要があります。 （最初の入力は&#x200B;*画像1*&#x200B;です。）\
*prev[2].pos* (Float2)、*next[2].pos* (Float2)、*vertex.corner* (bool)および&#x200B;*path.id* (float)変数にアクセスすることもできます。

>[!TIP]
>
> 上級ユーザー向けに、[パス形式の仕様](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)では、パスのデータがカラー画像にエンコードされる方法について説明し、このデータを直接操作するためのヒントを提供します。

>[!NOTE]
>
> [Paths 頂点プロセッサシンプル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor-1/paths-vertex-processor-simple.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | エンコードされたセグメントパスのリスト。 この入力を、[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別の&#x200B;*パス*&#x200B;処理ノードに接続します。 |
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
| <b>前のアクセス頂点</b> <i>整数</i> | このパラメーターを使用すると、<b>path</b>パラメーター関数の<b>Get</b>ノードを使用して、頂点単位関数 (*prev.pos*)および前の頂点(*prev[2].pos*)に沿った前の頂点の場所を取得できます。 |
| <b>次にアクセスされた頂点</b> <i>整数</i> | このパラメーターを使用すると、<b>path</b>パラメーター関数の<b>Get</b>ノードを使用して、頂点単位関数 (*next.pos*)に沿った次の頂点の位置と、次の頂点(*next[2].pos*)を取得できます。 |
| <b>画像入力数</b> <i>整数</i> | <b>頂点単位関数</b>パラメーター関数でサンプリングする必要があるイメージを接続するための表示可能な<b>入力#</b>入力コネクタの数。<br>必要なサンプルをすべて設定したら、このパラメーターの値を0に戻すことにより、未使用のピンを非表示にすることができます。 |
| <b>頂点単位関数</b> <i>浮動小数点2</i> | 各頂点に適用される関数。 新しい頂点位置を返す必要があります。<br>ガイダンスについては、このページの<b>説明</b>セクションを参照してください。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例2](paths-vertex-processor.resources/paths-vertex-processor-02.gif "ノードの例2")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
