---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/blurs/median-filter-grayscale.html"
breadcrumb-title: ''
description: 中間値フィルターのグレースケールノードを使用すると、ノイズを軽減し、エッジをグレースケールテクスチャで保持できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Blurs > Median filter grayscale
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 中間値フィルターのグレースケール
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5efb14d81ad72b1982785319e446d7eb318c9a03
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 1%

---


# 中間値フィルターのグレースケール

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![フィルターのグレースケールの中央値：アイコン](median-filter-grayscale.resources/MedianFilter_Icon_Grayscale.png "フィルターのグレースケールの中央値：アイコン")

<b>イン:</b>フィルター/ぼかし

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このフィルターは、エッジを保持しながら画像のノイズを滑らかにします。

各ピクセルについて、ノードはピクセルの隣接する領域の中央値に基づいてグレースケール値を計算します。

</td>
</tr>
</table>

>[!NOTE]
>
> [フィルターの色の中央値](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/blurs/median-filter-color/median-filter-color.md)も参照してください。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール</i> | フィルターを適用するグレースケールイメージです。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>出力</b> <i>グレースケール</i> | 入力グレースケールイメージにフィルターを適用することによって計算されるグレースケールイメージです。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>カーネルサイズ</b> *整数* | カーネルとは、フィルタの計算で使用される値の集合です。 この場合、隣接ピクセルの値になります。<br><br>各ピクセルに対して、フィルタは正方形のカーネル内のピクセルの周囲のすべての近隣の値を取得し、すべての近隣の中央値を計算します。<br><br>このパラメーターは、その正方形のカーネルのサイズをピクセル単位で制御します。 大きなカーネルを使用すると、より強力で広範囲に及ぶ平滑効果が得られますが、詳細な情報が多少犠牲になります。<br><br>*- 3x3:*&#x200B;カーネルの幅3ピクセル、高さ3ピクセル、隣接ピクセルの合計8ピクセル。<br>*- 5x5:*&#x200B;カーネルの幅5ピクセル、高さ5ピクセル、隣接ピクセルの合計24ピクセル。 |
| <b>フィルターの種類</b> *整数* | カーネルでサンプリングされた近隣に適用される計算です。<br><br>*- Median:*&#x200B;すべての近隣の中央値を直接使用してください。<br>*- MLMAD:* &#39;Median Of Least Median Absolute Deviation&#39;を表します。 偏差は、値と中央値との差を考慮に入れて算出されます。 MLMAD法では、偏差の大きい方のピクセルによって歪む可能性がある中央値を直接使用する代わりに、すべての偏差の中央値を使用します。 このメソッドは、カーネルサイズに従って領域を平坦化する、より強いスムージング効果を生成します。 |

## 例

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant2A.png" alt="MedianFilter_Variant2A">
      <br><i>前</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant2B.png" alt="MedianFilter_Variant2B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant4A.png" alt="MedianFilter_Variant4A">
      <br><i>前</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant4B.png" alt="MedianFilter_Variant4B">
      <br><i>後</i>
    </td>
  </tr>
</table>

<table>
  <tr>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant1A.png" alt="MedianFilter_Variant1A">
      <br><i>前</i>
    </td>
    <td>
      <img src="median-filter-grayscale.resources/MedianFilter_Variant1B.png" alt="MedianFilter_Variant1B">
      <br><i>後</i>
    </td>
  </tr>
</table>
