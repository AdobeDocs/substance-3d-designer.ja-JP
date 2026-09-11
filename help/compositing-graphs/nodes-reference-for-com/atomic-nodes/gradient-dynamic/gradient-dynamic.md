---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/gradient-dynamic.html"
breadcrumb-title: ''
description: 入力パラメーターと値で制御できる動的なグラデーションを作成するには、グラデーション（動的）ノードを使用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Gradient (Dynamic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラデーション (ダイナミック)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 9%

---


# グラデーション (ダイナミック)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード： Gradient dynamic](gradient-dynamic.resources/comp_dyngradient_1.png "原子ノード： Gradient dynamic"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

別の画像のピクセルの行または列によって提供されたグラデーションを使用して、画像内のグレースケール値を再マップします。

これはグラデーションノードに代わるわずかな機能ですが、グラデーションノードとは異なり、グラデーションカラーキーは内部では定義されず、外部入力から取得されます。

</td>
</tr>
</table>

これは主に、カラーのパラメータがノードの外部に移動するため、パラメータを公開できない問題を回避することができます。 これが「ダイナミック」な機能です。

Gradient (Dynamic)は単独で使用するのが難しいノードではありませんが、使用する方がやや高度です。ほとんどの標準の使用は、通常のGradientノードでカバーできます。

このノードは、グラデーションエディターのキーシステムによって制限しすぎて、カラーとランプの位置をグラフの他の入力、パラメーター、および部分によって制御したい場合に役立ちます。

また、グラデーション入力位置スライダーを使用して、単一のランプ入力内に保存された複数のグラデーションを交互に切り替えることもできます。

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
| <b>グラデーションのアドレス指定</b> *ブール値* | グラデーションを繰り返す（タイル状にする）か、クランプするかを設定します。   このパラメーターは、グレースケール入力の[0, 1]の範囲のHDRピクセルのうち、[0, 1]までのクランプまたは折りたたみを処理する方法を指定します。 |
| <b>グラデーションの向き</b> *整数* | 「グラデーション入力」をサンプリングする軸を設定します。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>水平方向：</i> X軸のピクセル列をサンプリングします。</li> <li data-preserve-html="true"><i>垂直方向：</i> Y軸のピクセル列をサンプリングします。</li> </ul> |
| <b>グラデーションの入力位置</b> *フロート* | 「グラデーション入力」でサンプリングされるピクセルの行または列の正規化された位置。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>グレースケール入力</b> *グレースケール*&#x200B;プライマリ | 再マップするグレースケール画像。 |
| <b>グラデーション入力</b> *カラー/グレースケール* | グラデーションはこの画像からサンプリングされます |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *カラー/グレースケール* |  |

## 例

*近日公開。*
