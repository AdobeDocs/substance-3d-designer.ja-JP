---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-color-blend.html"
breadcrumb-title: ''
description: マテリアルの色のブレンドノードを使用して、マテリアル間のカラーチャンネルをブレンドし、合成マテリアル効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Color Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルカラーブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 2%

---


# マテリアルカラーブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-color-blend.resources/material-color-blend-01.png){width="128px"}

<b>イン:</b> マテリアルフィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードを使用すると、その上に単色をブレンドして、マルチチャンネル、フルマテリアルに調整することができます。 これは、[マテリアル調整ブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/blending-material/material-adjustment-blend/material-adjustment-blend.md)との主な違いです。このブレンドでは、チャンネルに対して[レベル](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/levels/levels.md)の種類の調整のみが可能ですが、このノードでは、単色の[ブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)の種類の調整を使用しています。

このノードは、拡散反射光またはベースカラーにフラットカラーのヒントを導入する場合、または設定されたソリッドカラー値を使用して他のチャンネルを「フラット」にする場合に最も便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>色ID</b> <i>カラー入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>グレースケールマスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用します。 |
| <b>拡散</b> |  |
| <b>色</b> <i>（カラー値）</i> | Diffuseチャンネルの上でブレンドするカラー値。 |
| <b>不透明度</b> <i>0.0 - 1.0</i> | 前景と背景の間のブレンド不透明度。 |
| <b>描画モード</b> <i>標準、追加、減算、乗算、追加/サブ、最大、最小、切り替え</i> | オペレーションで使用するブレンドモード。 |
| <b>基本色</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>標準</b> |  |
| <b>ソース</b> <i>Height、マスク</i> |  |
| <b>描画モード</b> <i>結合、ブレンド</i> |  |
| <b>Heightの適用度</b> <i>0.0 - 1.0</i> |  |
| <b>Heightの不透明度</b> <i>0.0 - 1.0</i> |  |
| <b>形式</b> <i>DirectX、OpenGL</i> |  |
| <b>Specular</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>放射体</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>光沢</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>粗さ</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>メタリック</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>Specular level</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>環境オクルージョン</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>Height</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>不透明度</b> | このチャンネルの一番上に単色をブレンドし、[拡散反射光]領域のオプションを使用します。 |
| <b>カラー ID マスク</b> <i>False/True</i> | グレースケールマスクの代わりにカラー ID マスクを使用します。 これは1つの色に対してのみ有効です。<br><br>以下のすべてのオプションを有効にします。 |
| <b>色</b> <i>（カラー値）</i> | 選択して白に変換する色。 |
| <b>ぼやけ</b> <i>0.01 - 1.0</i> | 選択したカラーが隣接するカラーとブレンドされる度合い。 |
| <b>パディング</b> <i>0.0 - 1.0</i> | 選択したカラーのトランジションコントラスト。 |
