---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/quad-transform.html"
breadcrumb-title: ''
description: クアッドメニューの[変形]ノードを使用して、遠近法の補正とワープを行うテクスチャに四辺形変換を適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Quad Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 四角形の変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 2%

---


# 四角形の変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](quad-transform.resources/quad-transform-01.png){width="128px"}

![](quad-transform.resources/quad-transform-02.png){width="128px"}

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

特別な変形ノードで、四角形のシェイプをコーナーポイントとのインタラクションを通してトランスフォームできます。 非常に具体的な変形を実践的に行えます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>p00</b> | 左上のポイント： |
| <b>p01</b> | 左下の点 |
| <b>p10</b> | 右上のポイント。 |
| <b>p11</b> | 右下の点： |
| <b>カリング</b> <i>前面のみ、背面のみ、前面から背面、背面から前面</i> | ポイントが互いに交差している場合のシェイプのカリング/非表示を設定します。 |
| <b>タイリングを有効にする</b> <i>False/True</i> |  |
| <b>背景色</b> <i>（グレースケール値）</i> | タイリングがオフの場合は、背景色は塗りつぶされます。 |
| <b>サンプリング</b> <i>バイリニア、最も近い</i> | サンプリング品質を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="quad-transform.resources/quad-transform-03.gif" />
        </td>
    </tr>
</table>
