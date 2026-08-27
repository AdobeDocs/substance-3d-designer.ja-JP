---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
breadcrumb-title: ''
description: スプラインフローマッパーノードを使用して、スプラインパスに沿って流れるテクスチャパターンを作成し、有機的な効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Flow Mapper
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインフローマッパー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 0%

---


# スプラインフローマッパー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/spline-flow-mapper-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力スプラインに沿ってフローベクトルデータが描画されるフローマップを描画します。

これにより、スプラインを使用して、流れの向き、軌道、強さ、Thicknessを制御したり、グラデーションランプを使用して描画したデータを中間色の背景にフェードしたりできます。

</td>
</tr>
</table>

>[!IMPORTANT]
>
> 非常に低いThickness値を使用すると、スプラインのエンベロープの外側に望ましくないアーティファクトが生じる可能性があります。 これは既知の問題です。

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

<b>減衰プロファイル曲線</b> *グレースケール*<span id="_Hlk135812146"></span>&#x200B;最初のピクセル行の値を使用して曲線を表す画像です。\
減衰プロファイルパラメータを入力プロファイルカーブに設定すると、この入力を使用して、スプラインに沿って描画されたフローベクトルデータの減衰に対するグラディエントランプを制御します。\
[曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)ノードを使用して曲線を作成できます。

## 出力コネクタ

<b>出力</b> *色*&#x200B;カラー画像にエンコードされた出力フローマップです。

## パラメーター

<b>セグメント数</b> *整数*&#x200B;スプラインは、ベクトルフローデータが通過する前にセグメントに簡略化されます。\
セグメントの数が多いほど、曲線に沿ったフローマッピングがよりスムーズになります。

<b>モード</b> *整数*&#x200B;ベクトルフローデータを描画するスプラインの選択方法：\
*– スプラインリストの描画*：入力リストのすべてのスプラインが使用されます。\
*– 単一スプラインの描画*：指定されたインデックスを持つスプラインのみが使用されます。\
*– スプライン範囲の描画*：指定された範囲にインデックスが含まれるスプラインのみが使用されます。

<b>スプラインインデックスの描画</b> *整数* （&#39;Mode&#39;が&#39;Draw Single Spline&#39;に設定されている場合に使用可能）ベクトルフローデータを描画するスプラインのインデックスです。

<b>スプライン範囲の描画</b> *Integer2* （&#39;Mode&#39;が&#39;Draw Spline Range&#39;に設定されている場合に使用可能）ベクトルフローデータを描画するスプラインのインデックスの範囲。

<b>Thicknessモード</b> *整数*&#x200B;描画されたベクターフローデータのThicknessを設定する方式です\
*– 手動*: Thicknessを任意の値で明示的に設定します。\
*– スプラインから*:スプラインのThicknessを使用します。

<b>Thickness</b> *Float* （&#39;Thicknessモード&#39;が&#39;手動&#39;に設定されている場合に使用可能）スプラインに沿って描画されたベクターフローデータのThicknessの任意の値。<b></b>

<b>Thickness乗数</b> *フロート* （[Thicknessモード]が[スプラインから]に設定されている場合に使用可能）スプラインに沿って描画されたベクトルフローデータのThicknessのグローバルマルチプライヤ。このThicknessはスプラインによって駆動されます。

<b>方向</b> *整数*&#x200B;スプラインに対するベクトルフローの方向です。\
*– 接線*:スプラインの接線ベクトルを使用します。\
*– 法線*:スプラインの法線ベクトルを使用します。\
*– 法線ミラー*:スプラインの法線ベクトルのミラー化されたバージョンを使用します。

<b>方向を反転</b> *ブール値*&#x200B;スプラインの方向を反転します。これは流れベクトルの方向にも影響します。

<b>減衰プロファイル</b> *整数*&#x200B;スプラインに沿って描画されたフローベクトルデータの減衰を描画するために使用されるグラデーションランプ：\
*– 線形*：線形グラデーションランプを使用します；\
*– ガウス*:ガウスグラデーションランプを使用します\
*– プロファイルカーブの入力*：減衰プロファイルカーブの入力に指定されたカーブをグラデーションランプとして使用します。

<b>減衰の開始</b> *ブール演算式*<span id="_Hlk135769398"></span>&#x200B;スプラインの始点に半円を追加します。 半円は、スプラインと同じ減衰を使用します。

<b>減衰の終了</b> *ブール演算式*&#x200B;スプラインの終点に半円を追加します。 半円は、スプラインと同じ減衰を使用します。

<b>スプラインHeightの減衰</b> *フロート*&#x200B;スプラインに沿って描画されたフローベクトルデータの強さは、スプラインのHeightに対して乗算されます。ここで、描画されたデータは、Heightが0に近づくにつれて、背景のニュートラル(0.5、0.5、0)色にフェードします。

<b>非正方形の補正&#x200B;</b>*ブール値*&#x200B;ポイントの位置とThicknessを調整して、非正方形の解像度でスプラインのシェイプを保持します。\
これは均一な分布にも影響を与えます。

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-Before.jpg" alt="SplineFlowMapper-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/SplineFlowMapper-Variant1-After.jpg" alt="SplineFlowMapper-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/SplineFlowMapper-Demo.gif "ノードの例2")

</td>
</tr>
</table>
