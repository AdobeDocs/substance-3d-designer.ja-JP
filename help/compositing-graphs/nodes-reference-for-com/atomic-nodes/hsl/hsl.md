---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/hsl.html"
breadcrumb-title: ''
description: HSLノードを使用して、テクスチャの色相、彩度、明度を調整し、カラーの操作や補正を行います。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > HSL
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: HSL
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 9%

---


# HSL

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード： HSL](../../../../assets/comp_hsl_1.png "原子ノード： HSL"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

カラー画像の色相、彩度、明度を調整します。

これは基本的で使いやすいノードで、カラーデータを操作する場合に非常に便利です。

画像のトーンを他の方法で編集する場合は、[曲線](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)、[レベル](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)および[コントラスト/輝度](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/contrast-luminosity/contrast-luminosity.md)を確認してください。

</td>
</tr>
</table>

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
| <b>色相</b> *フロート* | 入力画像のカラーを指定します。   0.5より小さい値を指定すると色相が負にシフトし、0.5より大きい値を指定するとプラスにシフトします。 |
| <b>彩度</b> *フロート* | 入力画像のカラーの彩度を指定します。   0.5より小さい値を指定すると彩度が下がり、0.5より大きい値を指定すると彩度が上がります。 |
| <b>明るさ</b> *フロート* | 入力イメージの明度を決定します。0.5より小さい値を指定すると明度が下がり、0.5より大きい値を指定すると明度が上がります。 |

## 入力コネクタ

|  |  |
| --- | --- |
| <b>入力</b> *色*&#x200B;プライマリ | 処理する画像。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *色* |  |

## 例

*近日公開。*
