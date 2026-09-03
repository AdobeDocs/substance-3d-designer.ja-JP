---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/anisotropic-kuwahara-grayscale.html"
breadcrumb-title: ''
description: 異方性桑原グレースケールフィルターを使用して、方向性をスムーズに、スタイライズされた絵画調の効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Anisotropic Kuwahara Grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 異方性桑原グレースケール
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---


# 異方性桑原グレースケール

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![異方性桑原グレースケールアイコン](anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-01.png "異方性桑原グレースケールアイコン"){width="200px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

画像のディテールに沿った異方性指向性ブラーを適用します。 その結果、内部の図形の方向に&#x200B;*flow*&#x200B;と表示される画像が得られます。

この調整可能なぼかしは、*方向マップ*&#x200B;を計算または受け取って、流量を特定します。流量は、より平坦で明確に定義された領域にシャープにすることができます。

関連項目： [異方性桑原カラー](../anisotropic-kuwahara/anisotropic-kuwahara.md)

</td>
</tr>
</table>

また、ぼかしの向きを回転させて流れを分解してもよい。 同様に、カスタム方向マップを使用して、画像から計算された設定を上書きすることもできます。

このフィルターは、絵画調の効果を生み出すことができ、スタイル設定に便利です。

+++ 異方性

下の図に示すように、流れの強さは主に[異方性](#parameters)パラメーターで制御されます。

左：異方性 0.0 /右：異方性 1.0

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![桑原フィルターを0の異方性で適用した果物のボウル。](anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-02.jpg){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![桑原フィルターを0の異方性で適用した果物のボウル。](anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-03.jpg){zoomable="yes"}

</td>
</tr>
</table>

+++

## 入力

|                                                       |                                                                                                                                                                                                                                                                                                                         |
|-------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>入力</b> <i>グレースケール</i><br><code>プライマリ</code> | 処理するグレースケールイメージです。 |
| <b>異方性角度マップ</b> <i>グレースケール</i> | グレースケールの画像は、計算された方向に適用される追加の回転を表します。グレースケールの値は回転の回数です。   マップは、異方性パラメータが0の場合も影響を与えます。これは、桑原フィルタで使用されるカーネルのローテーションに影響を与えるためです。 |
| <b>勾配マップ</b> <i>グレースケール</i> | 「勾配マップ入力乗数」パラメータ値に従って、方向マップが準拠する勾配を表すマップ。 |
| <b>半径マップ（オプション）</b> <i>グレースケール</i> | 接続すると、ぼかしの「半径」が入力画像に対して乗算されます。 |
| <b>方向マップ</b> <i>色</i> | 異方性反射フィルタカーネルによって使用される方向を記述するマップ。   マップは、異方性パラメータが0の場合も影響を与えます。これは、桑原フィルタで使用されるカーネルのローテーションに影響を与えるためです。   メモ：この入力は、「入力方向マップーを使用」パラメーターが「True」に設定されている場合にのみ使用されます。 |

## 出力

|                                   |                                                                                                                                                                                                                                      |
|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>出力</b> <i>グレースケール</i> | 入力イメージ上のノードによって適用された異方性ブラーの結果。 |
| <b>方向マップ</b> <i>色</i> | 入力イメージから計算された方向マップで、異方性ブラーの駆動に使用されます。   「入力方向マップーを使用」パラメーターが「True」に設定されている場合、「方向マップー」入力に指定された画像が使用され、そのまま出力されます。 |

## パラメーター

|                                                                                                                              |                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <b>半径</b> <i>フロート</i> | ブラーの半径の値を大きくすると、ぼかし効果が強くなります。   最大値は32です。 |
| <b>Smoothness</b> <i>フロート</i> | 計算された方向にカラーをブレンドする量を調整します。   この値を0に設定すると、カラーはほとんどその方向に置き換えられ、ブレンドはほとんど発生しません。 |
| <b>シャープ</b> <i>フロート</i> | ぼやけた領域のコントラストが上がり、より平坦で鮮明に見えます。 |
| <b>異方性</b> <i>フロート</i> | ぼかしの方向マップの効果を調整します。   このパラメーター値が0の場合は、方向マップとそのすべての修飾子（パラメーターと入力マップの両方）が有効です。これは、方向マップが桑原フィルターカーネルで使用されているためです。 |
| <b>入力方向マップを使用する</b> <i>ブール値</i> | 「True」の場合、入力画像から方向マップは計算されず、代わりに「方向マップ」入力に接続された画像を使用して異方性ブラーが駆動されます。 |
| <b>テンソルSmoothness</b> <i>浮動小数</i><br><br><i>[入力方向マップーを使用]が&#39;False&#39;に設定されている場合に使用できます</i> | 画像から計算されて方向マップに保存された方向に対して適用されるぼかしの強さを調整します。   この値を大きくすると、画像に高い周波数のディテールが多く含まれている場合に、滑らかな結果が得られます。 |
| <b>異方性角度</b> <i>浮動小数</i><br><br><i>[入力方向マップーを使用]が&#39;False&#39;に設定されている場合に使用できます</i> | 方向マップに回転をターン数で追加します。   この追加回転は、&#39;異方性角度マップ&#39;入力で指定された回転と共に&#x200B;*累積*&#x200B;されます。 |
| <b>異方性角度マップ乗数</b> <i>浮動小数</i><br><br><i>[入力方向マップーを使用]が&#39;False&#39;に設定されている場合に使用できます</i> | 「異方性角度マップ」入力の値の強さを調整します。この値は、方向マップに適用される回転角度の上にターン数で追加されます。   この追加回転角度は、&#39;異方性角度&#39;パラメーターで指定された回転角度を持つ&#x200B;*累積回転角度*&#x200B;です。 |
| <b>勾配マップ入力乗数</b> <i>浮動小数</i><br><br><i>[入力方向マップーを使用]が&#39;False&#39;に設定されている場合に使用できます</i> | 「勾配マップ」の入力によって提供される勾配に合わせて方向マップの適用度を調整します。 |

## 例

<table>
  <tr>
    <td>
      <img src="anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-04.jpg" alt="anisotropic_kuwahara_gray_example_1_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-05.jpg" alt="anisotropic_kuwahara_gray_example_1_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-06.jpg" alt="anisotropic_kuwahara_gray_example_2_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-07.jpg" alt="anisotropic_kuwahara_gray_example_2_after">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-08.jpg" alt="anisotropic_kuwahara_gray_example_4_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="anisotropic-kuwahara-gra.resources/anisotropic-kuwahara-grayscale-09.jpg" alt="anisotropic_kuwahara_gray_example_4_after">
      <br><i>後</i>
    </td>
  </tr>
</table>
