---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-blend.html"
breadcrumb-title: ''
description: マテリアルのブレンドノードを使用すると、複合マテリアル効果を作成するためのマスクを使用して、マテリアル全体をブレンドできます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: db158eba37ce52811a853adc20ca6143f96a79b6
workflow-type: tm+mt
source-wordcount: '458'
ht-degree: 6%

---


# マテリアルブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-blend.resources/material-blend.png){width="128px"}

<b>イン:</b> マテリアルフィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

マテリアルブレンドは、[アトミックブレンドノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)に相当するマルチチャンネルのフルマテリアルです。 グレースケールマスクに基づいて、または必要に応じてカラー ID マスクから1つの単色に基づいて、2つの完全なマテリアル（可能なすべてのチャンネル）をブレンドします。

このノードは、2つのマテリアルをブレンドし、グレースケールマップはあるがフルカラーIDベイク処理がない場合に便利です。 カラーIDベイク処理を行っていて、3つ以上のマテリアルをブレンドする場合は、[マルチマテリアルブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/multi-material-blend/multi-material-blend.md)を使用することをお勧めします。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>色ID</b> <i>カラー入力</i> | オプションのベイクカラーIDマップ。 |
| <b>グレースケールマスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用します。 |
| <b>拡散</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>基本色</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>標準</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>Specular</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>放射体</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>光沢</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>粗さ</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>メタリック</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>Specular level</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>環境オクルージョン</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>Height</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>不透明度</b> |  |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景のブレンドの不透明度 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> |  |
| <b>カラー ID マスク</b> <i>False/True</i> | グレースケールマスクの代わりにカラー ID マスクを使用します。 これは1つのカラーのみに適用されることに注意してください。 |
| <b>色</b> <i>（カラー値）</i> | 選択して白に変換する色。 |
| <b>ぼやけ</b> <i>0.01 - 1.0</i> | 選択したカラーが隣接するカラーとブレンドされる度合い。 |
| <b>パディング</b> <i>0.0 - 1.0</i> | 選択したカラーのトランジションコントラスト。 |
