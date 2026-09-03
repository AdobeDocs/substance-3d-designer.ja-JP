---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/weathering/metal-weathering.html"
breadcrumb-title: ''
description: '[Metal Weathering]ノードを使用して、メッシュジオメトリに基づいて金属材料にリアルな錆効果と腐食効果を加えます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Weathering > Metal Weathering
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金属風化
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '284'
ht-degree: 14%

---


# 金属風化

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-weathering.resources/metal-weathering-01.png){width="128px"}

<b>イン：</b> メッシュベースのジェネレーター> 風化

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>標準WS</b> <i>カラー入力</i> | 内部エフェクトやマスキングに使用する、ベイク処理されたワールド空間の法線マップ。 |
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>詳細</b> |  |
| <b>標準の形式</b> <i>Direct X, Open GL</i> | 異なるノーマルマップ形式に切り替えます（グリーンチャンネルを反転します）。 |
| <b>マスク</b> <i>False/True</i> | マスクマップの使用のオン/オフを切り替えます。 |
| <b>効果</b> |  |
| <b>Dust</b> <i>0.0 - 1.0</i> |  |
| <b>汚れ</b> <i>0.0 - 1.0</i> |  |
| <b>損耗したエッジ</b> <i>0.0 - 1.0</i> |  |
| <b>ペイントの剥離</b> <i>0.0 - 1.0</i> |  |
| <b>錆</b> <i>0.0 - 1.0</i> |  |
| <b>錆の剥離</b> <i>0.0 - 1.0</i> |  |
| <b>錆の詳細</b> <i>錆、Verdigris</i> |  |
| <b>亀裂スケール</b> <i>1.0 - 16.0</i> |  |
| <b>亀裂のワープ強度</b> <i>0.0 - 1.0</i> |  |
| <b>シャープエッジScratchesスケール</b> <i>1.0 - 32.0</i> |  |
| <b>シャープなエッジScratchesのワープの強さ</b> <i>0.0 - 1.0</i> |  |
| <b>Rawメタルの色</b> <i>（カラー値）</i> |  |
| <b>Raw Metal Specularの色</b> <i>（カラー値）</i> |  |
| <b>Raw Metal 光沢度値</b> <i>（グレースケール値）</i> |  |
| <b>Raw Metal ラフネス値</b> <i>（グレースケール値）</i> |  |
| <b>ブレンド</b> |  |
| <b>Diffuseの適用度</b> <i>0.0 - 1.0</i> | 拡散反射光のブレンド強度。 |
| <b>Base colorの適用度</b> <i>0.0 - 1.0</i> | ベースカラーのブレンド強度。 |
| <b>法線の強度</b> <i>0.0 - 64.0</i> | 法線のブレンド強度。 |
| <b>Specularの適用度</b> <i>0.0 - 1.0</i> | Specularのブレンド強度。 |
| <b>光沢度の適用度</b> <i>0.0 - 1.0</i> | 光沢のブレンド強度。 |
| <b>ラフネスの適用度</b> <i>0.0 - 1.0</i> | 粗さのブレンド強度。 |
| <b>メタリック強度</b> <i>0.0 - 1.0</i> | メタリックのブレンド強度。 |
| <b>Ambient occlusionの適用度</b> <i>0.0 - 1.0</i> | アンビエントオクルージョンのブレンド強度。 |
| <b>Heightの適用度</b> <i>0.0 - 1.0</i> | Heightのブレンド強度。 |
