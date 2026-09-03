---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/surface-brush.html"
breadcrumb-title: ''
description: サーフェスブラシノードを使用して、サーフェスの方向に基づいてマスクを生成し、ディレクショナルウェザリングおよび摩耗効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Surface Brush
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 表面ブラシ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 7%

---


# 表面ブラシ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](surface-brush.resources/surface-brush-01.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、オブジェクトのジオメトリとAOによって隠された、オブジェクトのサーフェスに対する金属ブラシの興味深い効果を表します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>ワールド空間標準</b> <i>カラー入力</i> |  |
| <b>曲線</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>位置</b> <i>グレースケール入力</i> |  |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | グローバル効果レベルを設定し、徐々に表示します。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>Scratchesの長さ</b> <i>0.0 - 8.0</i> | スクラッチの長さを設定します。 小さい値を指定すると点に近くなり、大きい値を指定すると長い筋になります。 |
| <b>軸を隠す</b> <i>X、Y、Z、なし</i> | スクラッチを受けるオブジェクトの軸です。 傷の方向は変わりません。 |
| <b>軸強度を遮断</b> <i>0.0 - 1.0</i> | オクルージョン効果の強さです。 |
| <b>オクルージョン</b> <i>0.0 - 1.0</i> | 傷を塞ぐ上でAOの強さ。 |
| <b>シャープの適用度</b> <i>0.0 - 1.0</i> | 傷に適用するシャープ処理の適用量を設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="surface-brush.resources/surface-brush-02.gif" />
        </td>
    </tr>
</table>
