---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/effects-material/water-level.html"
breadcrumb-title: ''
description: '[水面]ノードを使用すると、水面のHeightに基づいてマテリアルをブレンドして、リアルな水面の効果を作成できます。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Effects (Material) > Water Level
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 水レベル
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# 水レベル

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](water-level.resources/water-level.png){width="128px"}

<b>内：</b> マテリアルフィルター >エフェクト

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

材料の全量に水分レベルを追加するオールインワンエフェクトです。 効果を適用するには、入力マテリアルに高画質のハイトマップが必要です。 結果はPBR-correctです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。 |
| <b>水位</b> <i>0.0 - 1.0</i> | メインコントロールは、水レベルを上げたり下げたりします。 |
| <b>水の闇</b> <i>0.0 - 1.0</i> | 水の一般的な「透明度」を設定します。 |
| <b>エッジの濡れ具合</b> <i>0.0 - 1.0</i> | 水のエッジの濡れた外観の度合いを指定します。 |
| <b>エッジの濡れ距離</b> <i>0.0 - 1.0</i> | 濡れたエッジの到達距離を設定します。 |
| <b>深度ぼかし量</b> <i>0.0 - 1.0</i> | 水中の深度に基づいてぼかしの量を設定します。 ぼかしの半径を変更します。 |
| <b>深度ぼかしの不透明度</b> <i>0.0 - 1.0</i> | 深度ぼかしのブレンド量を指定し、ぼかしの効果を下げるために使用します。 |
| <b>スラッジの色</b> <i>（カラー値）</i> | スラッジ効果のカラーを設定します。 |
| <b>汚泥深度</b> <i>0.0 - 1.0</i> | 水面に対して、スラッジが現れ始める深度を設定します。 |
| <b>スラッジの不透明度</b> <i>0.0 - 1.0</i> | スラッジエフェクトのグローバルな不透明度を設定します。 |
| <b>霜</b> <i>0.0 - 1.0</i> | 霜の量を設定します。 外側のエッジから表示を開始し、内側に移動します。 |
| <b>霜の強さ</b> <i>0.0 - 1.0</i> | 霜の強度を設定し、効果の「不透明度」を制御します。 |
| <b>霜の亀裂</b> <i>0.0 - 1.0</i> | 凍結から液体への変化の亀裂量を設定します。 |
| <b>フロスト通常形式</b> <i>DirectX/OpenGL</i> | フロストノーマルマップエフェクトのグリーンチャンネルを切り替えます。 |
