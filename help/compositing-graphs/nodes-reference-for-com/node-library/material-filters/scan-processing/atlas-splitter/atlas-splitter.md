---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/atlas-splitter.html"
breadcrumb-title: ''
description: Atlas Splitterノードを使用して、スキャンされたマテリアルを処理するためにテクスチャアトラスを個別のテクスチャに分割します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Atlas Splitter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Atlas Splitter
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---


# Atlas Splitter

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/atlas-splitter.png "ノードアイコン")

<b>イン：</b> マテリアルフィルター/スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

アトラス画像の入力を受け取り、すべての個別の要素を&#x200B;*個々のマテリアル*&#x200B;として分割します。

また、すべてのエレメントを整理し直して、グリッドに移動するためにも使用できます。

このノードは、[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)ノードの高度なアプリケーションとして機能します。

</td>
</tr>
</table>

## パラメーター

<b>グリッドビュー</b> *ブール値*\
検出されたすべての図形をグリッドに表示します。

<b>グリッドの不透明度</b> *フロート*\
グリッドビューがTrueの場合にグリッド線の不透明度を設定します。 デバッグオプション

<b>グリッドの選択範囲の不透明度</b> *フロート*\
グリッドビューがTrueの場合に、グリッド選択ハイライトの不透明度を設定します。 デバッグオプション

<b>自動スケール</b> *ブール値*\
図形をグリッドセルに合わせて自動的にスケールします。

<b>自動切り抜き</b> *ブール値*\
空きスペースを最小限に抑えるために、最大のシェイプに従って出力サイズを自動的に切り抜きます。

<b>図形の選択</b> *整数*\
グリッドビューでは、どのセルがハイライト表示されるかを設定し、グリッドビューの外側では、どのセルが返されるかを設定します。

<b>次より小さい図形を無視</b> *浮動小数*\
対角線のサイズが指定した値よりも小さい図形を無視します。

<b>自動回転</b> *ブーリアン*\
バウンディングボックスのサイズ比率に従ってシェイプを自動的に回転します。

<b>回転</b> *浮動小数*\
グローバルシェイプの回転角度

<b>標準形式を入力</b> *整数*\
入力法線の形式を設定します。 間違った形式を設定すると、間違った結果になります。

<b>不透明度マスクを縮小</b> *整数*\
不透明度マスクをダウンスケールして、ノイズの可能性があるピクセルや孤立したピクセルを削除します。 これにより、不要なシェイプの検出が防止され、パフォーマンスが向上します。

<b>拡張幅</b> *浮動小数*\
「標準」と「拡張」を除くすべてのチャンネルに、Height度マスクに基づく不透明度エフェクトを適用します。

<b>追加入力を有効にする</b> *ブーリアン*\
USer 1およびUser 2の入力と設定を、対象となっていない追加のマップで使用できるようにします。

<b>カスタム背景色</b> *ブール値*\
レイヤーのコンテンツの拡張ではなく、カスタムの背景色を選択できます。

<b>Base colorの背景の色</b> *浮動小数点3*\
base colorの背景色をカスタマイズします。

<b>標準の背景の色</b> *浮動小数点3*\
法線マップの背景色をカスタマイズします。

<b>メタリック背景の色</b> *フロート*\
メタリック用のカスタム背景カラー。

<b>ラフネスの背景の色</b> *フロート*\
ラフネスのカスタム背景カラー

<b>Heightの背景の色</b> *フロート*\
Heightのカスタム背景カラー

<b>ユーザー1 Bgカラー</b> *フロート*\
カスタムユーザー1マップのカスタムBGカラー

<b>ユーザー2 Bgカラー</b> *浮動小数*&#x200B;ユーザー1マップのカスタムBG色

## 例
