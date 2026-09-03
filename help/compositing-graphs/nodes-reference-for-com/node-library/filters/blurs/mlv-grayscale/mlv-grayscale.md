---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
breadcrumb-title: ''
description: MLVグレースケールぼかしフィルターを使用して、ダイナミックな外観にするためにグレースケールテクスチャにモーションぼかし効果を適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLVグレースケール
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 1%

---


# MLVグレースケール

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLVグレースケール：アイコン](mlv-grayscale.resources/mlv-grayscale-01.png "MLVグレースケール：アイコン")

<b>イン:</b>フィルター/ぼかし

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

MLVは<b>&#39;最小分散の平均&#39;</b>を表します。 このフィルターは、画像のエッジを強調し、ノイズを滑らかにします。

フィルターは、画像の中から構造化している領域を見つけ、その領域を使用してシャープとフラットの両方を行います。 場合によっては、その結果、グラデーションに沿ったステップの幅が構造の領域よりも広くなることがあります。

</td>
</tr>
</table>

>[!NOTE]
>
> [MLVカラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-color/mlv-color.md)も参照。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール</i> | 処理するグレースケールイメージです。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | フィルターされたグレースケールイメージ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> *フロート* | 画像に適用されるフィルタリングの強さ。<br><br>値が大きいほど、ディテールがより滑らかになり、より平坦な領域にノイズします。 |
| <b>Smoothness</b> *フロート* | 構造化する領域に適用されるスムージングの強さです。これにより、領域が丸くなり、フィルタリングの強さが高くなると発生するステッピング効果が軽減されます。 |
| <b>基準</b> *整数* | 画像内の構造化エリアを定義する値を選択するために使用する基準です。<br><br>つまり、平滑化する領域にピクセルをどのように&#x200B;*グループ化*&#x200B;するかを指定します。<br><br>*– 分散：*&#x200B;平均の周りの分散が最も低い値を選択します。これにより、ピクセルのクラスターが互いに似たものになります。<br>*– 変動係数：*&#x200B;平均を考慮しながら値を選択すると、明るい領域の変動が逆に少なくなります |
| <b>ガウス</b> *ブール値* | ガウス分布を使用して、ピクセルを構造化する領域にグループ化します。<br><br>&#39;True&#39;の場合、より滑らかな領域になり、フラット効果が減少します。 |
| <b>反復回数</b> *整数* | 各反復が前の結果に適用される、フィルタの実行回数。<br><br>反復数が多いほど、より平坦でシャープな構造領域になります。 |

## 例

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-02.png" alt="MLV_Variant1A">
      <br><i>前</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-03.png" alt="MLV_Variant1B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-04.png" alt="MLV_Variant2A">
      <br><i>前</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-05.png" alt="MLV_Variant2B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-04.png" alt="MLV_Variant2A">
      <br><i>前</i>
    </td>
    <td>
      <img src="mlv-grayscale.resources/mlv-grayscale-06.png" alt="MLV_Variant2C">
      <br><i>後</i>
    </td>
  </tr>
</table>
