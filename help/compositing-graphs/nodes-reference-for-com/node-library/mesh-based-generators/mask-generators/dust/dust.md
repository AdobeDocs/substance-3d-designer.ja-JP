---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/dust.html"
breadcrumb-title: ''
description: Dustノードを使用して、メッシュジオメトリに基づいてDustのアキュムレーションマスクを作成し、リアルなDustと汚れのエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Dust
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Dust
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '203'
ht-degree: 5%

---


# Dust

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](dust.resources/dust.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、上に向いている領域だけでなく、閉塞した領域や下がっている領域にも蓄積されているDustを表します。 適切なベイク処理されたAOおよびワールド空間法線が動作する必要があります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | Dustの配置に使用するベイク済みマップ。 必須！ |
| <b>ワールド空間標準</b> <i>カラー入力</i> | Dustの配置に使用するベイク済みマップ。 必須！ |
| <b>ノイズ</b> <i>グレースケール入力</i> | カスタムDustマップ（オプション）。[ノイズのオーバーライド]が[True]に設定されている場合にのみ表示されます。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | Dustの合計量を設定します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | Dustのコントラストを調整します。 |
| <b>オクルージョン金額</b> <i>0.0 - 1.0</i> | AOのインフルエンスを設定します。オクルージョン領域により多くのDustが表示されます。 |
| <b>ノイズの不透明度</b> <i>0.0 - 1.0</i> | ほこりの多い領域に表示されるノイズ量を設定します。 |
| <b>ノイズの上書き</b> <i>False/True</i> | カスタムDustマップ入力を使用するように設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="dust.resources/dust-ex.gif" />
        </td>
    </tr>
</table>
