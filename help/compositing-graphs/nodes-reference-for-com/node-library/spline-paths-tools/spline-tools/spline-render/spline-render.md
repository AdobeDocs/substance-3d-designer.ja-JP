---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-render.html"
breadcrumb-title: ''
description: '[スプラインレンダリング]ノードを使用すると、カスタマイズ可能な幅、色、描画モードを持つテクスチャとしてスプラインをレンダリングできます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Render
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインレンダリング
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '810'
ht-degree: 0%

---


# スプラインレンダリング

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-render.resources/spline-render-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力<b>スプライン</b>に沿ったセグメントの文字列を、入力<b>背景</b>上に描画します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>背景</b> <i>グレースケール</i> | スプラインを描画するグレースケールイメージ。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 入力スプラインをバックグラウンドの上に描画した結果イメージ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>モード</b> <i>整数</i> | 描画するスプラインの選択方法：<br>- <i>スプライン一覧の描画</i>：入力リストのすべてのスプラインを描画します。<br>- <i>単一スプラインの描画</i>：入力リストから指定されたスプラインのみを描画します。<br>- <i>スプライン範囲の描画</i>：入力リストから指定された範囲のスプラインのみを描画します。 |
| <b>スプラインインデックスの描画</b> <i>整数</i> | （「モード」が「単一スプラインを描画」に設定されている場合に使用可能）描画するスプラインのインデックスです。 |
| <b>スプライン範囲の描画</b> <i>整数2</i> | （「モード」が「スプライン範囲を描画」に設定されている場合に使用可能）描画する必要があるスプラインのインデックスの範囲。 |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | 各スプラインには、スプラインの始点に点を描き、終点に矢印を描きます。 |
| <b>セグメント数</b> <i>整数</i> | スプラインに沿って描画されるセグメントの数を調整します。<br>値を大きくすると、より滑らかな線になります。 |
| <b>エンベロープスプラインの量</b> <i>整数</i> | 各スプラインのThicknessに沿って描画する重複セグメントの数。 |
| <b>開始</b> <i>フロート</i> | スプラインの描画する部分の始点をオフセットします。<br>この値は、スプラインの正規化された長さを表します。 |
| <b>終了</b> <i>フロート</i> | 描画するスプライン部分の終点をオフセットします。<br>この値は、スプラインの正規化された長さを表します。 |
| <b>Thicknessサイズモード</b> <i>整数</i> | 描画された線分のThicknessを計算する方式： <br>- <i>Image</i>：この値はテクスチャ空間で正規化されます（1は画像の全幅）。 Thicknessはテクスチャ解像度を基準にしています。<br>- <i>Pixel</i>：値はテクスチャ内の絶対ピクセル数で、1は完全なピクセルです。 Thicknessは、テクスチャ解像度とは別のものです。 |
| <b>Thickness （画像）</b> <i>フロート</i> | （「Thicknessサイズモード」が「画像」に設定されている場合に使用可能）描画したセグメントのThicknessをテクスチャスペースで正規化します。1は画像の全幅です。 |
| <b>Thickness (px)</b> <i>フロート</i> | （「Thicknessサイズモード」が「ピクセル」に設定されている場合に使用可能）描画されたセグメントのThicknessを、テクスチャ内の絶対ピクセル数で指定します。1は完全なピクセルです。 |
| <b>ジョイントを有効にする</b> <i>ブール値</i> | スプラインに沿って描画された個々のセグメント間のギャップを、ディスクを使用して埋めます。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。<br>均一な分布にも影響します。 |
| <b>色</b> |  |
| <b>背景の適用度</b> <i>フロート</i> | 値に背景入力画像を掛けた値。 |
| <b>スプラインスタイル</b> <i>整数</i> | スプラインに色を付けるために使用された方式：<br>- <i>実線</i>：線分は均一なグレースケール値を使用して描画されます。<br>- <i>グラデーション</i>：線分の各文字列に沿って開始から終了まで黒から白へのグラデーションが適用されます。<br>- <i>Height</i>:スプラインのHeightは、線分を描画するためのグレースケール値として使用されます。 |
| <b>スプラインの色</b> <i>フロート</i> | セグメントの描画に使用する均一のグレースケール値。<br>[実線]以外のスプラインスタイルを選択すると、この色はスタイル設定された色に対して乗算されます。 |
| <b>ランダムな輝度</b> <i>フロート</i> | スプライン内のカットされていないセグメントの各文字列に対して、その文字列の描画に使用されるグレースケール値に対して、指定した範囲のランダムオフセットを適用します。 |
| <b>描画モード</b> <i>整数</i> | スプラインに沿って描画された背景と重なり合うセグメントの色をブレンドする方法： <br>- <i>最大</i>：最も明るい値が使用されます。<br>- <i>追加</i>：値が一緒に追加されます。 |
| <b>ランダムなセグメント</b> |  |
| <b>ランダムセグメントの開始</b> <i>フロート</i> | スプラインの始点に近いセグメントの文字列が切り取られる確率を調整します。 |
| <b>ランダムセグメントの終了</b> <i>フロート</i> | スプラインの端に近いセグメントの文字列が切り取られる確率を調整します。 |
| <b>ランダムオフセット</b> <i>フロート</i> | 各切断セグメントの法線に沿って適用されるディスプレイスメントの最大量を設定します。<br>このパラメーターは、StartとEndの両方が0に設定されている場合は無効です。 |
| <b>ランダムオフセットの中心</b> <i>フロート</i> | 各切断セグメントに適用されるランダムディスプレイスメントの中心を、その法線に沿ってオフセットします。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/SplineRender-Variant2-Before.jpg" alt="SplineRender-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-render.resources/SplineRender-Variant2-After.jpg" alt="SplineRender-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-render.resources/SplineRender-Variant1-After.jpg" alt="SplineRender-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-render.resources/SplineRender-Variant1-Before.jpg" alt="SplineRender-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-render.resources/SplineRender-Variant3.jpg" alt="SplineRender-Variant3">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例1](spline-render.resources/SplineRender-Demo.gif "ノードの例1")

</td>
</tr>
</table>
