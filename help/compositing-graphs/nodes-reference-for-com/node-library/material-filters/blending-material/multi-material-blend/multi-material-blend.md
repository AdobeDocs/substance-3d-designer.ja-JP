---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: 複数マテリアルのブレンドノードを使用すると、複数のマテリアルをブレンドして、複雑なマテリアルの組み合わせを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチマテリアルブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# マルチマテリアルブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-material-blend.resources/multi-material-blend.png){width="128px"}

<b>イン:</b> マテリアルフィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、マテリアルID/カラーIDマップに基づいて複数のマテリアルを組み合わせます。これは、メッシュからベイク処理できるマテリアルです。 最大16種類のマテリアルが用意されており、[チャンネル]領域で有効にするチャンネルの種類に関係なく使用できます。

このノードは、すべてのプロップを動的に結合しながらマテリアルを完全にパラメータ化できるため、完全なプロップをテクスチャリングする場合に非常に便利です。 適切なIDベイクを持つ単純な小道具から複雑な小道具のテクスチャリングに最適で、チームの標準に完全に統合する、完全にパイプライン化された「テンプレート」Substanceの作成にも最適です。

これを使用する場合、マテリアル1、スロット1は常に既定のマテリアルであり、他のマテリアルが表示されない場所に表示されることに注意してください。 そのため、カラーを設定できません。 このセーフを再生する場合は、たとえばラフブラックに設定された[ベースマテリアル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)を差し込みます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>1～16個のフルマテリアルスロット</b> | スロットの数は、<b>マテリアル</b>のドロップダウンによって決まります。 |
| <b>色ID</b> <i>カラー入力</i> | ベイクカラーIDマップ： |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>マテリアル</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | ブレンドする異なるマテリアルの最大量を設定します。 |
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>マテリアル 2-16</b> | 有効なマテリアルごとに1つのグループが表示されます。 |
| <b>色</b> <i>（カラー値）</i> | このマテリアルスロットに一致するID マップから選択する色です。 |
| <b>ぼやけ</b> <i>0.01 - 1.0</i> | 周囲のカラーににじみ出します。 |
| <b>パディング</b> <i>0.0 - 1.0</i> | トランジションの硬さ：マスクコントラスト。 |
