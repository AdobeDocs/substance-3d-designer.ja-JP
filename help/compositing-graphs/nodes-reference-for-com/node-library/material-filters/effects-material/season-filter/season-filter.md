---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/season-filter.html"
breadcrumb-title: ''
description: 季節フィルターノードを使用して季節の効果をマテリアルに適用し、春、夏、秋、冬のバリエーションを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Season Filter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 季節フィルター
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 11%

---


# 季節フィルター

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/default-icon.png){width="128px"}

<b>内：</b> マテリアルフィルター >エフェクト

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、アニメートされた水位、雪、氷、コケなどの効果を追加します。

これは、完全なPBR補正を目的としていない古いフィルターであることに注意してください。 これはレガシー/互換性の理由で保存されることが多いですが、場合によっては引き続き有用です。 最新のPBR補正版は、[Snowカバー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/snow-cover/snow-cover.md)と[水位](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/effects-material/water-level/water-level.md)で確認できます。

このノードでは、主に詳細なHeightmapまたはNormalmapを使用して、マテリアル入力の適切なセットが必要です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>詳細</b> |  |
| <b>標準の形式</b> <i>DirectX、OpenGL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>マスク</b> <i>False/True</i> | マスクマップの使用のオン/オフを切り替えます。 |
| <b>光の強さ</b> <i>0.0 - 1.0</i> | （偽装された）ライトの強度。 |
| <b>光源の角度</b> <i>0.0 - 1.0</i> | （偽）光の入射角 |
| <b>効果</b> |  |
| <b>Heightまたは標準からの効果</b> <i>Height、通常</i> | エフェクトを適用する入力マップを選択します。 |
| <b>水位</b> <i>0.0 - 1.0</i> | Height/法線の情報に基づいて水位を上昇または低下させます。 |
| <b>水の詳細</b> <i>0.0 - 1.0</i> | 水中のディテールの量を設定します。 |
| <b>屈折</b> <i>0.0 - 1.0</i> | エフェクトの擬似屈折の量を設定します。 |
| <b>リフレクション</b> <i>0.0 - 1.0</i> | エフェクトでの偽反射の量を設定します。 |
| <b>反射の距離</b> <i>0.0 - 1.0</i> | 反射のビジュアルを制御します。 |
| <b>反射角</b> <i>0.0 - 1.0</i> | 反射のビジュアルを制御します。 |
| <b>流れの方向</b> <i>0.0 - 1.0</i> | アニメーションの流れを制御します（Substance Playerを使用して表示します）。 |
| <b>氷</b> <i>0.0 - 1.0</i> | 水の凍結方法を設定します。 |
| <b>氷の詳細</b> <i>0.0 - 1.0</i> | 氷のディテールの量を設定します。 |
| <b>Snow</b> <i>0.0 - 1.0</i> | 積雪量を設定します。 |
| <b>コケ</b> <i>0.0 - 1.0</i> | コケの適用量を設定します。 |
| <b>コケのスケール</b> <i>1 - 4</i> | 生成されたコケのテクスチャのスケールを設定します。 |
| <b>コケの色</b> <i>（カラー値）</i> | コケのカラーを設定します。 |
| <b>水の色</b> <i>（カラー値）</i> | アルファ/不透明度を含む、水のカラーを設定します。 |
| <b>ブレンド</b> |  |
| <b>Diffuseの適用度</b> <i>0.0 - 1.0</i> | 拡散反射光のブレンド強度。 |
| <b>Base colorの適用度</b> <i>0.0 - 1.0</i> | ベースカラーのブレンド強度。 |
| <b>法線の強度</b> <i>0.0 - 1.0</i> | 法線のブレンド強度。 |
| <b>Specularの適用度</b> <i>0.0 - 1.0</i> | Specularのブレンド強度。 |
| <b>光沢度の適用度</b> <i>0.0 - 1.0</i> | 光沢のブレンド強度。 |
| <b>ラフネスの適用度</b> <i>0.0 - 1.0</i> | 粗さのブレンド強度。 |
| <b>Ambient occlusionの適用度</b> <i>0.0 - 1.0</i> | アンビエントオクルージョンのブレンド強度。 |
| <b>Heightの適用度</b> <i>0.0 - 1.0</i> | Heightのブレンド強度。 |
