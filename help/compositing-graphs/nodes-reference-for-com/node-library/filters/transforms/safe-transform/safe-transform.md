---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: '[セーフトランスフォーム]ノードを使用すると、テクスチャの境界を維持し、アーティファクトを回避しながら変換を適用できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: セーフ変換
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# セーフ変換

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## セーフ変換（グレースケール）

**場所：** *フィルター/変換*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

タイリングセーフバージョンの[Transform 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)。 タイリングを壊すことなく、またオフセットと回転が小さいためにピクセルのディテールを失うことなく（鮮明さやシャープネスの損失）、拡大・縮小、回転、オフセットすることができます。

最大限のコントロールや完全なシャープが必要な場合に、ノイズを変形するのに便利です。

## パラメーター

* **タイル**: *1 - 16*&#x200B;入力を並べて縮小します。
* **オフセットモード**: *手動、ランダム*&#x200B;手動で定義されたオフセットではなく、ランダムなオフセットに切り替えます。
* **オフセット**: *0.0 - 1.0*\
  結果を移動または変換します。 ピクセルがスナップされ、補間されていないことを確認します。
* **回転**: *0.0 ～ 1.0*&#x200B;入力を角度に沿って回転します。
* **タイルセーフ回転**: *False/True*&#x200B;回転の動作を決定します。ピクセルをぼかさないセーフ値にスナップするかどうかを指定します。
* **対称**: *なし、X、Y、X+Y*
* **背景色**: *（カラー値） （カラーバージョンのみ）*
* **Mipmapモード**: *自動、手動* mipmappingモードを決定します。 これを「手動」に設定すると、よりシャープな結果になります。
* **ミップマップレベル**: *0 - 10* Mipmapモードが手動に設定されている場合、別のMipmapを選択できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
