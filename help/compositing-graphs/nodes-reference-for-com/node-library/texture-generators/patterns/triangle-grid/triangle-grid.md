---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/triangle-grid.html"
breadcrumb-title: ''
description: Triangle Gridノードを使用して、Substance 3D Designerで幾何学的テクスチャを作成するための三角形のグリッドパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Triangle Grid
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Triangle Grid
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '1114'
ht-degree: 0%

---


# Triangle Grid

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![](../../../../../../assets/trianglegridgrayscale.jpg){width="200px"}

![](../../../../../../assets/trianglegridcolor.jpg){width="200px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

**Triangle Grid**&#x200B;ノードは、Zダウンの正射投影を使用して、3D空間の&#x200B;*頂点*&#x200B;のうち&#x200B;*三角パッチサーフェス*&#x200B;のグレースケール表現を生成します。

**カラー出力**&#x200B;パラメーターを使用すると、表現に使用するデータを選択でき、様々な表示スタイルを作成できます。\
頂点の&#x200B;*位置*&#x200B;を調整できます。これは、生成されたメッシュに影響します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>Height</b> <i>グレースケール</i>プライマリ | 頂点の&#x200B;*Height* （Z位置）をマップするために使用されるグレースケールイメージの入力です。    この入力の影響は、「Height入力乗数」パラメータによって制御されます。 |
| <b>ベクターマップ</b> <i>色</i> | X軸とY軸の頂点の&#x200B;*ディスプレイスメント*&#x200B;をマップするために使用するカラー画像入力です。    X/Yオフセットは、それぞれイメージのR/Gチャンネルにマップされます。    この入力の影響は、「ベクトルマップディスプレイスメント」パラメーターで制御されます。 |
| <b>カラー入力</b> <i>色</i> | 頂点、セグメント、または三角形の&#x200B;*色*&#x200B;をマップするために使用される色イメージの入力です。    この入力は、「カラーソース」パラメーターが「カラー入力」に設定されている場合に使用されます。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>色</i> | 出力画像。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>カラー出力</b> *整数* | 三角パッチサーフェスを表す方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>頂点単位：</b>各頂点にカラーが割り当てられ、三角形のサーフェス全体に補間されます</li> <li data-preserve-html="true"><b>三角形ごと：</b>三角形ごとに単色が割り当てられます</li> <li data-preserve-html="true"><b>細線</b><b>:</b>は、頂点間のセグメントにアウトラインを適用します</li> <li data-preserve-html="true"><b>エッジまでの距離</b><b>:</b>各三角形の最も近いセグメントまでの距離をレンダリングします</li> <li data-preserve-html="true"><b>中心</b><b>:</b>は、各三角形の重心までの正規化された距離をレンダリングします</li> </ul> |
| <b>三角形化</b> *整数* | サーフェスの三角形化の方法を設定します。つまり、四角形の&#x200B;*対の対向する頂点*&#x200B;を接続する方法を設定します。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>自動：</b>では、2つの頂点が自動的に選択され、結果として三角形が<i>カメラから最も離れた方向を向いています</i><br/> <b>45°:</b>反対側の頂点を接続し、X軸に対して<i>45度</i>回転した線を作成する</li> <li data-preserve-html="true"><b>-45°:</b>反対側の頂点を接続し、X軸に対して線<i>回転–45度</i>を作成</li> <li data-preserve-html="true"><b>水平クインキュックス：</b>頂点の三角形分割の向きを<i>1行おき</i>で交互に指定</li> <li data-preserve-html="true"><b>クインキュックス垂直方向：</b>頂点の三角形分割の向きを<i>1列おき</i>交互に変更<br/> </li> </ul> |
| <b>X金額</b> *整数* | X軸上に生成される頂点の量。 |
| <b>Y金額</b> *整数* | Y軸上に生成される頂点の量。 |
| <b>ランダム位置乗数</b> *フロート* | 主要なワープ効果の強度を調整します。 |
| <b>ランダムな位置</b> *浮動小数点2* | グリッド内の&#x200B;*セルのサイズ*&#x200B;に対して、各頂点のXおよびY位置に適用されるランダムオフセットの強度を調整します。   このオフセット&#x200B;*スタック*&#x200B;は、<b>Quincuxオフセット</b>および<b>ベクトルマップディスプレイスメント</b>のパラメーターを使用します。 |
| <b>ベクトルマップディスプレイスメント</b> *フロート* | <b>ベクトルマップ</b>入力の&#x200B;*サンプリングされた*&#x200B;値を使用して、各頂点に適用される&#x200B;*グローバル*&#x200B;ディスプレイスメント量を調整します。    このオフセット&#x200B;*スタック*&#x200B;は、<b>ランダムな位置</b>および<b>Quincuxオフセット</b>のパラメーターを使用します。 |
| <b>クインキュックスオフセットX</b> *フロート* | 指定したオフセット量を、グリッド内の&#x200B;*セルのサイズ*&#x200B;を基準として、頂点の&#x200B;*行おき*&#x200B;に適用します。   このオフセット&#x200B;*スタック*&#x200B;には、<b>ランダムな位置</b>および<b>ベクターマップディスプレイスメント</b>のパラメーターがあります。 |
| <b>クインキュックスのオフセットY</b> *フロート* | 指定したオフセット量を、グリッド内の&#x200B;*セルのサイズ*&#x200B;を基準として、頂点の&#x200B;*列おきに*&#x200B;適用します。    このオフセット&#x200B;*スタック*&#x200B;には、<b>ランダムな位置</b>および<b>ベクターマップディスプレイスメント</b>のパラメーターがあります。 |
| <b>回転</b> *フロート* | *指定*&#x200B;の回転量を、各頂点の&#x200B;*基本位置*&#x200B;の周りに適用します。つまり、各頂点の位置&#x200B;*前*&#x200B;のランダムオフセットとディスプレイスメントが適用されます。    この回転&#x200B;*スタック*&#x200B;には、<b>回転障害</b>パラメーターがあります。 |
| <b>回転障害</b> *フロート* | *ランダム*&#x200B;な回転量を、*基本位置*&#x200B;の周りの各頂点に適用します。つまり、各頂点の位置&#x200B;*前*&#x200B;のランダムオフセットとディスプレイスメントが適用されます。    この回転&#x200B;*スタック*&#x200B;は、<b>回転</b>パラメーターを使用します。 |
| <b>Height入力乗数</b> *フロート* | <b>Height</b>入力の値&#x200B;*サンプリング*&#x200B;を使用して、各頂点のZ位置を調整します。    このオフセット&#x200B;*スタック*&#x200B;は、<b>Heightランダム</b>パラメーターを使用します。 |
| <b>Heightランダム</b> *フロート* | 各頂点のZ位置にランダムオフセットを適用します。  このオフセット&#x200B;*スタック*&#x200B;は、<b>Height入力乗数</b>パラメーターを使用します。 |
| <b>描画モード</b> *整数* | *重なり合う三角形*&#x200B;の値をブレンドする方法を設定します。 このモードを使用すると、三角形のうち&#x200B;*どの*&#x200B;を表示するかを効果的に選択できます。 <ul data-preserve-html="true"> <li data-preserve-html="true"><b>分：</b>テキスト</li> <li data-preserve-html="true"><b>最大：</b>テキスト</li> <li data-preserve-html="true"><b>深度テスト</b>:テキスト</li> <li data-preserve-html="true"><b>Alphaブレンド：</b>テキスト</li> </ul>注意：使用できる描画モードは、<b>カラー出力</b>パラメーターの値によって異なります。 |
| <b>カラーソース</b> *整数* *&#39;カラー出力&#39;パラメーターが&#39;頂点単位&#39;、&#39;三角形ごと&#39;または&#39;細線&#39;に設定されている場合に使用できます。* | 選択した<b>カラー出力</b>モードに応じて、頂点、三角形、またはセグメントに割り当てる&#x200B;*カラー*&#x200B;の取得方法（輝度）を設定します：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Height</b><b>:</b>頂点のHeightを輝度として使用</li> <li data-preserve-html="true"><b>ランダム</b><b>:</b>ランダムな輝度値を使用</li> <li data-preserve-html="true"><b>色入力</b><b>:</b> <b style="">色入力</b>入力からサンプリングされた値を使用します</li> </ul> |
| <b>カラーソースの不透明度</b> *浮動小数点* *&#39;カラー出力&#39;パラメーターが&#39;細線&#39;に設定されている場合に使用できます。* | 選択した<b>カラーソース</b>から得られる値を使用して、<b>線の色</b>の値の&#x200B;*上書き*&#x200B;を制御します。   注意：この値が1に設定されている場合、<b>線の色</b>パラメーターは影響を受けません。 |
| <b>エッジThicknessまでの距離</b> *浮動小数点* *&#39;カラー出力&#39;パラメーターが&#39;エッジまでの距離&#39;に設定されている場合に使用できます。* | グラデーションのThicknessを設定します。 値が小さいほど、*短い*&#x200B;グラデーションになります。 |
| <b>線の色</b> *Float/Float4* *&#39;カラー出力&#39;パラメーターが&#39;細線&#39;に設定されている場合に使用できます。* | セグメントの輝度値。   注意： <b>カラーソースの不透明度</b>の値が1に設定されている場合、このパラメーターは影響しません。 |
| <b>背景色</b> *Float/Float4* *&#39;カラー出力&#39;パラメーターが&#39;細線&#39;に設定されている場合に使用できます。* | セグメント間に表示される背景の輝度値。   注意： <b>描画モード</b>が&#x200B;*最大*&#x200B;に設定されている場合、背景は予期したとおり&#x200B;*明るい*&#x200B;セグメントを上書きします。 |
| <b>ランダムカラーシードモード</b> *整数* *&#39;カラー出力&#39;パラメーターが&#39;頂点ごと&#39;、&#39;三角形ごと&#39;または&#39;細い線&#39;に設定され、&#39;カラーソース&#39;パラメーターが&#39;ランダム&#39;に設定されている場合に使用できます。* | 擬似ランダムのカラー分布で使用されるシードを取得する方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>グローバルランダムシード</b><b>:</b>は、ノードのグラフからシードを継承します</li> <li data-preserve-html="true"><b>手動シード</b><b>:</b>カスタムの個別シードを使用する</li> </ul> |
| <b>ランダムカラーシード</b> *整数* *&#39;ランダムカラーシードモード&#39;パラメーターが&#39;手動シード&#39;に設定され、&#39;カラーソース&#39;パラメーターが&#39;ランダム&#39;に設定されている場合に使用できます。* | 擬似ランダムのカラー分布で使用される離散シード値。 |
| <b>非正方形拡張</b> *ブール値* | スカッシュとストレッチを非正方形の比率で補正できます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid：例1](../../../../../../assets/triangle_grid_color_example_1.jpg "Triangle Grid：例1"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：例2](../../../../../../assets/trianglegrid-variant2.png "Triangle Grid：例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：例3](../../../../../../assets/trianglegridcolor-variant2.jpg "Triangle Grid：例3"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid：例4](../../../../../../assets/triangle_grid_color_example_2.jpg "Triangle Grid：例4"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：例5](../../../../../../assets/trianglegridcolor-variant4.jpg "Triangle Grid：例5"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid：例6](../../../../../../assets/trianglegridcolor-variant3.jpg "Triangle Grid：例6"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![Triangle Grid:レザー](../../../../../../assets/trianglegrid-demo.png "Triangle Grid:レザー"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![Triangle Grid:グラフ](../../../../../../assets/trianglegrid-node.png "Triangle Grid:グラフ"){zoomable="yes"}

</td>
</tr>
</table>
