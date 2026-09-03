---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-square-transform.html"
breadcrumb-title: ''
description: Non-Square Transformノードを使用して、XおよびYスケールが独立している非正方形テクスチャにトランスフォームを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Square Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 非正方形の変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 4%

---


# 非正方形の変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](non-square-transform.resources/non-square-transform-01.png)

![](non-square-transform.resources/non-square-transform-02.png)

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[Transform 2D](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)の非正方形セーフバージョンです。 非正方形の比率を自動的に検出し、正方形の入力画像を非正方形カンバスに変換できます。

このノードを最大限に活用するには、いくつかの設定を正しく設定する必要があるため、[グラフパラメーター](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)を十分に理解してください。

* **グラフ**&#x200B;のサイズは非正方形である必要があります。そうでない場合、このノードは必要ありません。
* 非正方形トランスフォーム&#x200B;**ノード**&#x200B;の出力サイズを「*親に対して相対的*」に設定します。
* 入力を1つの位置に変換するだけの場合は、**ノードの**&#x200B;並べて表示モードを「*並べて表示しない*」に設定します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>タイルモード</b> <i>自動、手動</i> | 非正方形の自動補正を有効にするかどうかを指定します。 |
| <b>タイル</b> <i>1 - 16</i> | [タイルモード]が[手動]に設定されている場合にのみ使用できます。 タイリングセーフな方法でスケールを変更できます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 結果を移動または変換します。 負の値を入力するには、スライダーをダブルクリックします。 |
| <b>回転</b> <i>0.0 - 1.0</i> | 入力画像を回転します。 |
| <b>セーフ回転（正方形のみ）</b> <i>False/True</i> | ピクセルのシャープさを保つために、安全な値にスナップされます。 |
| <b>背景色</b> <i>（カラー値）</i> | 画像を塗りつぶす背景色。 基本パラメーターの[タイルモードが「*タイル表示なし*」](../../../../../../compositing-graphs/graph-parameters/graph-parameters.md)に設定されている場合にのみ表示されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-square-transform.resources/non-square-transform-03.png" />
        </td>
    </tr>
</table>
