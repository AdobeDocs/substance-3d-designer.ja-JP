---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/waveform-1.html"
breadcrumb-title: ""
description: 「波形1」ノードを使用して、有機的なテクスチャやプロシージャル的なバリエーションを生み出すための波形パターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Waveform 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 波形1
user-guide-description: ""
user-guide-title: ""
source-git-commit: 0f214099ae94088d37122a5d474d3e70d4ccf46f
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 1%
---

# 波形1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![波形1 – アイコン](waveform-1.resources/waveform_01_v2.png "波形1 – アイコン"){width="200px"}

<b>イン：</b> テクスチャジェネレーター> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ユーザーが選択したパターンの水平方向の配置で、波形に似たシェイプにスタックされます。

</td>
</tr>
</table>

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 生成されるノイズをグレースケールビットマップとして指定します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>サンプル</b> <i>整数</i> | 波形を描くためにX軸に沿って配置されるパターンの量。値を小さくすると、段階的な外観になります。 |
| <b>関数</b> <i>整数</i> | 波形の描画に使用する関数。   これにより、各サンプルに配置されるパターンの垂直方向のサイズが制御されます。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>値のノイズ:</i>値のランダムな分布</li> <li data-preserve-html="true"><i>コサイン：</i>値はコサイン関数の進行に従います</li> <li data-preserve-html="true"><i>カスタム関数：</i>ユーザーが作成した関数を使用して値を制御します</li> </ul> |
| <b>カスタム関数</b> <i>浮動小数</i>   *&#39;Function&#39;が&#39;Custom function&#39;に設定されている場合に使用可能* | 各サンプルに配置されたパターンの垂直サイズを計算します。   使用可能な変数：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>pos</b> (<i>float</i>) X軸上のパターンの位置です。 これは、パターンの選択に使用できます。</li> </ul> |
| <b>ラフネス</b> <i>浮動小数</i> | クリーンで滑らかな波形を、より粗く均等に分布した波形で補間します。    これは、ホワイトノイズに対してクリーンな信号と考えることができます。 |
| <b>スケール</b> <i>整数</i> | 画像に表示される波形の水平方向の範囲です。 |
| <b>最小振幅</b> <i>浮動小数</i> | 波形の最小値（またはThickness）。 |
| <b>最大振幅</b> <i>浮動小数</i> | 波形の最大値（またはThickness）。 |
| <b>ノイズ</b> <i>浮動小数</i> | 波形にノイズを加え、垂直方向のスパンからランダムに差し引きます。 |
| <b>位置</b> <i>整数</i> | 画像内での波形の位置です。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>中央：</i>原点は画像の垂直方向の中心です</li> <li data-preserve-html="true"><i>下：</i>原点は画像の下部です</li> </ul> |
| <b>パターン</b> <i>整数</i> | 波形の各サンプルに配置されるパターン。 |
| <b>パターンバリエーション</b> <i>フロート</i> | 一部のパターンに使用できる追加の調整。 |
| <b>障害</b> <i>フロート</i> | 波形値を置き換えます。    これを使用してアニメーション化できます。 |
| <b>速度の乱れ</b> <i>フロート</i> | <b>Disorder</b>パラメーターによって適用されるディスプレイスメントの間隔を調整します。    これを使用して、波形をアニメーション化するときのディスプレイスメント速度を制御できます。 |

## 例

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="waveform-1.resources/waveform_01_v2_speed0.1_aniso0.gif" class="modal-image" alt="波形1 – 例1" />
        </td>
        <td style="border: 0;"></td>
        <td style="border: 0;"></td>
    </tr>
</table>
