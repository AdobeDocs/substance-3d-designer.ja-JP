---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-bridge-list.html"
breadcrumb-title: ''
description: '[スプラインブリッジリスト]ノードを使用して、複雑なパターンのリスト内の複数のスプライン間でテクスチャをブリッジします。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Bridge (List)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラインブリッジ（一覧）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# スプラインブリッジ（一覧）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-bridge-list.resources/spline-bridge-list-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

入力リスト内のすべてのスプラインを横断するスプラインを、これらのスプラインに沿って生成します。

生成されるスプラインは、線形（直線）または二次ベジェ（曲線）になります。

</td>
</tr>
</table>

>[!TIP]
>
> 生成されたスプラインは、リストの最初のスプラインから最後のスプラインに移動し、リスト内のこれらのスプラインの順序に厳密に従って中間のスプラインを横断します。
> 
> したがって、事前にスプラインを追加する順序に注意する必要があります。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | 出力スプラインの座標がカラー画像のRGBAチャンネルにエンコードされました。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br>-絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 出力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ブリッジスプラインの量</b> <i>整数</i> | 入力スプラインを通して生成されたスプラインの数です。 |
| <b>ブリッジスプラインの種類</b> <i>整数</i> | 生成されるスプラインの種類：<br><br> – 線形：開始から終了まで直線軌道で中間スプラインを接続する鋭いスプライン；<br> – 二次ベジェ：開始から終了まで滑らかな軌道で中間スプラインを接続する曲線スプライン。<br><br>注：二次ベジェスプラインを計算するには、少なくとも3つの入力スプラインが必要です。 |
| <b>入力スプラインが閉じています</b> <i>ブール値</i> | 入力スプラインの最初の点と最後の点を1点として処理するかどうかをコントロールします。 これにより、最初と最後のトラバーススプラインが重複するのを防ぐことができます。 |
| <b>方向を反転</b> <i>ブール値</i> | スプラインの方向を反転します。 |
| <b>ブリッジスプラインを閉じる</b> <i>ブール値</i> | トラバーススプラインを延長し、入力リストの最初のスプラインに戻ります。 |
| <b>最初のブリッジスプラインオフセット</b> <i>浮動小数点2</i> | すべてのトラバーススプラインの始点にオフセットを適用します。 この値は、入力スプラインの正規化された長さです。<br>トラバースされたスプラインの始点または終点に一致する生成されたスプラインは、そのまま残ります。 |
| <b>最後のブリッジスプラインオフセット</b> <i>浮動小数点2</i> | すべてのトラバーススプラインの終点にオフセットを適用します。 この値は、入力スプラインの正規化された長さです。<br>トラバースされたスプラインの始点または終点に一致する生成されたスプラインは、そのまま残ります。 |
| <b>ランダムオフセット範囲</b> <i>整数</i> | スプラインに適用されたランダムオフセットに使用される最大距離。<br><br>- <i>親スプライン：</i>親スプラインの全長が使用されます。 重複が発生する可能性があります。<br>- <i>間隔：</i>ブリッジスプライン間の間隔が使用されています。 これにより、重複が軽減されます。 この距離は、ブリッジスプラインの量が増えるにつれて減少します。 |
| <b>開始ランダムオフセット</b> <i>フロート</i> | ブリッジスプラインの開始位置に適用されるランダムオフセットの乗数。最大距離は<b>ランダムオフセット範囲</b>パラメータで指定されます。 |
| <b>ランダムオフセットの終了</b> <i>フロート</i> | ブリッジスプラインの終了位置に適用されるランダムオフセットの乗数。最大距離は<b>ランダムオフセット範囲</b>パラメータで指定されます。 |
| <b>グローバルランダムオフセット</b> <i>フロート</i> | ブリッジスプラインの開始位置と終了位置の&#x200B;*両方*&#x200B;に適用されたランダムオフセットの&#x200B;*等しい量*&#x200B;の乗数。最大距離は<b>ランダムオフセット範囲</b>パラメータで指定されます。 |
| <b>均一な分布</b> <i>ブール値</i> | Trueの場合、生成されたスプラインの点は、始点から終点まで等間隔になります。 |
| <b>Thickness</b> |  |
| <b>Thicknessモード</b> <i>整数</i> | ブリッジスプラインのThickness値を取得する方式です。<br><br>- <i>親スプラインから継承する：</i>ブリッジスプラインの開始位置と終了位置における親スプラインのThicknessを使用します<br>- <i>上書き：</i> <b>Thickness</b>パラメーターで指定した任意の値が使用されます |
| <b>Thickness</b> <i>フロート</i> | ブリッジスプラインに適用される絶対Thickness値。 |
| <b>Thicknessランダム</b> <i>フロート</i> | ブリッジスプラインのThicknessのランダム乗数。この乗数が適用される初期Thicknessは、<b>Thicknessモード</b>パラメーターで指定されます。 |
| <b>Height</b> |  |
| <b>Heightモード</b> <i>整数</i> | ブリッジスプラインのHeight値を取得する方式です。<br><br>- <i>親スプラインから継承する：</i>ブリッジスプラインの開始位置と終了位置における親スプラインのHeightを使用します<br>- <i>上書き：</i> <b>Height</b>パラメーターで指定した任意の値が使用されます |
| <b>Heightオフセット</b> <i>フロート</i> | Heightがブリッジスプラインに適用される前に、親スプラインから継承されたHeightに適用されるオフセットの量。 |
| <b>Height</b> <i>フロート</i> | ブリッジスプラインに適用される絶対Height値。 |
| <b>Heightランダム</b> <i>フロート</i> | ブリッジスプラインのHeightに対するランダムな調整量。この調整は、選択した<b>Heightモード</b>に依存します。パラメーター：<br><br>- <i>親スプラインから継承：</i>値は、継承されたHeightの乗数です。<br>- <i>上書き：</i>値はHeightに追加されたオフセットです。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。 これは均一な分布にも影響を与えます。 |
| <b>プレビュー</b> |  |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブール値</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインのビジュアライゼーションを描画するために使用するセグメントの数を調整します。 値が大きいほど、線は滑らかになります。 |
| <b>Thickness (px)</b> <i>フロート</i> | プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。 |
| <b>背景プレビューの適用度</b> <i>フロート</i> | プレビュービジュアライゼーションの強度。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-02.jpg" alt="SplineBridge-List_Variant1_Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-bridge-list.resources/spline-bridge-list-03.jpg" alt="SplineBridge-List_Variant1_After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-bridge-list.resources/spline-bridge-list-04.gif "ノードの例2")

</td>
</tr>
</table>

![グラフのノード](spline-bridge-list.resources/spline-bridge-list-05.jpg "グラフのノード")
