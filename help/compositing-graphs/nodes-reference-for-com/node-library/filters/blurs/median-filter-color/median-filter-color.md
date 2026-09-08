---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-color.html"
breadcrumb-title: ''
description: 中間値フィルターカラーノードを使用して、ノイズを軽減し、カラーテクスチャのエッジを保持します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 中間フィルターカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---


# 中間フィルターカラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![フィルターの色の中央値：アイコン](../../../../../../assets/MedianFilter_Icon_Color.png "フィルターの色の中央値：アイコン")

<b>イン:</b>フィルター/ぼかし

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このフィルターは、エッジを保持しながら画像のノイズを滑らかにします。

各ピクセルごとに、そのピクセルの隣接するピクセルの中間値に基づいてカラー値が計算されます。

</td>
</tr>
</table>

>[!NOTE]
>
> [中間値フィルターのグレースケール](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-grayscale/median-filter-grayscale.md)も参照してください。

## 入力コネクタ

<b>入力&#x200B;</b>*色*&#x200B;フィルターを適用するカラー画像。

## 出力コネクタ

<b>出力</b> *色*&#x200B;入力カラー画像にフィルターを適用して計算されたカラー画像。

## パラメーター

<b>カーネルサイズ</b> *整数*&#x200B;カーネルは、フィルターの計算に使用される特定の値のグループです。 この場合、隣接ピクセルの値になります。\
各ピクセルについて、そのピクセルの周囲にあるすべてのネイバー値を正方形のカーネル内に取り、すべてのネイバー値の中央値を計算します。\
このパラメーターは、その正方形のカーネルのサイズをピクセル単位で制御します。 カーネルが大きいほど、より強く、より広範囲に及ぶスムージング効果が得られ、ディテールが若干犠牲になります。\
*- 3x3:*&#x200B;カーネルの幅が3ピクセル、高さが3ピクセルで、隣接するピクセル数の合計が8ピクセルです。\
*- 5x5:*&#x200B;カーネル幅5ピクセル、高さ5ピクセル、隣接する24ピクセルの合計。

<b>フィルターの種類</b> *整数*&#x200B;カーネルでサンプリングされた近隣ノードに適用される計算です。\
*– メジアン：*&#x200B;すべての近隣の値のメジアンを直接使用します。\
*- MLMAD:*&#x200B;は&#39;最小中央値絶対偏差の中央値&#39;を表します。 偏差は、値と中央値との差を考慮に入れて算出されます。 MLMAD法では、偏差の大きい方のピクセルによって歪む可能性がある中央値を直接使用する代わりに、すべての偏差の中央値を使用します。 このメソッドは、カーネルサイズに従って領域を平坦化する、より強いスムージング効果を生成します。

<b>アルファに影響</b> *ブーリアン*&#x200B;画像のアルファチャンネルにフィルターを適用するかどうかを制御します。 *True*&#x200B;の場合、アルファチャンネルは変更されません。

## 例

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3A.png" alt="MedianFilter_Variant3A">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MedianFilter_Variant3B.png" alt="MedianFilter_Variant3B">
      <br><i>後</i>
    </td>
  </tr>
</table>
