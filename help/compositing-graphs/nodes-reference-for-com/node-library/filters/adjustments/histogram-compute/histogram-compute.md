---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/histogram-compute.html"
breadcrumb-title: ''
description: '[ヒストグラムの計算]ノードを使用して、解析および処理のためにテクスチャからヒストグラムデータを計算します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Histogram compute
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ヒストグラム計算
user-guide-description: ''
user-guide-title: ''
source-git-commit: 25c39c29f26db98b103665dba13e7619ed624d0b
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 1%

---


# ヒストグラム計算

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ヒストグラムの計算：アイコン](histogram-compute.resources/histogram_compute.png "ヒストグラムの計算：アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

グレースケール画像のヒストグラムを計算します。

ヒストグラムは、画像内のピクセルの行としてエンコードされます。各ピクセル値は、X 軸上のピクセルの位置に一致するカラー値の&#x200B;*母集団*&#x200B;です。\
例えば、(0.25, 0)のピクセル値が75の場合は、画像に0.25のカラー値を持つ75個のピクセルが存在することを意味します。

</td>
</tr>
</table>

ノードは、画像に対して計算された&#x200B;*累積分布関数* (CDF)も出力します。

カスタムツールは、次の「例」セクションに示すように、カスタムマスクなどのノードによって計算されたデータを使用して作成できます。

>[!IMPORTANT]
>
> [0,1]範囲外の値はすべてクランプされるので、HDRイメージのヒストグラムが正確でない場合があります。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール</i>プライマリ | ヒストグラムの計算対象となる画像。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>ヒストグラム</b> <i>グレースケール</i> | 入力画像について計算されたヒストグラムで、ピクセルの行としてエンコードされます。各ピクセル値は、X 軸上のピクセルの位置に一致するカラー値の&#x200B;*母集団*&#x200B;です。   例えば、(0.25, 0)のピクセル値が75の場合は、画像に0.25のカラー値を持つ75個のピクセルが存在することを意味します。 |
| <b>CDF</b> <i>グレースケール</i> | 画像に対して計算された&#x200B;*累積分布関数* (CDF)の結果。各ピクセルが左側のすべてのピクセル値の合計であるピクセルの行にエンコードされます。   その合計は、画像内の総ピクセル数に対して&#x200B;*正規化*&#x200B;されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ヒストグラムの解像度</b> *整数* | ヒストグラムの幅。 値を大きくすると、より細かい値の分布が可能になります。   使用可能な解像度は、ピクセル単位で256、512、1024、2048、4096です |

## 例

![ヒストグラムの計算：例1](histogram-compute.resources/histogram_compute_example_1.jpg "ヒストグラムの計算：例1"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_before.jpg" alt="histogram_compute_example_2_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="histogram-compute.resources/histogram_compute_example_2_after.jpg" alt="histogram_compute_example_2_after">
      <br><i>後</i>
    </td>
  </tr>
</table>
