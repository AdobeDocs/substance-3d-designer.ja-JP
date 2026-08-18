---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-mapper-color.html"
breadcrumb-title: ''
description: スプラインマッパーの色ノードを使用して、カスタマイズ可能なパラメータを使用してスプラインパスに沿ってカラーテクスチャをマッピングします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Point List
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインマッパーカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '1120'
ht-degree: 0%

---


# スプラインマッパーカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-mapper-color-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力スプラインに沿ってストレッチされたプリミティブシェイプに、入力カラー画像をマッピングします。

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

## 入力コネクタ

<b>スプライン座標</b> *色*&#x200B;入力スプラインの点の座標は、カラー画像のRGBAチャンネルでエンコードされています：\
<b> R</b> - X位置\
<b> G</b> - Y位置\
<b> B</b> - Height\
    <b>A</b> – パックされたデータ：\
        *記号：スプラインが閉じている（負）か、開いている（正）;\
        *絶対値：Thickness + 1。

<b>スプラインデータ</b> *色*&#x200B;カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データです。\
<b> R</b> – 接線X\
<b> G</b> – 接線Y\
<b> B</b> – 未使用\
<b> A</b> – 未使用

<b>スプラインの量</b> *整数*&#x200B;入力スプラインの数です。

<b>カラーマップ</b> *色*&#x200B;入力スプラインに沿ってマップする必要がある入力カラー画像です。

<b>Heightマップ</b> *グレースケール*&#x200B;入力スプラインに沿ってマップする必要がある入力グレースケールのHeightマップです。

<b>Twist Curve</b> *グレースケール*&#x200B;最初のピクセル行の値を使用して曲線を表す画像です。\
<b>シェイプ</b>パラメーターを&#x200B;*半円柱*&#x200B;または&#x200B;*円柱*&#x200B;に設定すると、この入力を使用して、シェイプの周囲のUVのねじれが制御されます。 その影響は、<b>ツイストUVカーブマルチプライヤ</b>パラメータを使用して制御されます。\
曲線は、スプラインに沿った回転量のプロファイルを提供します。行の最初のピクセルはスプラインの始点での回転で、最後のピクセルは終点での回転です。 グレースケール値は回転の回数を表します。\
[曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)ノードを使用して曲線を作成できます。

## 出力コネクタ

<b>色</b> *色*&#x200B;入力スプラインに入力カラー画像をカラー画像としてマッピングした結果。

<b>Height</b> *グレースケール*&#x200B;入力スプラインに入力Heightイメージをグレースケールイメージとしてマッピングした結果です。

<b>UV</b> *カラー*&#x200B;入力スプライン全体のマッピングのUV （座標）で、カラー画像にエンコードされます。

<b>ID</b> *グレースケール*&#x200B;入力スプラインに沿ってマップされたイメージのマスクです。白い値は、各シェイプを個別に選択できるように、スプライン間で1つずつ増加します。

## パラメーター

<b>セグメント数</b> *整数*&#x200B;スプラインは、イメージ座標が通過する前にセグメントに簡略化されます。\
セグメントの数が多いほど、曲線に沿ったマッピングがスムーズになります。

<b>UVの自動スケール</b> *ブール値*&#x200B;スプラインに沿ってマッピングするときに正方形のイメージを保持するように、座標のスケールを自動的に調整します。<b></b>

<b>UV スケール</b> *Float2* X （水平方向）およびY （垂直方向）にマップされた座標のスケールを調整します。\
値が大きいほど、画像のタイルの密度が高くなります。<b></b>

<b>モード</b> *整数*&#x200B;イメージをマップするスプラインを選択する方法：\
*– スプラインリストの描画*：入力リストのすべてのスプラインが使用されます。\
*– 単一スプラインの描画*：指定されたインデックスを持つスプラインのみが使用されます。\
*– スプライン範囲の描画*：指定された範囲にインデックスが含まれるスプラインのみが使用されます。

<b>スプラインインデックスの描画</b> *整数* （&#39;Mode&#39;が&#39;Draw Single Spline&#39;に設定されている場合に使用可能）イメージをマップする際のスプラインのインデックスです。

<b>スプライン範囲の描画</b> *Integer2* （&#39;Mode&#39;が&#39;Draw Spline Range&#39;に設定されている場合に使用可能）イメージをマップするスプラインのインデックスの範囲。

