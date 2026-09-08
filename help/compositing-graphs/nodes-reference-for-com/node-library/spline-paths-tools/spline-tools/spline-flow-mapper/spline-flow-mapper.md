---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-flow-mapper.html"
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
source-git-commit: e4c44720897b98db608bc9feabb860d4b1baf332
workflow-type: tm+mt
source-wordcount: '711'
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

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |
| <b>減衰プロファイル曲線</b> <i>グレースケール</i> | <span id="_Hlk135812146"></span>1行目のピクセルの値を使用して曲線を表す画像です。 減衰プロファイルパラメータを入力プロファイルカーブに設定すると、この入力を使用して、スプラインに沿って描画されたフローベクトルデータの減衰に対するグラディエントランプを制御します。<br>[曲線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)ノードを使用して曲線を作成できます。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>色</i> | カラー画像でエンコードされた出力フローマップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>セグメント数</b> <i>整数</i> | スプラインは、ベクトルフローデータが通過する前にセグメントに簡略化されます。 セグメントの数が多いほど、曲線に沿ったフローマッピングがよりスムーズになります。 |
| <b>モード</b> <i>整数</i> | ベクトルフローデータを描画するスプラインの選択方法：<br><br>- <i>スプラインの描画</i>：入力リストのすべてのスプラインを使用します。<br>- <i>単一スプラインの描画</i>：指定したインデックスのスプラインのみを使用します。<br>- <i>スプラインの描画</i>：指定した範囲にインデックスが含まれるスプラインのみを使用します。 |
| <b>スプラインインデックスの描画</b> <i>整数</i> （&#39;Mode&#39;が&#39;Draw Single Spline&#39;に設定されている場合に使用可能） | ベクトルフローデータを描画するスプラインのインデックス。 |
| <b>スプライン範囲の描画</b> <i>整数2</i> （&#39;Mode&#39;が&#39;Draw Spline Range&#39;に設定されている場合に使用可能） | ベクトルフローデータを描画するスプラインのインデックスの範囲。 |
| <b>Thicknessモード</b> <i>整数</i> | 描画されたベクターフローデータのThicknessを設定する方式<br><br>- <i>手動</i>：任意の値を使用してThicknessを明示的に設定します；<br>- <i>スプラインから</i>:スプラインのThicknessを使用します。 |
| <b>Thickness</b> <i>浮動小数</i> （&#39;Thicknessモード&#39;が&#39;手動&#39;に設定されている場合に使用可能） | スプラインに沿って描画されたベクトルフローデータのThicknessを表す任意の値。 |
| <b>Thickness乗数</b> <i>浮動小数</i> （&#39;Thicknessモード&#39;が&#39;スプラインから&#39;に設定されている場合に使用可能） | スプラインに沿って描画されたベクトルフローデータのThicknessのグローバルマルチプライヤ。このThicknessはスプラインによって駆動されます。 |
| <b>方向</b> <i>整数</i> | スプラインに対するベクトルフローの方向です。<br><br>- <i>正接</i>:スプラインの正接ベクトルを使用します。<br>- <i>法線</i>:スプラインの法線ベクトルを使用します。<br>- <i>法線ミラー</i>:スプラインの法線ベクトルのミラーを使用します。 |
| <b>方向を反転</b> <i>ブール値</i> | スプラインの方向を反転します。これは流れベクトルの方向にも影響します。 |
| <b>減衰プロファイル</b> <i>整数</i> | スプラインに沿って描画されたフローベクトルデータの減衰を描画するために使用するグラデーションランプ：<br><br>- <i>線形</i>：線形グラデーションランプを使用します。<br>- <i>ガウス</i>:ガウス式グラデーションランプを使用します。<br>- <i>入力プロファイルカーブ</i>：減衰プロファイル曲線の入力に指定されたカーブをグラデーションランプとして使用します。 |
| <b>減衰の開始</b> <i>ブール値</i> | <span id="_Hlk135769398"></span>スプラインの始点に半円を追加します。 半円は、スプラインと同じ減衰を使用します。 |
| <b>減衰の終了</b> <i>ブール値</i> | スプラインの終点に半円を追加します。 半円は、スプラインと同じ減衰を使用します。 |
| <b>スプラインHeightの減衰</b> <i>フロート</i> | スプラインに沿って描画されたフローベクトルデータの強さは、スプラインのHeightに対して乗算されます。ここで、Heightが0に近づくにつれて、描画されたデータは背景のニュートラル(0.5、0.5、0)カラーにフェードします。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。 これは均一な分布にも影響を与えます。 |

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
