---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-2d-transform.html"
breadcrumb-title: ''
description: '[スプライン2D変形]ノードを使用すると、直線移動、回転、および尺度変更を行うスプラインを変形できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン2D変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 1%

---


# スプライン2D変換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-2d-transform.resources/spline-2d-transform-01.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

方向の反転を含むすべての入力スプラインにグローバル変換を適用します。

</td>
</tr>
</table>

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
| <b>方向を反転</b> <i>ブール値</i> | スプラインの方向を反転します。 |
| <b>マトリックスの変形</b> <i>浮動小数点4</i> | スプラインに適用される変換行列。<br>マトリックスパラメーターを編集する3つのモードを使用できます。<br><br>- <i>変換ギズモ</i>:スプライン2D変形ノードが選択された場合に、2D ビューに表示されるギズモのハンドルを微調整します。<br>- <i>回転/伸縮</i>:スプラインの回転と伸縮を個別に制御します。 値は常に現在の変換に対して相対的に適用されることに注意してください。 例えば、50%の幅を2回適用すると、25%の幅になります。<br>- <i>行列の値</i>: 「行列の値を編集」ボタンをクリックして、行列の生の数値を直接入力します。 |
| <b>オフセット</b> <i>浮動小数点2</i> | 位置オフセットをX（水平）およびY（垂直）のスプラインに適用します。 |
| <b>プレビュー</b> |  |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブール値</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインのビジュアライゼーションを描画するために使用するセグメントの数を調整します。 値が大きいほど、線は滑らかになります。 |
| <b>Thickness (px)</b> <i>フロート</i> | プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-2d-transform.resources/spline-2d-transform-02.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-2d-transform.resources/spline-2d-transform-03.jpg" alt="Spline2DTransform-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-2d-transform.resources/spline-2d-transform-02.jpg" alt="Spline2DTransform-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-2d-transform.resources/spline-2d-transform-04.jpg" alt="Spline2DTransform-Variant1-After">
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

![ノードの例1](spline-2d-transform.resources/spline-2d-transform-05.gif "ノードの例1")

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
