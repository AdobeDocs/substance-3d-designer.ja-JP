---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/physical-sun-sky.html"
breadcrumb-title: ''
description: 物理的なSunSkyノードを使用して、物理的に正確な太陽と空のライティング環境を生成し、リアルなマテリアルプレビューを実現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Physical SunSky
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 物理SunSky
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 9%

---


# 物理的な太陽/空

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](physical-sun-sky.resources/physical-sun-sky-01.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ホセック – ウィキエのスカイライトモデルに基づく物理的な太陽と空の実装。 人工的なHDRIのための優れたベースを提供します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>太陽の位置</b> | 範囲= [0,1]x[0,1] （経緯度角度） |
| <b>濁度</b> <i>1.0 - 10.0</i> | 濁度は1 ～ 10の範囲です |
| <b>アルベド</b> <i>0.0 - 1.0</i> | アルベドの範囲は0 ～ 1です。 |
| <b>地面の色</b> <i>（カラー値）</i> | グリッドの色。 |
| <b>露光量(EV)</b> <i>-1.0 - 4.0</i> | 結果出力の露光量。 |
| <b>太陽の大きさ</b> <i>0.0 - 4.0</i> | 太陽のスケール。1以外の値は物理的に正しくありません。 値には微妙な効果があります。 |
| <b>太陽の強さ</b> <i>0.0 - 1.0</i> | 太陽ディスクの強度。 Sunのディスクはかなり小さいので、効果はすぐに見えません。 |
| <b>空の適用度</b> <i>0.0 - 1.0</i> | 空の適用度。 また、ディスク自体ではなく、空での太陽の輝きに影響を与えます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="physical-sun-sky.resources/physical-sun-sky-02.gif" />
        </td>
    </tr>
</table>