<b>開始</b> *フロート*&#x200B;マップするスプラインの部分の始点をオフセットします。\
この値は、スプラインの正規化された長さを表します。

<b>終了</b> *フロート*&#x200B;マップするスプラインの端をオフセットします。\
この値は、スプラインの正規化された長さを表します。

<b>Thicknessモード</b> *整数*&#x200B;マップされたイメージのThicknessを設定するメソッド：\
*– 手動*: Thicknessを任意の値で明示的に設定します。\
*– スプラインから*:スプラインのThicknessを使用します。

<b>Thickness</b> *フロート* （&#39;Thicknessモード&#39;が&#39;手動&#39;に設定されている場合に使用可能）スプラインに沿ったマップされたイメージのThicknessの任意の値。<b></b>

<b>Thickness乗数</b> *フロート* （&#39;Thicknessモード&#39;が&#39;スプラインから&#39;に設定されている場合に使用可能）マップされたイメージがスプラインに沿ってThicknessするときのグローバルマルチプライヤ。このThicknessはスプラインによって駆動されます。

<b>図形</b> *整数*&#x200B;スプラインに沿ってイメージ座標をマップするために使用されるプリミティブシェイプ：\
*– 平面*：座標が平面にマップされています；\
*– 半円柱*：座標は、基本円の軸がスプラインの方向に従う半円柱にマップされます。\
*– 円柱*：座標は、基本円の軸がスプラインの方向に従う円柱にマップされます。<b></b>

<b>シリンダHeight乗数</b> *フロート* （&#39;Shape&#39;が&#39;Half Cylinder&#39;または&#39;Cylinder&#39;に設定されている場合に使用可能）Height出力における円柱のHeightの割合の強度の乗数。\
Height調整は累積的です。

<b>円柱Heightのオフセット</b> *フロート* （&#39;Shape&#39;が&#39;Half Cylinder&#39;または&#39;Cylinder&#39;に設定されている場合に使用可能） \
円柱または半円柱のシェイププロファイルの中心をスプラインのサーフェスからサーフェスの下の1つの直径にオフセットします。

<b>UVのツイスト強度</b> *フロート* （&#39;Shape&#39;が&#39;Half Cylinder&#39;または&#39;Cylinder&#39;に設定されている場合に使用可能）画像のねじれ。円柱の周りを回転します。\
ねじれでは、スプラインの端の円柱のみが回転します。 次に、回転がスプラインに沿って補間されます。

<b>ツイストUVカーブマルチプライヤ</b> *フロート* （&#39;Shape&#39;が&#39;Half Cylinder&#39;または&#39;Cylinder&#39;に設定されている場合に使用可能）Twist Curve入力の強さが円柱のねじれに与える影響の乗数。\
曲線は、スプラインに沿った回転量のプロファイルを提供します。行の最初のピクセルはスプラインの始点での回転で、最後のピクセルは終点での回転です。 グレースケール値は回転の回数を表します。

<b>ツイストUVカーブオフセット</b> *フロート* （&#39;Shape&#39;が&#39;Half Cylinder&#39;または&#39;Cylinder&#39;に設定されている場合に使用可能）Twist Curveによって指定された回転値に対して、回転の回数でグローバルオフセットを適用します。

<b>スプラインHeight乗数</b> *フロート* Height出力に対するスプラインHeight入力の影響の強さを調整します。\
Height調整は累積的です。<b></b>

<b>入力Height乗数</b> *浮動小数点* Height出力に対するHeightマップ入力の影響の強さを調整します。\
Height調整は累積的です。<b></b>

<b>背景色</b> *Float4*&#x200B;カラー出力の背景色です。

<b>非正方形の補正&#x200B;</b>*ブール値*&#x200B;ポイントの位置とThicknessを調整して、非正方形の解像度でスプラインのシェイプを保持します。\
これは均一な分布にも影響を与えます。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-Before.jpg" alt="SplineMapperColor-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineMapperColor-Variant1-After.jpg" alt="SplineMapperColor-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineMapperColor-Demo.gif "ノードの例2")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例3](../../../../../../assets/SplineMapperColor-Variant1-After1.jpg "ノードの例3")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
