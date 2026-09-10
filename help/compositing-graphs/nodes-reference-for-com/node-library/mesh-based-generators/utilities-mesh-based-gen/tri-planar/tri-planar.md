---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/utilities-mesh-based-generators/tri-planar.html"
breadcrumb-title: ''
description: Tri Planarノードを使用して3つの直交平面からテクスチャを投影し、複雑なジオメトリ上でシームレスなテクスチャマッピングを行います。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Utilities (Mesh Based Generators) > Tri Planar
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3平面
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1ea5f4e048a3b4591bf71d9b18707837dac1bf6f
workflow-type: tm+mt
source-wordcount: '443'
ht-degree: 6%

---


# 3平面

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](tri-planar.resources/triplanar-1.png){width="128px"}

![](tri-planar.resources/triplanar-grayscale.png){width="128px"}

<b>In:</b> メッシュベースのジェネレータ>ユーティリティ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

この高度なノードは、ベイク処理された位置とワールド空間の法線データに基づいて、2Dの三平面投影マッピングを実行します。 つまり、UV座標は本質的に完全にメッシュ自体に基づく（ほとんど）シームのないマッピングに変換されます。

これは、毎回再焼き付けすることなく、継ぎ目を避けるための良い方法です（パン屋と同じようなことが可能です）。 欠点は、このノードが非常に重いため、高速ではないということです。

あなたのパンは高精度である必要があることに注意してください： 8ビットのパンは非常に良い結果をもたらさないでしょう。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>位置</b> <i>カラー入力</i> | ベイク処理された位置マップ。 16ビット以上の精度が理想的です。 |
| <b>ワールド空間標準</b> <i>カラー入力</i> | ベイク処理されたワールド空間の法線マップ、理想的には16ビット以上の精度。 |
| <b>入力X</b> <i>カラー入力（グレースケール入力）</i> | トライプラナー投影を介してUVからワールド空間に再マップする入力マップ。 画像入力が1に設定されている場合はすべての軸で使用され、3に設定されている場合はX軸で使用されます。 |
| <b>入力Y</b> <i>カラー入力（グレースケール入力）</i> | イメージ入力が3に設定されている場合のみ。 Y軸上のUVからワールド空間に再マップする入力マップ。 |
| <b>入力Z</b> <i>カラー入力（グレースケール入力）</i> | イメージ入力が3に設定されている場合のみ。 Z軸上のUVからワールド空間に再マップする入力マップ。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>プロジェクション</b> <i>すべての軸、Xのみ、Yのみ、Zのみ</i> | ブレンドする軸を設定します。 |
| <b>画像入力</b> <i>1入力、3入力</i> | すべての軸に1つのマップを使用するか、軸ごとに特定のマップを使用するかを設定します。 |
| <b>描画モード</b> <i>リニア、アドバンスト</i> | 精度と精度が向上します。 |
| <b>コントラストのブレンド</b> <i>0.001 - 1.0</i> | トランジションのコントラスト。滑らかなトランジションと粗いトランジションをブレンドします。 |
| <b>正規化係数</b> <i>0.0 - 1.0</i> | ブレンド領域のコントラストの損失を復元することで、プロジェクションブレンドを改善します。 |
| <b>タイリング</b> <i>0.0 - 10.0</i> | 入力テクスチャを並べて表示する回数。 |
| <b>グローバルローテーション</b> <i>0.0 - 1.0</i> | すべての軸に対するグローバル回転。 |
| <b>ミラー化された投影を修正する</b> <i>False/True</i> | ミラー化された投影の処理方法を設定します。 |
| <b>回転X</b> <i>0.0 - 1.0</i> | 投影のX軸に対する個々の回転。 |
| <b>回転Y</b> <i>0.0 - 1.0</i> | 投影のY軸に対する個々の回転。 |
| <b>回転Z</b> <i>0.0 - 1.0</i> | 投影のZ軸に対する個々の回転。 |
| <b>オフセットX</b> <i>0.0 - 1.0</i> | 投影のX軸にオフセット |
| <b>ランダムオフセットX</b> <i>0.0 - 1.0</i> | X軸オフセットのランダム化を可能にします。 |
| <b>オフセットY</b> <i>0.0 - 1.0</i> | 投影のY軸にオフセット |
| <b>ランダムオフセットY</b> <i>0.0 - 1.0</i> | Y軸オフセットのランダム化を可能にします。 |
| <b>オフセットZ</b> <i>0.0 - 1.0</i> | 投影のZ軸にオフセット |
| <b>ランダムオフセットZ</b> <i>0.0 - 1.0</i> | Z軸オフセットのランダム化を可能にします。 |
