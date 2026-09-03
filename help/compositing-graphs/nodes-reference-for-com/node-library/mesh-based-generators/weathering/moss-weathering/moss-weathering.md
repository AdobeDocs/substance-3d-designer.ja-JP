---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/moss-weathering.html"
breadcrumb-title: ''
description: '[コケの風化]ノードを使用して、メッシュの曲率と位置に基づいてマテリアルにコケの成長パターンを追加します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Moss Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: コケ風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 7%

---


# コケ風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](moss-weathering.resources/moss-weathering-01.png){width="128px"}

<b>イン：</b> メッシュベースのジェネレーター> 風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

これは完全なマテリアル効果で、複数のチャンネルで同時に機能します。 このエフェクトは、伝播を1つのコントロールで制御して、オーバーグロウンモスエフェクトを生成します。

このエフェクトは、ベイク処理されたワールド空間の位置マップと追加のハイトマップで最適に機能します。 これは正確な要件ではありませんが、効果をより信頼できる配置に貸します。

完全なマテリアルを扱う場合は、[リンク作成モード](https://support.allegorithmic.com/documentation/display/SD5/Link+Creation+Modes)を正しく理解してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>位置</b> <i>カラー入力</i> | ベイクワールドスペースの位置。 |
| <b>Height</b> <i>グレースケール入力</i> | 追加のHeightmap入力。 |
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
| <b>コケの伝播</b> <i>0.0 - 1.0</i> | コケの広がりを設定します。 わずかな被覆率から、厚く厚い暗いコケまで、段階的に成長します。 |
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
            <img src="moss-weathering.resources/moss-weathering-02.gif" />
        </td>
    </tr>
</table>
