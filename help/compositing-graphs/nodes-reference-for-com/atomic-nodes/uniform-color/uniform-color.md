---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/uniform-color.html"
breadcrumb-title: ''
description: '[色を統一]ノードを使用して、単色の塗り潰しとベースレイヤを作成するための均一な色のテクスチャを生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Uniform color
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 均一カラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '182'
ht-degree: 8%

---


# 均一カラー

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード：均一な色](uniform-color.resources/comp_uniform_1.png "原子ノード：均一な色"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

フラットなグレースケールまたはカラー値を生成します。

これは、カラーを追加したり、特定の値を作成したりするための出発点として頻繁に使用される単純なノードです。

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

>[!TIP]
>
> パフォーマンスの最適化
> 
> どちらの調整も、ノードの計算時間とメモリのフットプリントを削減します。
> 
> * グレースケール値が必要な場合は、ノードの[カラーモード](#parameters)を&#39;グレースケール&#39;に切り替えてください。
> * ノードの出力は単色なので、できるだけ低い解像度を使用します。 ノードの&#39;[出力サイズ](../../../../compositing-graphs/output-size/output-size.md)&#39;パラメーターを&#39;絶対&#39; [継承メソッド](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)、解像度16 x 16ピクセルを使用するように設定します。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## パラメーター

</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | グレースケールとカラー出力画像を切り替えます。 |
| <b>出力色</b> *フロート/フロート4* | 出力画像に使用する単色を選択します。   「カラー」カラーモードを使用する場合、Alphaチャンネルは不透明度に使用されます。0は完全に透明で、1は完全に不透明です。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *カラー/グレースケール* |  |

## 例

*近日公開。*
