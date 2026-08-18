---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/shape-light.html"
breadcrumb-title: ''
description: シェイプライトノードを使用して、カスタムシェイプの光源をHDRI環境に追加し、クリエイティブな照明効果を得ます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Shape Light
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライトを形成
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '336'
ht-degree: 0%

---


# ライトを形成

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

## ライトを形成

**イン：** *3Dビュー/HDRI ツール*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

球状に投影された長方形を生成します。 シェイプの変形は、変形ギズモによって行われます。

## 入力

* **背景画像の入力**: *色入力*&#x200B;生成された光を構成するオプションの背景。
* **シェイプ画像入力**: *カラー入力*&#x200B;球体光にマップするオプションの画像。 シェイプのカラーモードが画像入力に設定されている場合にのみ使用されます。

## パラメーター

* **シェイプ行列**
  * **行列**: *（変換行列）*\
    結果の変換コントロール。 カンバスを直接操作して、結果を変更できます。
  * **オフセット**: *-2.0 - 2.0*\
    結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。
* **図形**: *長方形、ディスク*\
  配置するシェイプを選択します。
* **図形のカラーモード**: *RGB、色温度（ケルビン）、画像入力*\
  シェイプカラーの設定に使用する方法を選択します。 イメージ入力により、2番目の入力スロットが使用可能になります。
* **色**: *（色値）*\
  シェイプカラーモードを「RGB」に設定した場合のみ シェイプのカラーを選択します。
* **図形の温度**: *800.0 - 20000.0*\
  Shape Color ModeがTemperatureに設定されている場合のみ シェイプのカラーのケルビン値を設定します。
* **シェイプ画像の入力ガンマ**: *sRGB、リニア*\
  シェイプのカラーモードを画像入力に設定した場合のみ。 シェイプ画像の入力を解釈する方法を指定します。
* **図形の露出(EV)**: *0.0 - 10.0*\
  生成されたシェイプの露光量値を設定します。背景画像の露光量値と理想的に一致させます。
* **図形の硬さ**: *0.0 ～ 1.0*\
  形状エッジの硬さを設定します。
* **ホットスポットの露出(EV)**: *0.0 ～ 10.0*\
  中央のホットスポットの露光量を設定します。 RGBモードでは確認できません。
* **ホットスポットのサイズ**: *0.0 ～ 1.0*\
  中央のホットスポットのサイズ。
* **ホットスポットフォールオフ**: *0.0 - 1.0*\
  中央ホットスポットの減衰。
* **ホットスポットの位置**: *0.0 ～ 1.0*\
  中央のホットスポットのX位置とY位置。
* **バックグラウンド入力を有効にする**: *False/True*\
  オプションの背景画像の使用を切り替え 生成されたライトを背景の上に合成します。
* **背景色**: *（色値）*\
  背景入力を使用しない場合は、単色の背景色を設定します。
* **バックグラウンドガンマ**: *sRGB、リニア*&#x200B;バックグラウンド入力を使用する場合は、バックグラウンド入力の解釈方法を設定します。

## サンプル画像

![](../../../../../../assets/shape-light-ex.gif)

</td>
</tr>
</table>
