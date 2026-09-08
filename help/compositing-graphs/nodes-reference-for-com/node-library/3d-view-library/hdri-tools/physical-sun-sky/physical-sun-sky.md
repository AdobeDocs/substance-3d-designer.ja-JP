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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---


# 物理的な太陽/空

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/panorama-physical-sun-sky.png){width="200px"}

## 物理的な太陽/空

**イン：** *3D ビュー/HDRI ツール*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ホセック – ウィキエのスカイライトモデルに基づく物理的な太陽と空の実装。 人工的なHDRIのための優れたベースを提供します。

## パラメーター

* **太陽の位置**:\
  範囲= [0,1]x[0,1] （経緯度角度）
* **濁度**: *1.0 - 10.0*\
  濁度は1 ～ 10の範囲です
* **アルベド**: *0.0 ～ 1.0*\
  アルベドの範囲は0 ～ 1です。
* **地面の色**: *（色の値）*\
  グリッドの色。
* **露出(EV)**: *-1.0 - 4.0*\
  結果出力の露光量。
* **太陽の大きさ**: *0.0 ～ 4.0*\
  太陽のスケール。1以外の値は物理的に正しくありません。 値には微妙な効果があります。
* **太陽の強度**: *0.0 ～ 1.0*\
  太陽ディスクの強度。 Sunのディスクはかなり小さいので、効果はすぐに見えません。
* **空の強度**: *0.0 ～ 1.0*&#x200B;空の強度。 また、ディスク自体ではなく、空での太陽の輝きに影響を与えます。

## サンプル画像

![](../../../../../../assets/sky-ex.gif)

</td>
</tr>
</table>
