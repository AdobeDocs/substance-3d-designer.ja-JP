---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Atlas Splitterノードを使用して、テクスチャアトラスを個別のテクスチャに分割し、スキャンしたマテリアルを処理します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas Splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/atlas-splitter.png "ノードアイコン")

<b>内：</b>個のマテリアルフィルター/スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

アトラス画像の入力を取得し、すべての個別の要素を&#x200B;*個々のマテリアル*&#x200B;として分割します。

また、すべてのエレメントを再編成し、グリッドに移動するためにも使用できます。

このノードは、[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)ノードの高度なアプリケーションとして機能します。

</td>
</tr>
</table>

## パラメーター

<b>グリッドビュー</b> *ブール値*\
検出されたすべての図形をグリッドに表示します。

<b>グリッドの不透明度</b> *浮動小数点*\
グリッドビューがTrueの場合にグリッドラインの不透明度を設定します。 デバッグオプション

<b>グリッド選択の不透明度</b> *浮動小数点*\
グリッド表示がTrueの場合に、グリッド選択ハイライトの不透明度を設定します。 デバッグオプション

<b>自動スケール</b> *ブール値*\
グリッドセルに合わせて図形を自動的にスケールします。

<b>自動切り抜き</b> *ブール値*\
空きスペースを最小限に抑えるために、最大のシェイプに従って出力サイズを自動的に切り抜きます。

<b>図形の選択</b> *整数*\
グリッド表示では、ハイライト表示するセルを設定し、グリッド表示の外側では、返すセルを設定します。

<b>小さい図形を無視</b> *浮動小数点*\
対角線のサイズが指定した値よりも小さい図形を無視します。

<b>自動回転</b> *ブール値*\
バウンディングボックスのサイズ比率に従ってシェイプを自動的に回転します。

<b>回転</b> *浮動小数点*\
グローバルシェイプの回転角度

<b>標準形式の入力</b> *整数*\
入力法線の形式を設定します。 間違った形式を設定すると、間違った結果になります。

<b>不透明度マスクを縮小</b> *整数*\
不透明度マスクをダウンスケールして、ノイズや孤立したピクセルを除去します。 これにより、不要なシェイプの検出が防止され、パフォーマンスが向上します。

<b>拡張幅</b> *フロート*\
標準チャンネルとHeightチャンネルを除くすべてのチャンネルに、不透明度マスクに基づいて拡張効果を適用します。

<b>追加入力を有効にする</b> *ブール値*\
USer 1およびUser 2の入力と設定を、対象となっていない追加のマップで使用できるようにします。

<b>カスタム背景色</b> *ブール値*\
レイヤーの内容を拡張するのではなく、カスタムの背景色を選択できます。

<b>ベースカラーの背景カラー</b> *浮動小数点3*\
ベースカラーのカスタム背景色。

<b>標準の背景カラー</b> *浮動小数点3*\
法線マップのカスタムBGカラー

<b>メタリック背景カラー</b> *浮動小数点*\
メタリックのカスタムBGカラー。

<b>粗さの背景カラー</b> *浮動小数点*\
粗さのカスタム背景カラー

<b>Heightの背景の色</b> *浮動小数点*\
Heightのカスタム背景カラー

<b>ユーザー1 Bgカラー</b> *浮動小数点*\
カスタムユーザー1マップのカスタムBGカラー

<b>ユーザー2 Bgカラー</b> *浮動小数点*&#x200B;カスタムユーザー1マップのカスタムBGカラー

## 例
