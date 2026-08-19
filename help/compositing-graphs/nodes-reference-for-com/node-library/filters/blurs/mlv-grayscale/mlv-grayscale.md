---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/mlv-grayscale.html"
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
source-git-commit: 27326c60e0247617a8f57554a68c9663934cd2bc
workflow-type: tm+mt
source-wordcount: '314'
ht-degree: 0%

---


# MLVグレースケール

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![MLVグレースケール：アイコン](../../../../../../assets/MLV_Grayscale_Icon.png "MLVグレースケール：アイコン")

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

## 入力コネクタ

<b>入力&#x200B;</b>*グレースケール*&#x200B;処理するグレースケールイメージです。

## 出力コネクタ

<b>出力&#x200B;</b>*グレースケール*&#x200B;フィルター処理されたグレースケール画像。

## パラメーター

<b>適用度</b> *フロート*&#x200B;画像に適用されたフィルターの強度です。\
値が大きいほど、ディテールが滑らかになり、平坦な領域にノイズが発生します。

<b>Smoothness</b> *フロート*&#x200B;構造化する領域に適用される滑らかさの強度です。その結果、領域が丸くなり、フィルタリングの強度が高い場合に発生することがあるステッピング効果が軽減されます。

<b>基準</b> *整数*&#x200B;画像の構造化領域を定義する値を選択するために使用される基準です。\
言い換えると、スムージングする領域にピクセルをどのように&#x200B;*グループ化*&#x200B;するかを指定します。\
*– 分散：*&#x200B;平均の周りのばらつきが最も小さい値を選択します。これにより、ピクセルのクラスタが互いに類似するようになります\
*– 変動係数：*&#x200B;平均を考慮しながら値を選択すると、明るい領域で逆に変動が少なくなります

<b>ガウス</b> *ブール値*&#x200B;ガウス分布を使用して、ピクセルを構造化領域にグループ化します。\
「True」の場合、より滑らかな領域になり、分割・統合の効果が減少します。

<b>反復回数</b> *整数*&#x200B;フィルターが実行され、各繰り返しが前の繰り返しの結果に適用される回数です。\
反復が多いほど、より平坦でシャープな構造領域になります。

## 例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant1A.png" alt="MLV_Variant1A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant1B.png" alt="MLV_Variant1B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2B.png" alt="MLV_Variant2B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MLV_Variant2A.png" alt="MLV_Variant2A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MLV_Variant2C.png" alt="MLV_Variant2C">
      <br><i>後</i>
    </td>
  </tr>
</table>
