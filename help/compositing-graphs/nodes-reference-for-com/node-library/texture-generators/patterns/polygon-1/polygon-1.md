---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/polygon-1.html"
breadcrumb-title: ''
description: Polygon 1ノードを使用して、ジオメトリテクスチャのカスタマイズ可能な側面とプロパティを持つ基本的なポリゴンパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Polygon 1
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多角形1
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 7%

---


# 多角形1

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](polygon-1.resources/polygon-1-1.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

調整のための多くのオプションを持つ多角形を生成します。 より単純なバージョンについては、[ポリゴン2](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/polygon-2/polygon-2.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>辺</b> <i>3 - 32</i> | 多角形の辺の数を設定します。 |
| <b>分解</b> <i>0.0 - 1.0</i> | 多角形の「スライス」を離します。 |
| <b>三角形サイズ</b> <i>0.0 - 1.0</i> | スライス/三角形のサイズを調整します。 調整をおこなうと、シェイプは1,1だけ分解されます。 完全に連携しています。 |
| <b>スケール</b> <i>0.0 - 1.0</i> | シェイプ全体を1つにスケールします。 |
| <b>自動スケール</b> <i>False/True</i> | 既定のパラメータを使用して、ポリゴン全体がビューに収まるように尺度調整します。 |
| <b>回転</b> <i>0.0 - 1.0</i> | シェイプ全体を回転します。 |
| <b>グラデーション</b> <i>False/True</i> | ベタ塗りではなくグラデーションスライス/三角形を生成します。 注：この設定を有効にすると、ポリゴン2に似た状態になります。 |
| <b>グラデーション反転</b> <i>False/True</i> | 「グラデーション」が有効な場合に、グラデーション方向を反転します。 |
| <b>タイル表示</b> <i>1 - 16</i> | 結果をタイルする回数を設定します。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチを非正方形の比率で補正できます。 |
| <b>非正方形タイリング</b> <i>False/True</i> | 非正方形拡張が有効な場合、これによりシェイプが押しつぶされずに並べて表示されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="polygon-1.resources/polygon-1-ex.gif" />
        </td>
    </tr>
</table>
