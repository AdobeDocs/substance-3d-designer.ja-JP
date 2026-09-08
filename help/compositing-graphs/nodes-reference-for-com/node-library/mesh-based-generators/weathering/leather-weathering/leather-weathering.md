---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/leather-weathering.html"
breadcrumb-title: ''
description: レザー風化ノードを使用して、メッシュの曲率に基づいてレザーマテリアルに磨耗パターンとエージングエフェクトを加えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Leather Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レザー風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 9%

---


# レザー風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/leather-weathering.png){width="128px"}

<b>イン：</b> メッシュベースのジェネレーター> 風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これは完全なマテリアル効果で、複数のチャンネルで同時に機能します。 年齢と汚れをコントロールしながら、ランダムなレザーの摩耗効果を追加します。 [ファブリック風化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/weathering/fabric-weathering/fabric-weathering.md)に似ていますが、特に革に合わせて調整されています。<br>適切にベイクされたAOとワールド空間のノーマルマップを埋め込まない限り、この効果は効果がありません。すべてのデータを適切に計算して生成するには、これらを使用する必要があります。

フルマテリアルを使用する場合は、[リンク作成モード](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)について十分に理解してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>標準のワールド空間</b> <i>カラー入力</i> |  |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>詳細</b> |  |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>マスク</b> <i>False/True</i> | マスクマップの使用のオン/オフを切り替えます。 |
| <b>効果</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> | ワールド空間のノーマルマップで上を向いた領域に基づく、暗いDust効果のブレンド。 |
| <b>汚れ</b> <i>0.0 - 1.0</i> | グローバルなDirt/指先エフェクトのブレンドです。主にAOの隠れた（暗い）領域に基づきます。 |
| <b>損耗したエッジ</b> <i>0.0 - 1.0</i> | マテリアル法線に基づいて、エッジにシャープ/強調エフェクトを追加します。 |
| <b>使用済み</b> <i>0.0 - 1.0</i> | グローバルな着用革仕様のブレンド。 |
| <b>年齢</b> <i>0.0 - 1.0</i> | 着用革のブレンドは、AOに基づいて折り目に見えます。 配置はAge Tresholdに大きく影響されます。 |
| <b>年齢しきい値</b> <i>0.0 - 1.0</i> | エイジ効果のアピアランスのしきい値を設定します。 |
| <b>亀裂スケール</b> <i>1.0 - 16.0</i> | [使用済み]および[エージ]効果から磨耗した革の深度を設定します。 |
| <b>亀裂ワープの強さ</b> <i>0.0 - 1.0</i> | [使用済み]と[エージ]の効果から、損耗した革の強度を設定します。 |
| <b>シャープエッジScratchesスケール</b> <i>1.0 - 32.0</i> |  |
| <b>シャープなエッジScratchesのワープの強さ</b> <i>0.0 - 1.0</i> |  |
| <b>使用されているレザーの彩度低下</b> <i>0.0 - 1.0</i> | AgeとUsedの効果から、摩耗した革の外観の彩度を設定します。 |
| <b>使用されている革の明るさ</b> <i>0.0 - 1.0</i> | AgeとUsedエフェクトから使用されている革の外観の明るさを設定します。 |
| <b>ブレンド</b> |  |
| <b>Diffuseの適用度</b> <i>0.0 - 1.0</i> | 拡散反射光のブレンド強度。 |
| <b>Base colorの適用度</b> <i>0.0 - 1.0</i> | ベースカラーのブレンド強度。 |
| <b>法線の強度</b> <i>0.0 - 1.0</i> | 法線のブレンド強度。 |
| <b>Specularの適用度</b> <i>0.0 - 1.0</i> | Specularのブレンド強度。 |
| <b>光沢度の適用度</b> <i>0.0 - 1.0</i> | 光沢のブレンド強度。 |
| <b>ラフネスの適用度</b> <i>0.0 - 1.0</i> | 粗さのブレンド強度。 |
| <b>Ambient occlusionの適用度</b> <i>0.0 - 1.0</i> | アンビエントオクルージョンのブレンド強度。 |
| <b>Heightの適用度</b> <i>0.0 - 1.0</i> | Heightのブレンド強度。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-ex.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/leather-ex2.png" />
        </td>
    </tr>
</table>
