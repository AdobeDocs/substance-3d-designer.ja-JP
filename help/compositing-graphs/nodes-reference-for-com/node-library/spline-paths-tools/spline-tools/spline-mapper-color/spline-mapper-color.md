---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-color.html"
breadcrumb-title: ''
description: スプラインマッパーカラーノードを使用して、カスタマイズ可能なパラメータを使用してカラーテクスチャをスプラインパスに沿ってマップします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインマッパーカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '1132'
ht-degree: 0%

---


# スプラインマッパーカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-mapper-color.resources/spline-mapper-color-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力スプラインに沿って伸縮されたプリミティブシェイプに入力カラーイメージをマップします。

プリミティブシェイプは、平面、半円柱、または円柱です。 円柱をスプラインに沿ってツイストすると、それに応じてマッピングされたイメージを変形できます。

</td>
</tr>
</table>

マップされたイメージは、カラー画像として出力されるほか、Height、UV（イメージ座標）、マップされた各スプラインを個別に選択するためのIDマスクなどの他の情報も出力されます。

>[!IMPORTANT]
>
> 非常に低いThickness値を使用すると、スプラインのエンベロープの外側に望ましくないアーティファクトが生じる可能性があります。 これは既知の問題です。

>[!NOTE]
>
> [スプラインマッパーグレースケール](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/spline-mapper-grayscale/spline-mapper-grayscale.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |
| <b>カラーマップ</b> <i>色</i> | 入力スプラインに沿ってマップされる入力カラーイメージ。 |
| <b>高さマップ</b> <i>グレースケール</i> | 入力スプラインに沿ってマップされる入力グレースケール高さマップ。 |
| <b>Twist Curve</b> <i>グレースケール</i> | 1行目のピクセルの値を使用して曲線を表す画像。<br><b>シェイプ</b>パラメーターを<i>半円柱</i>または<i>円柱</i>に設定すると、この入力を使用して、シェイプの周囲のUVのねじれが制御されます。 その影響は、<b>ツイストUVカーブマルチプライヤ</b>パラメータを使用して制御されます。<br>曲線は、スプラインに沿った回転量のプロファイルを提供します。行の最初のピクセルはスプラインの始点での回転で、最後のピクセルは終点での回転です。 グレースケール値は回転の回数を表します。<br>[曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)ノードを使用して曲線を作成できます。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>色</b> <i>色</i> | 入力スプラインに入力カラー画像をカラー画像としてマッピングした結果。 |
| <b>Height</b> <i>グレースケール</i> | 入力スプラインに入力Heightイメージをマッピングした結果(グレースケールイメージ)。 |
| <b>UV</b> <i>色</i> | 入力スプライン全体のマッピングのUV（座標）で、カラー画像にエンコードされます。 |
| <b>ID</b> <i>グレースケール</i> | 入力スプラインに沿ってマップされたイメージのマスク。白い値は、各シェイプを個別に選択できるように、1つのスプラインから次のスプラインに1つずつ増加します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>セグメント数</b> <i>整数</i> | スプラインは、イメージ座標が通過する前にセグメントに単純化されます。<br>セグメントの数が多いほど、曲線に沿ったマッピングがよりスムーズになります。 |
| <b>UVの自動スケール</b> <i>ブール値</i> | 座標のスケールを自動的に調整し、スプラインに沿ってマッピングするときに正方形のイメージを保持します。 |
| <b>UV スケール</b> <i>浮動小数点2</i> | マップされた座標のスケールをX （水平方向）およびY （垂直方向）で調整します。<br>値を大きくすると、画像のタイル密度が高くなります。 |
| <b>モード</b> <i>整数</i> | イメージをマップするスプラインの選択方法：<br>- <i>スプラインの描画</i>：入力リストのすべてのスプラインを使用します。<br>- <i>単一スプラインの描画</i>：指定したインデックスのスプラインのみを使用します。<br>- <i>スプラインの描画</i>：指定した範囲にインデックスが含まれるスプラインのみを使用します。 |
| <b>スプラインインデックスの描画</b> <i>整数</i> | （「モード」が「単一スプラインを描画」に設定されている場合に使用可能）イメージのマッピングに使用するスプラインのインデックス。 |
| <b>スプライン範囲の描画</b> <i>整数2</i> | （「モード」が「スプライン範囲を描画」に設定されている場合に使用可能）イメージをマッピングするスプラインのインデックスの範囲。 |
| <b>開始</b> <i>フロート</i> | マッピングするスプラインの部分の始点をオフセットします。<br>この値は、スプラインの正規化された長さを表します。 |
| <b>終了</b> <i>フロート</i> | マッピングするスプライン部分の終点をオフセットします。<br>この値は、スプラインの正規化された長さを表します。 |
| <b>Thicknessモード</b> <i>整数</i> | マップされたイメージのThicknessを設定するメソッド：<br>- <i>手動</i>：任意の値を使用してThicknessを明示的に設定します；<br>- <i>スプラインから</i>:スプラインのThicknessを使用します。 |
| <b>Thickness</b> <i>フロート</i> | （「Thicknessモード」が「手動」に設定されている場合に使用可能）スプラインに沿ったマップされたイメージのThicknessの任意の値。 |
| <b>Thickness乗数</b> <i>フロート</i> | （[Thicknessモード]が[スプラインから]に設定されている場合に使用可能）マップされたイメージがスプラインに沿ってThicknessするときのグローバルマルチプライヤ。このThicknessはスプラインによって駆動されます。 |
| <b>図形</b> <i>整数</i> | スプラインに沿ったイメージ座標のマッピングに使用されるプリミティブシェイプ：<br>- <i>平面</i>：座標が平面にマッピングされます。<br>- <i>半円柱</i>：座標がスプラインの方向に沿った基本円の軸を持つ半円柱にマッピングされます。<br>- <i>円柱</i>：座標がスプラインの軸に沿った基本円の方向を持つ円柱にマッピングされます。 |
| <b>シリンダHeight乗数</b> <i>フロート</i> | （[形状]が[半円柱]または[円柱]に設定されている場合に使用可能）Height出力における円柱のHeightの割合の強度の乗数。<br>Height調整は累積的です。 |
| <b>円柱Heightのオフセット</b> <i>フロート</i> | （「シェイプ」が「円柱の半分」または「円柱」に設定されている場合に使用可能）円柱または円柱のシェイププロファイルの中心を、スプラインのサーフェスからサーフェスの下の1つの直径にオフセットします。 |
| <b>UVのツイスト強度</b> <i>フロート</i> | （「シェイプ」が「半円柱」または「円柱」に設定されている場合に使用可能）円柱の周囲のイメージのツイストです。<br>ねじれにより、スプラインの端のみで円柱が回転します。 次に、回転がスプラインに沿って補間されます。 |
| <b>ツイストUVカーブマルチプライヤ</b> <i>フロート</i> | （「シェイプ」が「半円柱」または「円柱」に設定されている場合に使用可能）円柱のツイストに対するTwist Curve入力の割合の強度の乗数。<br>曲線は、スプラインに沿った回転量のプロファイルを提供します。行の最初のピクセルはスプラインの始点での回転で、最後のピクセルは終点での回転です。 グレースケール値は回転の回数を表します。 |
| <b>ツイストUVカーブオフセット</b> <i>フロート</i> | （&#39;Shape&#39;が&#39;Half Cylinder&#39;または&#39;Cylinder&#39;の場合に使用可能）Twist Curveによって指定された回転値に対して、回転の回数でグローバルオフセットを適用します。 |
| <b>スプラインHeight乗数</b> <i>フロート</i> | Height出力に対するスプラインHeight入力の影響の強さを調整します。<br>Height調整は累積的です。 |
| <b>入力Height乗数</b> <i>フロート</i> | Height出力に対する高さマップ入力の影響の強さを調整します。<br>Height調整は累積的です。 |
| <b>背景色</b> <i>浮動小数点4</i> | カラー出力の背景色。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。<br>均一な分布にも影響します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-mapper-color.resources/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-mapper-color.resources/SplineMapperColor-Variant1-After.jpg" alt="SplineMapperColor-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-mapper-color.resources/SplineMapperColor-Demo.gif "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例3](spline-mapper-color.resources/SplineMapperColor-Variant1-After1.jpg "ノードの例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
