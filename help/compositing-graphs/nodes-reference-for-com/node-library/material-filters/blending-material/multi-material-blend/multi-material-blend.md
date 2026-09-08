---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/multi-material-blend.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 1%

---


# マルチマテリアルブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/multi-material-blend.png){width="128px"}

## マルチマテリアルブレンド

**イン：** *マテリアルフィルター/描画*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

このノードは、マテリアルID/カラーIDマップに基づいて複数のマテリアルを組み合わせます。これは、メッシュからベイク処理できるマテリアルです。 最大16種類のマテリアルが用意されており、[チャンネル]領域で有効にするチャンネルの種類に関係なく使用できます。

このノードは、すべてのプロップを動的に結合しながらマテリアルを完全にパラメータ化できるため、完全なプロップをテクスチャリングする場合に非常に便利です。 適切なIDベイクを持つ単純な小道具から複雑な小道具のテクスチャリングに最適で、チームの標準に完全に統合する、完全にパイプライン化された「テンプレート」Substanceの作成にも最適です。

これを使用する場合、マテリアル1、スロット1は常に既定のマテリアルであり、他のマテリアルが表示されない場所に表示されることに注意してください。 そのため、カラーを設定できません。 このセーフを再生する場合は、たとえばラフブラックに設定された[ベースマテリアル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/base-material/base-material.md)を差し込みます。

## パラメーター

### 入力

* **1～16個の完全なマテリアルスロット**&#x200B;スロットの数は、**マテリアル**&#x200B;ドロップダウンで決定されます。
* **カラーID**: *カラー入力*\
  ベイクカラーIDマップ：

### パラメーター

* **マテリアル**: *2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16*&#x200B;描画するマテリアルの最大量を設定します。
* **チャネル**\
  この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。
* **マテリアル 2-16**&#x200B;有効にしたマテリアルごとに1つのグループが表示されます。
  * **カラー**: *（カラー値）*このマテリアルスロットに一致するID マップから選択するカラー。
  * **ぼやけ**: *0.01 ～ 1.0*&#x200B;色が近くまで裁ち落とされます。
  * **パディング**: *0.0 ～ 1.0*&#x200B;トランジションの硬さ:マスクコントラスト。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
