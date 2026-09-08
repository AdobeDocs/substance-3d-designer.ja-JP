---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
breadcrumb-title: ''
description: マルチブレンドノードを使用すると、複数のマテリアルをブレンドして、複雑なマテリアルの組み合わせを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Multi-Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 7%

---


# マルチブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

<b>イン:</b> マテリアルフィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、マテリアル ID /カラーID マップに基づいて複数のマテリアルを組み合わせます。1つはメッシュからベイクできます。 最大16種類のフルマテリアルを使用でき、「チャンネル」グループでどのような種類のチャンネルを有効にしてもかまいません。

このノードは、フルプロップをテクスチャリングする場合に非常に便利です。すべてのプロップをダイナミックに結合しながら、マテリアルを完全にパラメータ化することができます。 適切なID ベイクを持つ単純な小道具から複雑な小道具へのテクスチャリングに最適です。また、チームの標準に完全に統合する、パイプライン化された「テンプレート」Substanceの作成にも最適です。

これを使用する場合、マテリアル1、スロット1は常にデフォルトのマテリアルであり、他のマテリアルが表示されない場所に表示されることに注意してください。 そのため、カラーを設定できません。 このセーフを再生する場合は、たとえばラフブラックに設定された[ベースマテリアル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)を差し込みます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>1～16個のフルマテリアルスロット</b> | スロットの数は、<b>マテリアル</b>のドロップダウンによって決まります。 |
| <b>色ID</b> <i>カラー入力</i> | カラーID マップをベイクしました。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>マテリアル</b> <i>2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16</i> | ブレンドする異なるマテリアルの最大量を設定します。 |
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。例えば、メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合などです。 |
| <b>マテリアル 2-16</b> | 有効なマテリアルごとに1つのグループが表示されます。 |
| <b>色</b> <i>（カラー値）</i> | このマテリアルスロットに一致するID マップから選択する色です。 |
| <b>ぼやけ</b> <i>0.01 - 1.0</i> | 周囲のカラーににじみ出します。 |
| <b>パディング</b> <i>0.0 - 1.0</i> | トランジションの硬さ：マスクコントラスト。 |
