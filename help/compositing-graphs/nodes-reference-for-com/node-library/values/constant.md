---
helpx_url: ""
breadcrumb-title: ''
description: Substance 3D Designerの定数ノードにアクセスして、Substanceグラフの定数値を定義します。
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 定数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---


# 定数

固定ノードは、グラフ内で使用する静的値を作成する手段です。

これらのノードは、ライブラリの&#x200B;**値>定数**&#x200B;セクションにあります。\
これらはすべて、値を生成する単純な[バリュープロセッサー](../../atomic-nodes/value-processor/value-processor.md)ノードを含みます。

+++ ライブラリ内の定数ノード

![constants-library.png](constant.resources/constant-01.png)

+++

<p style="text-align: center;"><img src="./constant.resources/constant-02.png" alt="定数浮動小数ノード" /></p>

## 整数

定数整数は整数を生成し、1段階になります。

[浮動小数](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)に変換できます。これは、加算、減算、単純な比較よりも複雑な処理を行う場合に推奨されます。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![整数型アイコン](constant.resources/constant-03.png "整数型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整数</b>

整数は一つの要素を持つ。 次のような選択を行う際に索引として便利です。

* ユーザーにドロップダウンメニューとして表示されるオプションを選択します（[このページ](../../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)の「ドロップダウンリスト」を参照）。
* [マルチスイッチ](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/multi-switch/multi-switch.md)ノードの入力を選択しています。<b></b>

>[!IMPORTANT]
>
> <b>パラメーター関数の負の整数</b>は&#x200B;*サポートされていません*。 回避策については、[技術的な問題]の[このページ](../../../../technical-issues/parameters-not-working/parameters-not-working-as-expected.md)を参照してください。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer2型アイコン](constant.resources/constant-04.png "Integer2型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>整数2</b>

Integer2ノードは、(X,Y)成分を持つ静的2成分整数ベクトルを生成する。

整数2の一般的な使用例の1つは、[Tile Generator](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)ノードのように、XおよびY グリッドサイズを設定することです。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer3型アイコン](constant.resources/constant-05.png "Integer3型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer3</b>

Integer3ノードは、(X, Y, Z)成分を持つ静的3成分整数ベクトルを生成する。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Integer4型アイコン](constant.resources/constant-06.png "Integer4型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>Integer4</b>

Integer4ノードは、(X, Y, Z, W)成分を持つ静的4成分整数ベクトルを生成する。

</td>
</tr>
</table>

## フロート

定数浮動小数値は小数を生成します。小数点以下の数値がサポートされ、1より小さいステップで調整できます。 （デフォルト： 0.01）

[フロートは整数](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/cast-nodes/cast-nodes.md)に変換できますが、最も近い整数に切り上げまたは切り捨てられます。つまり、データと精度が失われます。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![フロートの種類のアイコン](constant.resources/constant-07.png "フロートの種類のアイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>フロート</b>

Floatは単一の要素を持ち、精度が必要な単一の値に対して非常に一般的に使用されます。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float2型アイコン](constant.resources/constant-08.png "Float2型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮動小数点2</b>

Float2ノードは、(X, Y)成分を持つ2成分ベクトルを生成します。

Float2は、[サンプリング座標](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/sampler-nodes/sampler-nodes.md)、[オフセット変換](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/transforms.md)および一般的な2Dベクトル操作に一般的に使用されます。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float3型アイコン](constant.resources/constant-09.png "Float3型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮動小数点3</b>

Float3ノードは、3成分(X、Y、Z)ベクトルを生成します。

Float3は、主に、[3D SDFノード](../../../../function-graphs/nodes-reference-for-fun/function-node-library/function-node-library.md#sdf-functions)などにおける3Dオブジェクトと[3Dスケール座標](../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/cube-3d/cube-3d.md)を操作する場合や、RGBの色をより簡単に保存する方法（Alphaなし）として使用されます。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![Float4型アイコン](constant.resources/constant-10.png "Float4型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>浮動小数点4</b>

Float4は、4成分(X、Y、Z、W)のベクトルを生成します。

Float4は、[均一カラーノード](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)などのように、XYZW値がRGBAにマップされるカラー情報を格納および設定する方法として推奨されます。

</td>
</tr>
</table>

## 数値以外

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

![ブール型アイコン](constant.resources/constant-11.png "ブール型アイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

<b>ブール値</b>

ブーリアンは最も単純なデータ型で、次の2つの状態のみを認識します： <code>true</code> または<code>false</code>.

この型は、切り替えパラメーターと[If/Else](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md)条件を操作する場合によく使用されます。<br>ブール値は、[スイッチノード](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blending/switch/switch.md)を使用するなど、関数またはグラフのフローを制御する簡単で効率的な方法です。

</td>
</tr>
</table>
