---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-select.html"
breadcrumb-title: ''
description: '[スプライン選択]ノードを使用して、グラフ内のスプラインパスに基づいて特定の領域を選択し、マスクします。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline Select
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン選択
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---


# スプライン選択

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-select.resources/spline-select-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

指定した基準に従って入力リストのスプラインを選択し、選択したスプラインのみを含む新しいリストを出力します。

選択したスプラインをトリムすることもできます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | 出力スプラインの座標がカラー画像のRGBAチャンネルにエンコードされました。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 出力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>選択モード</b> <i>整数</i> | 入力リストのスプラインを選択する方法：<br>- <i>最初</i>：一覧の最初のスプラインを選択します。<br>- <i>最後</i>：一覧の最後のスプラインを選択します。<br>- <i>インデックス</i>：指定されたインデックスを持つスプラインを選択します。<br>- <i>範囲</i>：指定された範囲にインデックスを含むスプラインを選択します。 |
| <b>スプラインインデックス</b> <i>整数</i> | （「選択モード」が「インデックス」に設定されている場合に使用可能）選択するスプラインのインデックス。 |
| <b>範囲の開始</b> <i>整数</i> | （「選択モード」が「範囲」に設定されている場合に使用可能）選択したスプラインの範囲の最小インデックス。 |
| <b>範囲の終了</b> <i>整数</i> | （「選択モード」が「範囲」に設定されている場合に使用可能）選択したスプラインの範囲の最大インデックス。 |
| <b>開始</b> <i>フロート</i> | 選択するスプライン部分の始点をオフセットします。 これにより、スプラインが効果的にトリムされます。<br>この値は、スプラインの正規化された長さを表します。 |
| <b>終了</b> <i>フロート</i> | 選択するスプライン部分の終点をオフセットします。 これにより、スプラインが効果的にトリムされます。<br>この値は、スプラインの正規化された長さを表します。 |
| <b>プレビュー</b> |  |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインの視覚化に使用するセグメントの数を調整します。<br>値を大きくすると、より滑らかな線になります。 |
| <b>方向のヘルパーを表示</b> <i>ブール値</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブール値</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>Thickness (px)</b> <i>浮動小数</i> | プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/spline-select-02.jpg" alt="SplineSelect – バリアント1 – 前">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-select.resources/spline-select-03.jpg" alt="SplineSelect-Variant1-After2">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-select.resources/spline-select-04.jpg" alt="SplineSelect – バリアント2 – 前">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-select.resources/spline-select-05.jpg" alt="SplineSelect-Variant2-After">
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

![ノードの例1](spline-select.resources/spline-select-06.gif "ノードの例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
