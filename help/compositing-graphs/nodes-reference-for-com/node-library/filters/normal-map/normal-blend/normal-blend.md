---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/normal-blend.html"
breadcrumb-title: ''
description: 法線ブレンドノードを使用して法線マップをブレンドし、サーフェスのディテール間の滑らかな変化を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Normal Blend
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 標準ブレンド
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '160'
ht-degree: 2%

---


# 標準ブレンド

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/normal-blend.png){width="128px"}

## 標準ブレンド

**場所：** *フィルター/法線マップ*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

「法線ブレンド」を使用すると、すべての値を正規化した状態に保ちながら、2つの法線マップをオプションのマスクとブレンドできます。 [アトミックブレンドノード](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)とほとんど変わりませんが、ノーマルマップの内部計算が追加されました。

法線ブレンドは、法線マップを結合（オーバーレイ）するためのものではありません。法線マップでは、上のマップが下のマップに詳細を追加します。 その場合は、代わりに[通常の結合](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/normal-combine/normal-combine.md)を使用します。

## パラメーター

### 入力

* **NormalFG**: *カラー入力*\
  前景/上法線マップ：
* **NormalBG**: *カラー入力*\
  背景/下部の法線マップ：
* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。 「マスクを使用」パラメーターで切り替えることができます。

### パラメーター

* **不透明度**: *0.0 ～ 1.0*\
  前景と背景のブレンドの不透明度
* **マスクを使用**: *False/True*\
  マスクマップの使用のオン/オフを切り替えます。

## サンプル画像

![](../../../../../../assets/normalblend-ex.gif)

*（.gif形式はディザリングを導入しています。アプリケーション内の結果はスムーズです）*

</td>
</tr>
</table>
