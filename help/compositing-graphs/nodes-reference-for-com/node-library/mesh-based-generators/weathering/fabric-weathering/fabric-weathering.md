---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/fabric-weathering.html"
breadcrumb-title: ''
description: ファブリック風化ノードを使用して、メッシュのジオメトリと曲率に基づいて、ファブリックマテリアルに摩耗と経年変化の効果を加えます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Fabric Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 織物風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6eb38d6ccaadda1d070e4e0b67311312adb7d082
workflow-type: tm+mt
source-wordcount: '483'
ht-degree: 8%

---


# 織物風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/fabric-weathering.png){width="128px"}

<b>イン：</b> メッシュベースのジェネレーター> 風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これは完全なマテリアル効果で、複数のチャンネルで同時に機能します。 年齢と汚れをコントロールして、ランダムなファブリックの摩耗効果を追加します。<br>適切にベイクされたAOとワールド空間のノーマルマップを挿入しないと、すべてが適切に計算および生成されるため、この効果はあまり効果がありません。

フルマテリアルを使用する場合は、[リンク作成モード](../../../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)について十分に理解してください。

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
| <b>使用済み</b> <i>0.0 - 1.0</i> | AOに基づいて、非常に暗い累積された折り目のDirtのブレンド。 「最大」と「最小」の値は極端に変化する傾向があるため、注意して使用してください。 |
| <b>年齢</b> <i>0.0 - 1.0</i> | グローバルなタイリングの摩耗パターンに対するブレンド。 下のトレッシュホールドコントロールはAOの影響を制御します。 「最大」と「最小」の値は、極端に変化する傾向があります。 |
| <b>年齢しきい値</b> <i>0.0 - 1.0</i> | AOがAgeパラメータに影響する範囲を設定します。 |
| <b>年齢の折り目</b> <i>0.0 - 1.0</i> | エージエフェクトでかすかに追加した折り目のブレンドを制御します。 |
| <b>シャープエッジScratchesスケール</b> <i>1.0 - 32.0</i> | 小さな傷のスケールを設定します。これは主に使用済みとエイジ効果を取り除きます。 |
| <b>シャープなエッジScratchesのワープの強さ</b> <i>0.0 - 1.0</i> | 上の小さな傷のワープの強さを設定します。 |
| <b>古いファブリックの彩度低下</b> <i>0.0 - 1.0</i> | エージエフェクトの彩度を下げます。 |
| <b>古いファブリックの明るさ</b> <i>0.0 - 1.0</i> | エージエフェクトの明るさを調整します。 *これは、好みに合わせて変更する必要がある非常に重要なパラメーターですが、結果は極端になる場合があります。小さな変更で使用してください。* |
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
            <img src="../../../../../../assets/fabric-ex.gif" />
        </td>
    </tr>
</table>
