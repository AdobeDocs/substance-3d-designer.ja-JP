---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-splatter.html"
breadcrumb-title: ''
description: シェイプスプラッターノードを使用して、プロシージャルのパターンやディテールを作成するために、テクスチャ間でシェイプを散乱します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Splatter
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプスプラッタ
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '960'
ht-degree: 7%

---


# シェイプスプラッタ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-splatter.resources/shape-splatter.png){width="128px"}

<b>イン：</b> テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

付随するノード[シェイプスプラッタブレンド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-blend/shape-splatter-blend.md)、[シェイプスプラッタからマスク](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-to-mask/shape-splatter-to-mask.md)および[シェイプスプラッタデータの抽出](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-data-ext/shape-splatter-data-extract.md)と組み合わせて使用するように設計された、非常に複雑なノードです。 [Samplerを並べる](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)または[Generator](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)と同じように図形を分割するために使用しますが、[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)と同様の複数レベルのシステムを通じて、すべてのステップを制御できる動的で非破壊的なプロセスを使用します。 Flood Fillが外部ソースから基本入力マップを受け取るのに対し、Shape Splatterはマップを作成し、その後のデータを[Flood Fill](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/flood-fill/flood-fill.md)の一種の高度なバージョンとして1回の手順で生成します。

主な目的は、高さマップ上にシェイプを配置して動かし、スプラッタデータからさまざまなマップを作成することです。 例えば、岩、小枝、葉を風景の上に配置し、様々なマップで方向付けて駆動します。 Height、法線、ベースカラー、ラフネス、その他のチャンネルに異なるマップを使用できますが、すべてのマップは引き続き同じ共有スプラッタデータに基づいています。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>背景Height</b> <i>グレースケール入力</i> | タイルを配置して様々な効果を生み出す背景Height。 |
| <b>パターン1-8</b> <i>グレースケール入力</i> | オプションのパターン |
| <b>パターンの配布</b> <i>グレースケール入力</i> | グレースケールマップ |
| <b>シェイプの拡大・縮小</b> <i>グレースケール入力</i> | グレースケールマップはタイルの拡大・縮小を促進します。 |
| <b>図形の回転</b> <i>グレースケール入力</i> | グレースケールマップはタイルの回転を促進します。 |
| <b>Heightオフセット</b> <i>グレースケール入力</i> | タイルHeightのオフセットとして使用するグレースケールマップ。 |
| <b>Heightスケール</b> <i>グレースケール入力</i> | タイルHeightのオフセットとして使用するグレースケールマップ。 |
| <b>ランダムなマスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>ベクターマップ</b> <i>カラー入力</i> | タイルの配置と回転を促進するカラーベクトルマップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>X金額</b> <i>1 - 64</i> | パターンのX反復の量。 |
| <b>Y金額</b> <i>1 - 64</i> | パターンのY反復の量。 |
| <b>パターン</b> |  |
| <b>パターンの入力番号</b> <i>1 - 8</i> | 使用する異なるパターンの量を設定します。 新しいパターン入力スロットをロック解除します。 |
| <b>パターン配布モード</b> <i>ランダム、パターンインデックス、行インデックス、列インデックス</i> | 使用するパターンの決定方法を設定します。 ランダムに、またはパターン、線、列によって。 |
| <b>パターン分布マップ乗数</b> <i>0.0 - 1.0</i> | パターンの配置に対するオプションの分布マップの影響を設定します。 |
| <b>パターンの回転</b> <i>0, 90, 180, 270</i> | プリセットを設定、パターンを90度回転 |
| <b>パターンの回転ランダム</b> <i>0.0 - 1.0</i> | パターンに対してランダムな90度ステップ回転の量を設定します。 |
| <b>サイズ</b> |  |
| <b>スケール</b> <i>0.0 - 5.0</i> | すべてのタイルに同一スケールを設定します。 |
| <b>ランダムに拡大・縮小</b> <i>0.0 - 1.0</i> | タイルごとに均等スケールをランダム化します。 |
| <b>スケール（重なりを除く）</b> <i>0.0 - 1.0</i> | タイルが重ならないように、均一に（ただし下のみ）拡大・縮小をランダムに行います。 前の2つのパラメータと一緒に使用しないでください。 |
| <b>スケールマップマルチプライヤ</b> <i>0.0 - 1.0</i> | スケールマップの影響を設定します。 |
| <b>サイズ</b> <i>0.0 - 1.0</i> | タイルを不均等にスケーリングできます。 |
| <b>Bg 勾配からのサイズ比</b> <i>0.0 - 1.0</i> | 背景マップ勾配（計算済みの法線）を使用して、タイルを不均一に尺度変更します。 遠近法ワープをシミュレートします。 |
| <b>サイズ（X/Y量比）</b> <i>0.0 - 1.0</i> | XとYの量の異なる比率を補正するための不均等なスケーリング。 |
| <b>位置</b> |  |
| <b>ランダムな配置</b> <i>0.0 - 2.0</i> | すべてのタイルに対してオプションをランダムにオフセット |
| <b>ランダム配布</b> <i>ガウス、均一</i> | 前のパラメータに使用する計算を設定します。 大きな違いはありません。数値が高いほど顕著です。 「ガウス」を使用すると、スプレッドがより均一になる傾向があります。 |
| <b>ベクトルマップマルチプライヤ</b> <i>0.0 - 1.0</i> | オフセットに対するベクトル入力マップの影響。 |
| <b>水平方向のオフセット</b> <i>-2.0 - 2.0</i> | グローバル水平オフセット： |
| <b>垂直方向のオフセット</b> <i>-2.0 - 2.0</i> | グローバル垂直オフセット： |
| <b>枠からはみ出させるオプション</b> <i>シェイプを拡大・縮小、位置を固定</i> | タイルが範囲外に表示される場合に実行するアクション。 |
| <b>回転</b> |  |
| <b>回転</b> <i>0.0 - 1.0</i> | すべてのタイルをグローバルに回転します。 |
| <b>ランダムな回転</b> <i>0.0 - 1.0</i> | タイルごとにランダムに回転します。 |
| <b>Bg 勾配からの回転</b> <i>0.0 - 1.0</i> | 背景マップ勾配（計算済みの法線）を使用してタイルを回転させます。 勾配上でシェイプのポイントを上または下に設定するために使用できます。 |
| <b>回転マップ乗数</b> <i>0.0 - 1.0</i> | タイルごとの回転に対する回転マップの効果をブレンドします。 |
| <b>ベクトルマップマルチプライヤ</b> <i>0.0 - 1.0</i> | タイルごとの回転に対する回転マップの効果をブレンドします。 |
| <b>Height</b> |  |
| <b>Heightスケールの自動調整</b> <i>False/True</i> | 絶対範囲を指定する代わりに、背景に対して相対的にHeight範囲を自動調整します。 より少ない数または多くの制御を可能にします。 |
| <b>Heightオフセット</b> <i>-1.0 - 1.0</i> | Heightの範囲内ですべてのタイルを均等にオフセット/移動するモディファイヤ。 |
| <b>Heightオフセットランダム</b> <i>0.0 - 1.0</i> | タイルごとにHeightオフセットをランダムに変更します。 |
| <b>Heightオフセットマップマルチプライア</b> <i>0.0 - 1.0</i> | モディファイヤは、オフセットマップの影響を設定します。 |
| <b>Heightスケール</b> <i>0.0 - 1.0</i> | すべてのタイルをHeight範囲に均等に拡大/縮小するモディファイヤ。 オフセットの反対に、コントラストのように値が離れます。 |
| <b>Heightスケールのランダム</b> <i>0.0 - 1.0</i> | タイルごとにHeightスケールをランダムに変化させます。 |
| <b>Heightスケールマップマルチプライヤ</b> <i>0.0 - 1.0</i> | [修正]を使用して、スケールマップの影響を設定します。 |
| <b>背景に合わせる</b> <i>0.0 - 1.0</i> | タイルと背景のブレンドに影響します。 最適化を行わない場合は、背の形状に従ってマップが固定され、最適化が行われます。 たとえば、葉と棒に適しています。 |
| <b>最適化された滑らかな背景</b> <i>0.0 - 2.0</i> | 前のエフェクトのスムージング値。不正確なまたは極端な変動を防ぎます。 |
| <b>Bg 勾配からの歪み</b> <i>0.0 - 1.0</i> | 調整/勾配タイルHeightは、背景勾配によって駆動（通常の計算値）。 |
| <b>バックグラウンド勾配 Smoothness</b> <i>0.0 - 2.0</i> | 前のエフェクトのスムージング値。不正確なまたは極端な変動を防ぎます。 |
| <b>黒ピクセルのカットアウト</b> <i>False/True</i> | タイルのベースシェイプのブラック(0)ピクセルを無視するように切り替えます。 |
| <b>パターンベースをフラット化</b> <i>False/True</i> | 背景を使用してタイルのブレンド動作を調整します。タイルは、背景と交差(False)するか、低い位置にあるときに背景をオーバーライドします。 |
| <b>マスク</b> |  |
| <b>ランダムなマスク</b> <i>0.0 - 1.0</i> | タイルをランダムに非表示にします。 この値が高いほど、タイルがより多く消えます。 |
| <b>マスクランダムマップマルチプライヤ</b> <i>0.0 - 1.0</i> | タイルの非表示を開始するタイミングをマスクマップのトレッシュホールドします。 |
| <b>Bg 勾配からのマスク</b> <i>-1.0 - 1.0</i> | 背景マップ勾配（計算済みの法線）を使用してタイルを非表示にします。 |
