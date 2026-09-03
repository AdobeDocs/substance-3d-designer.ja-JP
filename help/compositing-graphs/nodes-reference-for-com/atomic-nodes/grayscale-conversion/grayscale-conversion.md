---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/grayscale-conversion.html"
breadcrumb-title: ''
description: さまざまな変換方法を使用してカラーテクスチャをグレースケールに変換するには、グレースケール変換ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Grayscale conversion
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グレースケール変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 7%

---


# グレースケール変換

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：グレースケール変換](grayscale-conversion.resources/grayscale-conversion-01.png "原子ノード：グレースケール変換"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

各カラーチャンネルの輝度に重み付けを行い、カラー画像をグレースケールに変換します。

このノードは、目的のチャンネル（1に設定する必要がある）を除くすべての「チャンネルの重み」を0に設定することにより、カラー画像からグレースケールチャンネルを抽出するための最適化方法として使用できます。

</td>
</tr>
</table>

ほとんどのノードは、グレースケールまたはカラーで出力するように設定できます。グレースケールまたはカラーは、簡単でパフォーマンス上の理由から好まれます。

実際、最初からグレースケールで作業し、ワークフローの後半で、例えば[グラデーションマップ](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)ノードを使用して、画像をカラー化することをお勧めします。

つまり、グレースケール変換ノードは通常、カラー画像をグレースケールに変換する場合にのみ使用されます。 その場合は、[グレースケール変換の詳細設定](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/grayscale-conversion-adv/grayscale-conversion-advanced.md)と[マスクの色](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/color-to-mask/color-to-mask.md)も参照してください。

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

## パラメーター

</td>
<td style="border: 0;" valign="top">

### 入力コネクタ

</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>チャンネルの太さ</b> *浮動小数点4* | グレースケール変換の各RGBAチャンネルのウェイトを設定します。   デフォルトでは、RGBチャンネルで均等に分割されます。 |
| <b>アルファを統合</b> *ブール値* | グレースケール値にはAlpha情報を含めることができないため、最終的なグレースケール結果に対するAlphaの動作を設定します。   *True*&#x200B;の場合、グレースケール変換は入力画像のAlphaチャンネルに対して乗算されます |
| <b>背景の値</b> *フロート* | 入力にアルファマスクが含まれている場合に、ベース背景値を設定します。 つまり、透明として扱うピクセルを指定します。   *&#39;アルファの平坦化&#39;が&#39;True&#39;に設定されている場合に使用できます。* |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *色*&#x200B;プライマリ | 処理するカラー画像。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール* |  |

## 例

*近日公開。*
