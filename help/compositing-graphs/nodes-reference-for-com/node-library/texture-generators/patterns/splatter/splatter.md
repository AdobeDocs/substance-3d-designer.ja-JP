---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/splatter.html"
breadcrumb-title: ''
description: スプラッタノードを使用して、テクスチャ間でシェイプを散乱化し、ランダムなパターンや有機的なテクスチャディテールを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプラッタ
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '340'
ht-degree: 9%

---


# スプラッタ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](splatter.resources/splatter.png)

![](splatter.resources/splatter-color.png)

<b>イン：</b>テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

スプラッタは、マップ入力をランダムに配置するためのパターンジェネレータです。 幾何学的にパターン化された配置のための多くのコントロールがあり、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)よりも使いやすくなっています。 後者の場合も同様の結果を得ることができますが、はるかに複雑です。

スプラッタは、何度も微調整しなくても、一部のシェイプをすばやく型抜きするのに適しています。

デフォルトのスプラッタパラメータは全くランダムに表示されないことに注意してください。ランダム化を行うには、一部を微調整する必要があります（主にディセーションパラメータ）。 また、スプラッタを使用するにはマップ入力が必要です。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>パターンサイズの幅</b> <i>0.0 - 1000.0</i> | X軸で使用するパターンの数。 |
| <b>パターンサイズのHeight</b> <i>0.0 - 1000.0</i> | Y軸で使用するパターンの数。 |
| <b>回転</b> <i>-360.0 - 360.0</i> | すべてのパターンを設定量だけ回転します。 |
| <b>回転バリエーション</b> <i>0.0 - 360.0</i> | すべての個別のシェイプにランダムな回転を導入します。 |
| <b>ズーム</b> <i>100.0 - 10000.0</i> | 最終結果を拡大します。 タイリングが壊れていることに注意してください。 |
| <b>ゲイン</b> <i>0.0 - 10.0</i> | すべてのパターンの描画ゲインを調整します。 より目立つようになります。 |
| <b>パンX</b> <i>-100.0 - 100.0</i> | X軸上で結果を丸ごとパンします。 |
| <b>パンY</b> <i>-100.0 - 100.0</i> | 結果をY軸にパンします。 |
| <b>障害</b> <i>0.0 - 100.0</i> | シェイプをランダムにシフトします。 |
| <b>グリッド番号</b> <i>0 - 8</i> | 結果のスケールを調整するために、様々なグリッドサイズにジャンプします。 タイルを維持します。 |
| <b>乱雑な角度</b> <i>0.0 - 360.0</i> | 乱れの変化の角度をコントロールします。 |
| <b>ランダムな障害</b> <i>False/True</i> | 乱れの角度をランダム化し、さらにカオスを加えます。 |
| <b>パターンサイズ</b> <i>5 - 12</i> |  |
| <b>サイズのバリエーション</b> <i>0.0 - 100.0</i> | すべてのシェイプにランダムな拡大・縮小を導入します。 |
| <b>画像入力フィルタリング （エンジン > v4のみ）</b> <i>バイリニア+ミップマップ，バイリニア，最も近い</i> | 入力画像に適用するフィルタリング。 |
| <b>出力レベルの最小値</b> <i>0.0 - 1.0</i> | 最小レベル調整が不足しています。 |
| <b>出力レベルの最大値</b> <i>0.0 - 1.0</i> | 最大レベル調整が不足しています。 |
| <b>背景色</b> <i>（グレースケール値）</i> | 単色の背景色を設定します。 |
| <b>輝度バリエーション</b> <i>0.0 ～ 1.0 （グレースケールバージョンのみ）</i> | 輝度のバリエーションを導入します。 |
| <b>カラーバリエーション</b> <i>0.0 ～ 1.0 （カラーバージョンのみ）</i> | カラーバリエーションを導入します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="splatter.resources/splatter-ex.gif" />
        </td>
    </tr>
</table>
