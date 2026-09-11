---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/material-selector.html"
breadcrumb-title: ''
description: マテリアルセレクタノードを使用して、マルチマテリアルテクスチャ効果を作成するためのメッシュデータに基づいてマテリアルを選択します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Material Selector
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルセレクター
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '179'
ht-degree: 5%

---


# マテリアルセレクター

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-selector.resources/material-selector.png){width="128px"}

<b>In:</b> メッシュベースのジェネレータ>ユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

フルカラーのIDマップを、白黒のバイナリマスクに変換します。 異なるカラーをブレンドして1つのマスクに結合できます。

これは、[マルチマテリアルのブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)を使用せずにマスクを手動で使用する場合や、同じマスクを他の場所で手動で使用する場合に便利です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>マテリアル</b> <i>1 - 16</i> | 結合が有効になっているマテリアルの数を設定します。 |
| <b>マテリアル #1-16を有効にする</b> <i>False/True</i> | 最終的な出力マスクへのカラーのブレンドと合成を切り替えます。 結合するカラーの数に応じて有効にできます。 |
| <b>マテリアル #1-16</b> <i>（カラー値）</i> | 白黒に変換されるマテリアルカラーのカラーピッカー。 |
| <b>カラーピッカーパラメーター</b> | カラーのブレンドと、カラーの白黒への変換を変更します。 |
| <b>ぼやけ</b> <i>0.01 - 1.0</i> | 隣接するカラーとどれだけブレンドするかを指定します。 |
| <b>パディング</b> <i>0.0 - 1.0</i> | コントラストなど、変化のシャープさ。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="material-selector.resources/matselector-ex.png" />
        </td>
    </tr>
</table>
