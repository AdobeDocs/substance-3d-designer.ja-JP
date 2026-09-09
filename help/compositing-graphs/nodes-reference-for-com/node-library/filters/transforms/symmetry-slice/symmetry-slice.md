---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/symmetry-slice.html"
breadcrumb-title: ''
description: 対称スライスノードを使用すると、対称軸に沿ってテクスチャをスライスし、ミラーされたパターンやエフェクトを作成することができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Symmetry Slice
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 対称スライス
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 6%

---


# 対称スライス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](symmetry-slice.resources/mirror-2.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

複雑なシンメトリ/ミラーリング操作ノード。 フルコントロールで様々な幾何演算が可能ですが、多少の実験が必要です。

[ミラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/mirror-filter-node/mirror-filter-node.md)および[対称](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/symmetry/symmetry.md)と比較すると、このノードにはさらに多くのオプションがあります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>対称モード</b> <i>0 - 6</i> | 対称ジオメトリ/対称軸を選択します。 オプションには、「水平方向」、「垂直方向」、「左右斜め」、「左右斜め」、「左右斜め」、「垂直反転」、「コーナー」、「対角角コーナー」があります。 |
| <b>転送モード</b> <i>0 - 6</i> | 描画モード。 次のオプションがあります。 |
| <b>ブレンド</b> <i>0.0 - 1.0</i> | 元の画像を結果に再びブレンドします。 |
| <b>左右反転</b> <i>False/True</i> | 原点を反転します。これは、操作の原点の側が反転することを意味します。 たとえば、左から右への対称は右から左になります。 |
| <b>左右反転2</b> <i>False/True</i> | 対称モードが5または6の場合にのみ使用します。 コーナーの原点を反転します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="symmetry-slice.resources/symslice.png" />
        </td>
    </tr>
</table>
