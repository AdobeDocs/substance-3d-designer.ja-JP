---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/blending-material/material-adjustment-blend.html"
breadcrumb-title: ''
description: マテリアル補正ブレンドノードを使用して、マテリアル間のマテリアル補正をブレンドし、合成効果を微調整します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Blending (Material) > Material Adjustment Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアル調整ブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 2%

---


# マテリアル調整ブレンド

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/material-adjustment-blend.png){width="128px"}

<b>イン:</b> マテリアルフィルター/描画

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードでは、マスクに基づいて、マテリアル全体の任意のチャンネルとすべてのチャンネルを調整できます。 これは、完全なマテリアルワークフローをより簡単かつ迅速にすることを目的としています。

このエフェクトは、同じマスクに基づいてマテリアルの一部のチャンネルを補正する（拡散反射光を明るくしたりラフネスを暗くするなど）場合に便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>カラー ID マスク</b> <i>カラー入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>グレースケールマスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | このグループ内のマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスではなくSpecular/光沢度マップを使用する場合などです。<br><br>これにより、チャンネルの関連するグループの表示も有効または無効になります。 |
| <b>Diffuse</b> | マスクによって定義された領域のDiffuseチャンネルに対して調整処理を行います。 |
| <b>Base color</b> | マスクによって定義された領域のBase colorチャンネルに対して調整が行われます。 |
| <b>標準</b> |  |
| <b>適用度</b> <i>0.0 - 1.0</i> | 標準強度を下げる |
| <b>Specular</b> | マスクによって定義された領域のSpecularチャンネルに対して調整処理を行います。 |
| <b>Emissive</b> | マスクによって定義された領域のエミッシブチャンネルに対して調整操作を実行します。 |
| <b>光沢</b> | マスクによって定義された領域の光沢チャンネルに調整操作を実行します。 |
| <b>粗さ</b> | マスクによって定義される領域の粗さチャンネルに対して調整操作を実行します。 |
| <b>メタリック</b> | マスクによって定義された領域のメタリックチャンネルに対して調整操作を実行します。 |
| <b>Specular level</b> | マスクによって定義された領域のSpecular levelチャンネルに対して調整が行われます。 |
| <b>環境オクルージョン</b> | マスクによって定義された領域のアンビエントオクルージョンチャンネルに対して調整処理を行います。 |
| <b>Height</b> | マスクによって定義された領域のHeightチャンネルに対して調整が行われます。 |
| <b>不透明度</b> | マスクによって定義された領域の不透明度チャンネルに対して調整操作を実行します。 |
| <b>カラー ID マスク</b> <i>False/True</i> | グレースケールマスクの代わりにカラー ID マスクを使用するように設定します。 |
| <b>ぼやけ</b> <i>0.01 - 1.0</i> | カラー ID マスクが有効な場合、これによりColor IDの選択範囲カラーのスプレッドが決まります。 |
| <b>色</b> <i>（カラー値）</i> | カラーID マップから選択してマスクに使用するカラーを設定します。 |
| <b>パディング</b> <i>0.0 - 1.0</i> | カラーIDマスクの描画コントラスト/効果を指定します。 |
