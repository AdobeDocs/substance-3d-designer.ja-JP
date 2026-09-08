---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/safe-transform.html"
breadcrumb-title: ''
description: 「セーフ変形」ノードを使用すると、変形を適用する際に、テクスチャの境界を維持し、斑点を除去することができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Safe Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: セーフ変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 1%

---


# セーフ変形

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/safe-transform.png)

![](../../../../../../assets/safe-transform-grayscale.png)

## セーフ変形（グレースケール）

**場所：** *フィルター/変形*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

[2Dの変形](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)のタイリングセーフバージョンです。 オフセットと回転が小さいために、タイリングを損なうことなく、ピクセルのディテールを損なうことなく（鮮明さやシャープさの損失）、拡大・縮小、回転、オフセットできます。

最大限のコントロールや完全なシャープが必要な場合に、ノイズを変形するのに便利です。

## パラメーター

* **タイル**: *1 - 16*&#x200B;入力をタイリングして縮小します。
* **オフセットモード**: *手動、ランダム*&#x200B;手動で定義されたオフセットではなく、ランダムなオフセットに切り替えます。
* **オフセット**: *0.0 - 1.0*\
  結果を移動または移動します。 ピクセルがスナップされ、補間されていないことを確認します。
* **回転**: *0.0 ～ 1.0*&#x200B;入力を角度に沿って回転します。
* **タイルセーフ回転**: *False/True*&#x200B;回転の動作を決定します。この動作をピクセルをぼかさないセーフ値にスナップするかどうかを指定します。
* **対称**: *なし、X、Y、X+Y*
* **背景色**: *（カラー値） （カラーバージョンのみ）*
* **ミップマップモード**: *自動、手動*&#x200B;マッピングモードを決定します。 これを「手動」に設定すると、よりシャープな結果になります。
* **ミップマップレベル**: *0 ～ 10*&#x200B;ミップマップモードが[手動]に設定されている場合、別のミップマップを選択できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
