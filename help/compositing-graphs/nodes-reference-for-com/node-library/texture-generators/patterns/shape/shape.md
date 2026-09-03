---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape.html"
breadcrumb-title: ''
description: シェイプノードを使用して、Substance 3D Designerでパターンやテクスチャを作成するための基本的な幾何学的シェイプを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '217'
ht-degree: 6%

---


# シェイプ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape.resources/shape-01.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

基本シェイプを編集するためのオプションを使用して、様々なプロシージャルシェイプを作成します。 シェイプは常に完全に補間され、高精度です。

シンプルであるにもかかわらず、これは非常に便利なノードです。これは、最もプロシージャル的なHeightmap世代の構成要素です。 基本的なシェイプと変形ノードを組み合わせることで、ビットマップよりもはるかに正確な完全にプロシージャルしたハイトマップシェイプを作成できます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>タイル表示</b> <i>1 - 16</i> | 結果をタイルする回数を設定します。 |
| <b>パターン</b> <i>正方形、円盤、放物面、ベル、ガウス、とげ、ピラミッド、レンガ、グラデーション、波、ハーフベル、うね付きベル、クレカント、カプセル、円錐、半球</i> | 使用するパターン形状を選択します。 |
| <b>パターン固有</b> <i>0.0 - 1.0</i> | 選択したパターンのシェイプを変更できます。 効果は選択したパターンによって異なります。 |
| <b>スケール</b> <i>0.0 - 1.0</i> | シェイプ全体を拡大縮小します。 |
| <b>サイズ</b> <i>0.0 - 1.0</i> | X方向またはY軸に不均等にスケーリングできます。 |
| <b>角度</b> <i>0.0 - 1.0</i> | シェイプ全体を回転します。 |
| <b>回転45°</b> <i>False/True</i> | 事前に設定された45度回転します。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |
| <b>非正方形タイリング</b> <i>False/True</i> | 非正方形拡張が有効な場合、これによりシェイプが押しつぶされずに並べて表示されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape.resources/shape-02.gif" />
        </td>
    </tr>
</table>
