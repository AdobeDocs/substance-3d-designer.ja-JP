---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/tile-random.html"
breadcrumb-title: ''
description: 「タイルランダム」ノードを使用して、自然なテクスチャ効果に対してプロシージャルのバリエーションを持つランダム化されたタイルパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Tile Random
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: タイルをランダムに
user-guide-description: ''
user-guide-title: ''
source-git-commit: b63bc7a45aa6eadef1b72eb05d4a6aded05866a8
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 7%

---


# タイルをランダムに

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tile-random.resources/tile-random.png){width="128px"}

<b>イン：</b>ジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

タイルをランダムに選択すると、プロシージャルしたタイルパターンが作成されます。タイルの形状は、対応する[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)よりも少しカオスな状態になります。 これは、ランダムに特定のタイルを小さなタイルに分割することによってこれを行います。 多くのコンセプトが似ているため、タイルランダムに取り組む前に、まずTile Generatorについて考えてみることをお勧めします。

目標が古い見た目の整理されていないパターンである場合は、[Tile Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)の代わりにタイルランダムが使用されます。 ただし、制限があるので、他の高度なニーズには[Samplerを並べて表示](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)を検討してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パターン入力</b> <i>グレースケール入力（カラー入力）</i> | カスタムパターン画像。「Pattern」パラメーターが「Image Input」に設定されている場合に使用されます。 |
| <b>バックグラウンド入力</b> <i>グレースケール入力（カラー入力）</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>X金額</b> <i>1 - 64</i> | パターンのX繰り返しの量。 |
| <b>Y金額</b> <i>1 - 64</i> | パターンのY繰り返しの量。 |
| <b>非正方形拡張</b> <i>False/True</i> | カボチャと伸縮の補正を非正方形の比率で有効にします。 |
| <b>パターン</b> |  |
| <b>パターン</b> <i>パターン入力，正方形，円盤， 放物面,ベル，ガウス， とげ, ピラミッド, レンガ,グラデーション，波，ハーフベル,うね付きベル,三日月,カプセル,円錐</i> | 使用するパターン形状を選択します。 |
| <b>画像入力フィルタリング (エンジン > v4)</b> <i>バイリニア+ミップマップ，バイリニア，最も近い</i> |  |
| <b>パターン固有</b> <i>0.0 - 1.0</i> | 選択したパターンのシェイプを変更できます。 効果は選択したパターンによって異なります。 |
| <b>パターン固有のランダム</b> <i>0.0 - 1.0</i> | ランダム化効果は、選択したパターンに依存します。 |
| <b>回転</b> <i>0, 90, 180, 270,ランダムな水平方向，ランダムな垂直方向</i> | 回転を90度ステップで設定します。オプションでランダム化します。 |
| <b>ランダムな回転</b> <i>0.0 - 1.0</i> | ランダムな自由回転を追加します。 |
| <b>対称ランダム</b> <i>0.0 - 1.0</i> | 選択した対称ランダムモードで特定のパターンをランダムにミラーします。 この値が大きいほど、ミラーされるパターンの数が多くなります。 |
| <b>対称ランダムモード</b> <i>水平方向+垂直方向、水平方向、垂直方向</i> | 対称ランダムが0より大きい場合のミラーリングの動作を指定します。 |
| <b>分割</b> |  |
| <b>モード</b> <i>なし、自動、水平方向に自動、垂直方向に自動、ランダムh+v</i> | タイルの分割方法に関するルールを設定します。 |
| <b>しきい値</b> <i>0.0 - 1.0</i> | タイルを分割するタイミングに合わせてサイズが変更されます。 |
| <b>乗数</b> <i>0 - 10</i> | マルチプライヤの分割 この値が大きいほど、より多くの分割が行われます。 |
| <b>サイズ</b> |  |
| <b>ランダムX</b> <i>0.0 - 1.0</i> | X軸全体に不均等にスケーリングします。 |
| <b>ランダムY</b> <i>0.0 - 1.0</i> | Y軸に均等でないスケーリングをランダムにします。 |
| <b>間隔</b> |  |
| <b>モード</b> <i>最小のレンガを基準にする、最大のレンガを基準にする</i> | レンガサイズの間隔を設定します。 |
| <b>金額</b> <i>0.0 - 1.0</i> | レンガ間の隙間のサイズを設定します。 |
| <b>図形</b> |  |
| <b>スケール</b> <i>0.0 - 1.0</i> | すべてのタイルをグローバルに拡大縮小します。 |
| <b>ランダムに拡大・縮小</b> <i>0.0 - 1.0</i> | タイルごとにランダムにスケーリングします。 |
| <b>回転</b> <i>0.0 - 1.0</i> | 各タイルのグローバルな回転。 |
| <b>ランダムな回転</b> <i>0.0 - 1.0</i> | タイルごとにランダムに回転します。 |
| <b>回転制約</b> <i>False/True</i> | 回転したタイルが重なり合わないように、尺度を制限します。 |
| <b>位置</b> |  |
| <b>オフセット</b> <i>0.0 - 1.0</i> | タイルをグローバルに移動または移動します。X軸でのみスライドします。 |
| <b>オフセットランダム</b> <i>0.0 - 1.0</i> | タイルごとにオフセットをランダム化し、X 軸にスライドします。 |
| <b>ランダム</b> <i>0.0 - 1.0</i> | X方向とY軸の両方でタイルが動いて、位置がランダムになります。 |
| <b>ランダム制約</b> <i>False/True</i> | タイルが接するようにスケールを制限しますが、重ならないようにします。 ランダム位置エフェクトのトーンを大幅に下げます。 |
| <b>色</b> |  |
| <b>色</b> <i>（グレースケール値） / （カラー値）</i> | すべてのタイルに単色を設定します。 |
| <b>カラーランダム</b> <i>0.0 - 1.0</i> | タイルごとにカラーをランダム化します。 |
| <b>色のパラメーター化</b> <i>なし、面積、サイズx、サイズy</i> | カラーバリエーションをこれらの設定のいずれかに依存させます。 |
| <b>カラーパラメーター化の強度</b> <i>0.0 - 1.0</i> | 上記のパラメーター化エフェクトの乗数です。 |
| <b>色パラメーター化効果（色のみ）</b> <i>RGB+Alpha、RGBのみ、Alphaのみ</i> | カラーのみのパラメーター化エフェクトを指定します。 |
| <b>背景色</b> <i>（グレースケール値） / （カラー値）</i> | 単色の背景色を設定します。 |
| <b>描画モード</b> <i>Add/Sub、Max / Add/Sub、ブレンド（カラー）</i> | タイルの描画モードを背景上に設定します。 |
| <b>マスク</b> |  |
| <b>ランダム</b> <i>0.0 - 1.0</i> | タイルのマスキングをランダムに開始します。 値が大きいほど、表示されるタイルの数が多くなります。 |
| <b>反転</b> <i>False/True</i> | マスクの結果を反転します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="tile-random.resources/tile-random-1.png" />
        </td>
    </tr>
</table>
