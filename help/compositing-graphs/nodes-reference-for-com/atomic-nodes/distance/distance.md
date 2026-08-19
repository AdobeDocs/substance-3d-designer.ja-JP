---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/distance.html"
breadcrumb-title: ''
description: '[距離]ノードを使用して、シェイプから距離マップを計算し、マスクや手続き型の効果を作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Distance
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 距離
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 8%

---


# 距離

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：距離](../../../../assets/comp_distance_1.png "原子ノード：距離"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

マスク内の最も近い白ピクセルの位置を求め、その位置からグラデーションを出力するか、ソース画像内のその位置のカラーを出力します。

このノードは、0.5グレースケール値を超える入力maxの任意のピクセルから外向きの線形フェード（グラデーション）を作成します。

</td>
</tr>
</table>

外側に広がるフェードは、別のセルに接するとすぐに終了し、重なることはありません。 内部的には、距離ノードをクランプ/最大値に設定して、最も近いピクセル> 0.5までの距離を計算して表示します。

オプションのソースマップを使用すると、セルを二次入力マップのテクスチャと組み合わせることができます。

距離ノードはマスターするのが簡単なノードではありませんが、主なユースケースは、既存のマスクを確実な方法で拡張すること（ぼかしやコントラストの調整と比較した場合）、ボロノイ型のノイズセルを生成すること、およびシャープな線形プロファイルで既存のシェイプをベベルすることです（これは後で再マッピングできます）。

詳細については、以下の[例](#examples)を参照してください。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | グレースケールとカラー出力画像を切り替えます。 また、「ソース入力」入力タイプも変更されます。 |
| <b>最大距離</b> *フロート* | マスクの最も近い境界線を検出するための最大距離をピクセル単位で調整します。 |
| <b>ソース/距離の結合</b> *ブール値* | オプションの「ソース入力」を最終セルと組み合わせる方法を指定します。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>結合：</i> &#39;ソース入力&#39;値をフェードする線形マスクと結合します。 「ソース入力」入力が接続されている場合、その値は計算された距離と結合されます。</li> <li data-preserve-html="true"><i>ソースのみ：</i> &#39;ソース入力&#39;からのみ単色になります。</li> </ul> |
| <b>距離モード</b> *整数* | 抽出されたマスクの最も近い境界までの距離を計算する方法を選択します。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>ユークリッド：</i>X/Y差の平方和。</li> <li data-preserve-html="true"><i>マンハッタン：</i> X/Y差の絶対値の合計。</li> <li data-preserve-html="true"><i>Chebyshev:</i> X/Y差の絶対値の最大値です。</li> </ul>  <div><img alt="距離モードの例" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_table_copy_copy_copy_row-yj03rtt-column-0i13nfd_image" src="../../../../assets/distance-comparison.jpg" title="距離モードの例"/></div> |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>マスク入力</b> *グレースケール*&#x200B;プライマリ | グレースケールマスクは、境界線の距離の値を計算する必要があります。   0.5のしきい値を使用して画像からバイナリマスクが抽出されます。この値を超えるすべての値は白で、下回るすべての値は黒です。 |
| <b>ソース入力</b> *カラー/グレースケール* | オプションのグレースケール画像。この画像から、「マスク入力」の最も近い境界にあるピクセル値をコピーします。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *カラー/グレースケール* |  |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/distance-ex01.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/distance-ex02.gif){width="250px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/distance-ex03.gif){width="250px"}

</td>
</tr>
</table>
