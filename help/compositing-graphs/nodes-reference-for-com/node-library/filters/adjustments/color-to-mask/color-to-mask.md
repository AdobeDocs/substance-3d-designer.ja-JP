---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/color-to-mask.html"
breadcrumb-title: ''
description: カラーをマスクにノードを使用して、特定のカラーをマスクに変換し、選択的な処理およびマスクエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Color to mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マスクするカラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# マスクするカラー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![マスクの色 – アイコン](../../../../../../assets/color_to_mask.png "マスクの色 – アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

カラー画像内の選択したカラーからグレースケールマスクを抽出します。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 入力

</td>
<td style="border: 0;" valign="top">

### 出力

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## 入力

|  |  |
| --- | --- |
| <b>入力</b>の色 | マスクがカラーに基づいて抽出される入力カラー画像。 |
| <b>カラー入力</b>カラー&#x200B;*&#39;カラー入力を使用&#39;が&#39;True&#39;に設定されている場合に使用可能* | ピクセルごとの参照カラーの定義に使用する入力カラー画像。 |

## 出力

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* | 生成されたマスクはグレースケールビットマップです。 |

## パラメーター

|  |  |
| --- | --- |
| <b>カラー入力を使用</b>ブール値 | ピクセルごとに参照カラーを定義するには、均一なカラーの代わりに入力画像を使用します。    入力画像は、<b>色入力</b>入力によって提供されます。 |
| <b>カラー</b>浮動小数点3 *&#39;カラー入力を使用&#39;が&#39;False&#39;に設定されている場合に使用可能* | カラー選択を実行する基準となる一定のカラー。 |
| <b>しきい値</b>浮動小数点 | 基準カラーとの距離を指定します。基準カラーの下では、カラーが選択されます。 |
| <b>選択範囲のフェード</b>浮動小数点 | カラー選択を参照色との距離に基づいてフェードします。 |
| <b>距離カラースペース</b>整数 | イコライズプロセスでは、カラーを比較してカラー間の距離を決定します。 特定のユースケースには、特定のカラースペースおよび距離アルゴリズムの方が適しています。   このドロップダウンリストでは、カラーの比較に使用するカラースペースを選択できます。<ul data-preserve-html="true"> <li data-preserve-html="true"><b><i>RGB （データ）:</i></b>色は、赤、緑、青のチャンネルに分割され、人間の知覚を無視してそれらの軸に沿ってまっすぐに分布します。 これは、生データを保持する画像に適しています。</li> <li data-preserve-html="true"><i>リニアsRGB （カラー）:</i>色は、赤、緑、青のチャンネルに分割され、ピクセルの光の強さに対してリニアに分散されます。 これは、ディスプレイで視覚化できる画像に適しています。</li> <li data-preserve-html="true"><b><i>輝度（カラー） :</i></b>カラーは、色相、クロマ、輝度の値に分割され、比較には輝度の値のみが使用されます。 これは、ディスプレイで視覚化できる画像に適しています。</li> <li data-preserve-html="true"><i>Lab (Color):</i>標準化された知覚的カラースペースです。「感じる」近くの色が実際には立方体で近くなるように色を分配します。 これは、ディスプレイで視覚化できる画像に適しています。</li> <li data-preserve-html="true"><i>角度（標準）:</i>カラーをベクトルのX、Y、Z軸に分割し、ドット積で比較します。 これは、接線空間法線を保持するイメージに適しています。</li> </ul> |
| <b>距離の重み</b>浮動小数点3 | Labカラー距離アルゴリズム(DeltaE2000)では、明度、クロマ、色相値ごとに特定の重み係数が導入されています。   値を小さくすると、色差アルゴリズムの要素の影響が小さくなります。   目は一般に、彩度(C)や色相(H)よりも明るさ(L)の差が大きいと受け入れるので、(L:C:H)のデフォルトの比率は(0.5:1:1)です。 0.5:1:1の比率では、彩度や色相と比較して明度に2倍の差が生じます。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

</td>
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
