---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/brick-generator.html"
breadcrumb-title: ''
description: '[レンガジェネレータ]ノードを使用して、カスタマイズ可能なサイズ、オフセット、モルタルのプロパティを使用してプロシージャルのレンガパターンを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Brick Generator
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レンガジェネレータ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 79916cdb133abb1a43d11012c9d23c3c6d27b079
workflow-type: tm+mt
source-wordcount: '211'
ht-degree: 8%

---


# レンガジェネレータ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/brick-generator.png){width="128px"}

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高度なレンガパターンジェネレーター。 人工的なレンガパターンを作成するためのオプションが多数あります

その他のオプションについては、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レンガ</b> <i>1 - 64</i> | レンガの量をX方向とY軸の両方で設定します。 |
| <b>ベベル</b> <i>0.0 - 1.0</i> | レンガのベベルプロファイルを変更します。2方向に変更したり、フォールオフプロファイルやコーナーの丸めを設定できます。 |
| <b>縦横比を維持</b> <i>False/True</i> | ベベルプロファイルをレンガサイズに関連付けるかどうかを指定します。 |
| <b>ギャップ</b> <i>0.0 - 1.0</i> | レンガ間に残すギャップ。 ベベルもギャップを発生させることに注意してください。したがって、ベベルも設定すると、このパラメーターで補正する必要があります。 |
| <b>中央サイズ</b> <i>0.0 - 1.0</i> | レンガパターンのオフセット。1列または1行おきにサイズを変更します。 |
| <b>Height</b> <i>-1.0 - 1.0</i> | Heightプロファイルを変更します。 輝度のバリエーションやあらゆる種類のランダム化が可能です。 |
| <b>勾配</b> <i>-1.0 - 1.0</i> | レンガごとに勾配を発生させます。特定のレンガを斜めに寝かせているような効果を与えます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 行単位でレンガをオフセットし、行ごとの間隔に影響します。 |
| <b>非正方形拡張</b> <i>False/True</i> | カボチャと伸縮の補正を非正方形の比率で有効にします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/brick-generator-ex-01.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/brick-generator-ex-02.gif" />
        </td>
    </tr>
</table>
