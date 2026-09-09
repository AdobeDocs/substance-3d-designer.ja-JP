---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: MLVカラーぼかしフィルターを使用して、カラーテクスチャにモーションブラー効果を適用し、ダイナミックな外観にします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLVカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 1%

---


# MLVカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLVカラー：アイコン](mlv-color.resources/MLV_Color_Icon.png "MLVカラー：アイコン")

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
> [MLVグレースケール](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/mlv-grayscale/mlv-grayscale.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>色</i> | 処理するカラー画像。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>色</i> | フィルター処理されたカラー画像。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> *浮動小数* | 画像に適用されるフィルタリングの強さ。<br><br>値が大きいほど、ディテールがより滑らかになり、より平坦な領域にノイズします。 |
| <b>Smoothness</b> *浮動小数* | 構造化する領域に適用されるスムージングの強さです。これにより、領域が丸くなり、フィルタリングの強さが高くなると発生するステッピング効果が軽減されます。 |
| <b>基準</b> *整数* | 画像内の構造化エリアを定義する値を選択するために使用する基準です。<br><br>つまり、平滑化する領域にピクセルをどのように&#x200B;*グループ化*&#x200B;するかを指定します。<br><br>*– 分散：*&#x200B;平均の周りの分散が最も低い値を選択します。これにより、ピクセルのクラスターが互いに似たものになります。<br>*– 変動係数：*&#x200B;平均を考慮しながら値を選択すると、明るい領域の変動が逆に少なくなります |
| <b>ガウス</b> *ブール値* | ガウス分布を使用して、ピクセルを構造化する領域にグループ化します。<br><br>&#39;True&#39;の場合、より滑らかな領域になり、フラット効果が減少します。 |
| <b>アルファに影響</b> *ブール値* | 「True」の場合、フィルタリングは画像のアルファチャンネルにも適用されます。<br><br>&#39;False&#39;の場合、アルファチャンネルは完全に無視され、出力にそのまま残されます。 |
| <b>反復回数</b> *整数* | 各反復が前の結果に適用される、フィルタの実行回数。<br><br>反復数が多いほど、より平坦でシャープな構造領域になります。 |

## 例

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>前</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>前</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="mlv-color.resources/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>前</i>
    </td>
    <td>
      <img src="mlv-color.resources/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>後</i>
    </td>
  </tr>
</table>
