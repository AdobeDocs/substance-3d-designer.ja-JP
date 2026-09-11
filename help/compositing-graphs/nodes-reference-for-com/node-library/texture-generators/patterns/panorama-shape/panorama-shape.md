---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/panorama-shape.html"
breadcrumb-title: ''
description: '[パノラマシェイプ]ノードを使用して、環境テクスチャを生成するためのパノラマ座標にマップされたシェイプを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Panorama Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パノラマシェイプ
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '208'
ht-degree: 6%

---


# パノラマシェイプ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](panorama-shape.resources/panorama-shape-1.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、プロシージャルの「Studio」タイプのパノラママップを生成するのに役立ちます。 スポットライトイメージを配置および変更したり、そのHDRプロパティを設定することができます。 複数のシェイプに対して連結できます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>シェイプ行列</b> | 結果を移動または移動します。カンバスと直接対話することで変更できます。 |
| <b>図形</b> <i>正方形、ディスク</i> | シェイプの種類を設定します。 |
| <b>図形の色</b> <i>（カラー値）</i> | シェイプのカラーを設定します。 |
| <b>図形の適用度</b> <i>0.0 - 100.0</i> | シェイプのHDR強度を設定します。 |
| <b>図形のソフト境界線</b> <i>0.0 - 1.0</i> | シェイプの境界線の柔らかさを変更します。 |
| <b>ホットスポットの適用度</b> <i>0.0 - 100.0</i> | シェイプのホットスポットのHDR強度を設定します。 |
| <b>ホットスポットのサイズ</b> <i>0.0 - 1.0</i> | シェイプ内のホットスポットのサイズを変更します。 |
| <b>ホットスポットフォールオフ</b> <i>0.0 - 1.0</i> | ホットスポットのフォールオフ、エッジのブレンドを変更します。 |
| <b>ホットスポットの位置</b> <i>0.0 - 1.0</i> | ホットスポットをシェイプに対して相対的に移動します。 |
| <b>背景を有効にする</b> <i>False/True</i> | 背景を単色で塗りつぶすことができます。 つまり、ブレンドによって連結できなくなったということです。 |
| <b>背景色</b> <i>（カラー値）</i> | 背景色を設定します。 |
| <b>テクスチャ入力を有効にする</b> <i>False/True</i> | 定義済みのシェイプの種類ではなく、カスタム入力が可能です。 |
