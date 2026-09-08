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
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '335'
ht-degree: 5%

---


# ライトを形成

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-shape.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

球状に投影された長方形を生成します。 シェイプの変形は、変形ギズモによって行われます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>背景画像の入力</b> <i>カラー入力</i> | 生成されたライトを構成するオプションの背景。 |
| <b>シェイプ画像の入力</b> <i>カラー入力</i> | 球体ライトにマップするオプションのイメージ。 シェイプのカラーモードが画像入力に設定されている場合にのみ使用されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>シェイプ行列</b> |  |
| <b>行列</b> <i>（変換行列）</i> | 結果の変換コントロール。 カンバスを直接操作して、結果を変更できます。 |
| <b>オフセット</b> <i>-2.0 - 2.0</i> | 結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。 |
| <b>図形</b> <i>長方形、ディスク</i> | 配置するシェイプを選択します。 |
| <b>図形のカラーモード</b> <i>RGB、色温度（ケルビン）、画像入力</i> | シェイプカラーの設定に使用する方法を選択します。 イメージ入力により、2番目の入力スロットが使用可能になります。 |
| <b>色</b> <i>（カラー値）</i> | シェイプカラーモードを「RGB」に設定した場合のみ シェイプのカラーを選択します。 |
| <b>図形の色温度</b> <i>800.0 - 20000.0</i> | Shape Color ModeがTemperatureに設定されている場合のみ シェイプのカラーのケルビン値を設定します。 |
| <b>シェイプ画像の入力ガンマ</b> <i>sRGB、リニア</i> | シェイプのカラーモードを画像入力に設定した場合のみ。 シェイプ画像の入力を解釈する方法を指定します。 |
| <b>図形の露出(EV)</b> <i>0.0 - 10.0</i> | 生成されたシェイプの露光量値を設定します。背景画像の露光量値と理想的に一致させます。 |
| <b>図形の硬さ</b> <i>0.0 - 1.0</i> | シェイプのエッジの硬さを設定 |
| <b>ホットスポット露出(EV)</b> <i>0.0 - 10.0</i> | 中央のホットスポットの露光量を設定します。 RGBモードでは確認できません。 |
| <b>ホットスポットのサイズ</b> <i>0.0 - 1.0</i> | 中央のホットスポットのサイズ。 |
| <b>ホットスポットフォールオフ</b> <i>0.0 - 1.0</i> | 中央ホットスポットの減衰。 |
| <b>ホットスポットの位置</b> <i>0.0 - 1.0</i> | 中央のホットスポットのX位置とY位置。 |
| <b>バックグラウンド入力を有効にする</b> <i>False/True</i> | オプションの背景画像の使用を切り替え 生成されたライトを背景の上に合成します。 |
| <b>背景色</b> <i>（カラー値）</i> | 背景入力を使用しない場合は、単色の背景色を設定します。 |
| <b>背景ガンマ</b> <i>sRGB、リニア</i> | バックグラウンド入力を使用する場合は、バックグラウンド入力の解釈方法を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/shape-light-ex.gif" />
        </td>
    </tr>
</table>
