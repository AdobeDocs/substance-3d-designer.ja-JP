---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/cracks-weathering.html"
breadcrumb-title: ''
description: 風化ノードを使用して、メッシュ曲率と応力点に基づいてマテリアルに亀裂パターンを追加します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Cracks Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 3%

---


# 風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](cracks-weathering.resources/cracks-weathering.png){width="128px"}

<b>イン：</b> メッシュベースのジェネレーター> 風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これはフルマテリアルのエフェクトで、複数のチャンネルで同時に機能します。 拡散と深度を制御して、ランダムな亀裂パターンを追加します。

フルマテリアルを使用する場合は、[リンク作成モード](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)を正しく理解してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲率</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスキングに使用する、ベイクまたは生成されたマップ。 |
| <b>Height</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスキングに使用する、ベイクまたは生成されたマップ。 |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。例えば、メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合などです。 |
| <b>詳細</b> |  |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>マスク</b> <i>False/True</i> | マスクマップの使用のオン/オフを切り替えます。 |
| <b>効果</b> |  |
| <b>亀裂の伝達</b> <i>0.0 - 1.0</i> | 亀裂がどの程度広がるかを指定します。 このエフェクトのメインコントロールです。 |
| <b>深度</b> <i>0.0 - 1.0</i> | クラック効果の深度。 主にHeightに生じ、わずかに腟のThicknessにも生じる。 |
| <b>ブレンド</b> | 生成される各チャンネルにエフェクトをブレンドする強さを制御します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="cracks-weathering.resources/cracks-ex.gif" />
        </td>
    </tr>
</table>
