---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/clone-filter-node.html"
breadcrumb-title: ''
description: コピーフィルターノードを使用して、テクスチャ領域を複製およびオフセットし、シームレスなパターン作成およびタイリング効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Clone (Filter Node)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: クローン（フィルタノード）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 03373417b3d82a278c159aa83baf282b67c9cbe3
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 4%

---


# クローン（フィルタノード）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/clone-4.png)

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

指定した場所に入力画像のクローンを1回作成します。 単純な「コピースタンプ」ツールとして機能できます。

意図した結果を得るには、ある程度の注意が必要です。

* 理想的には、ブレンドは直線コピーにすぎないため、入力画像には（デカールのような）アルファチャンネルが含まれています。
* マスクはデフォルトで黒に設定されているので、すべての結果を確認するには、少なくとも均一な白のグレースケール値を挿入する必要があります。
* オフセットは、画像の外側を簡単にクリップするので、小さい値を使用します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>ソース</b> <i>カラー入力</i> | コピーする画像。 重要：画像にアルファチャンネルが含まれていることが理想的です。 |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 デフォルトは黒です。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>オフセット</b> <i>-</i> | 結果を移動または変換します。 正の値は左と上、負の値は右と下です。 小さい値1.0以上を使用すると、画像の外側に移動します。 |
| <b>マスクをぼかす</b> <i>0.0 - 10.0</i> | ぼかしフィルターをマスクに適用して、エッジをソフトにします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/clone-example.png" />
        </td>
    </tr>
</table>
