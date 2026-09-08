---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-color.html"
breadcrumb-title: ''
description: MLVカラーぼかしフィルターを使用して、モーションブラー効果をカラーテクスチャに適用し、ダイナミックなビジュアルルックを実現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > MLV color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MLVカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# MLVカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLVカラー：アイコン](../../../../../../assets/MLV_Color_Icon.png "MLVカラー：アイコン")

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

## 入力コネクタ

<b>入力&#x200B;</b>*色*&#x200B;処理するカラー画像です。

## 出力コネクタ

<b>出力</b> *色*&#x200B;フィルター処理されたカラー画像。

## パラメーター

<b>適用度</b> *フロート*&#x200B;画像に適用されたフィルターの強度です。\
値を大きくすると、ディテールがより滑らかになり、より平坦な領域にノイズします。

<b>Smoothness</b> *浮動小数*&#x200B;構造を形成する領域に適用される滑らかさの強度です。これにより、領域が丸くなり、フィルタリングの強度が高い場合に発生することがあるステッピング効果が軽減されます。

<b>基準</b> *整数*&#x200B;画像内の構造化する領域を定義する値を選択するために使用される基準です。\
言い換えると、スムージングする領域にピクセルをどのように&#x200B;*グループ化*&#x200B;するかを指定します。\
*– 差異：*&#x200B;平均の周囲の分散が最も低い値を選択します。これにより、ピクセルのクラスターが互いに似ています\
*– 変動係数：*&#x200B;平均を考慮しながら値を選択すると、明るい領域で逆に変動が少なくなります

<b>ガウス</b> *ブーリアン*&#x200B;ガウス分布を使用して、ピクセルを構造化する領域にグループ化します。\
「True」の場合、より滑らかな領域になり、分割・統合の効果が減少します。

<b>アルファに影響</b> *ブーリアン*&#39;True&#39;の場合、フィルタリングは画像のアルファチャンネルにも適用されます。\
&#39;False&#39;の場合、アルファチャンネルは完全に無視され、出力にそのまま残されます。

<b>反復回数</b> *整数*&#x200B;フィルターが実行された回数です。各反復は、前の結果に基づいて適用されます。\
反復を増やすと、より平坦でシャープな構造領域になります。

## 例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant4A.png" alt="MLV_Variant4A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant4B.png" alt="MLV_Variant4B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant5A.png" alt="MLV_Variant5A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant5B.png" alt="MLV_Variant5B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant3A.png" alt="MLV_Variant3A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant3B.png" alt="MLV_Variant3B">
      <br><i>後</i>
    </td>
  </tr>
</table>
