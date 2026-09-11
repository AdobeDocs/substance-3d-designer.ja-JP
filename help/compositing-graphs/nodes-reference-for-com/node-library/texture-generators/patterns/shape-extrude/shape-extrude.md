---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/shape-extrude.html"
breadcrumb-title: ''
description: シェイプの押し出しノードを使用してシェイプを押し出し、テクスチャで3Dのような深度効果を生み出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > Shape Extrude
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェイプの押し出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: dbfe5b7ce453a6178d8d970698d3a5f8225151b4
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 5%

---


# シェイプの押し出し

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](shape-extrude.resources/shape-extrude.png){width="128px"}

<b>イン：</b> テクスチャジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

2Dのバイナリ「シェイプ」入力を3D回転のハイトマップにレンダリングできる高度なノード。 3Dパッケージでシェイプをその軸に沿って押し出し、ボリュームを作成する場合と同様に機能します。 プロファイルグラデーションマスクと組み合わせて、回転/レイズタイプのボディも作成できます。 ハイトマップの複雑な人為的シェイプを作成する場合に非常に便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>押し出しシェイプの入力</b> <i>グレースケール入力</i> | 「シェイプを押し出し」を「カスタム」に設定した場合は、ここで独自（できれば）のバイナリシェイプマスクをプラグインします。 |
| <b>プロファイルグラデーション</b> <i>グレースケール入力</i> | [プロファイルの種類]が[垂直グラデーション]に設定されている場合は、回転ボディの軸に沿ったシェイプの尺度を定義するために使用できます。 |
| <b>プロファイルマスク</b> <i>グレースケール入力</i> | 軸に沿って押し出しシェイプを非表示にしたり表示したりするために使用するマスクスロット。 軸に沿ってシェイプの連続性を解除するために使用できます。 バイナリとしてのみ解釈されます：グレースケールのput値は0または1に丸められます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>押し出しHeight</b> <i>0.0 - 1.0</i> | シェイプを中心から上に押し出す量。 |
| <b>押し出し深度</b> <i>0.0 - 1.0</i> | 中心から下向きにシェイプを押し出す量。 |
| <b>シェイプを押し出し</b> <i>立方体、円柱、カスタム入力</i> | 組み込みのシェイプを使用するか、独自のカスタムシェイプを外部に入力します。 |
| <b>押し出しシェイプサイズ</b> <i>0.0 - 1.0</i> | 組み込み立方体と円柱でのみ使用され、基本シェイプのサイズを決定し、不均等にスケーリングできます。 |
| <b>スケール</b> <i>0.0 - 1.0</i> | エフェクトのグローバルスケールを設定します。 組み込みシェイプでは、均一な基本シェイプのスケールになり、Heightや深度には影響しません。<br><br>カスタム入力では、最終結果全体が均一にスケールされます。 |
| <b>プロファイルの種類</b> <i>直線、垂直グラデーション、マスク</i> | エフェクトのビヘイビアーを指定するメインコントロールと、オプションの追加入力マップの使用。<br><br>直線は標準の押し出し動作です。垂直グラデーションを使用すると、軸全体に沿ってカスタムのスケール値を設定できます。マスクを使用すると、マスクごとに軸に沿ってセクションを非表示にできます。 |
| <b>ベベルHeight</b> <i>0.0 - 1.0</i> | 押し出し軸に沿ってベベルが到達する距離を設定します。 |
| <b>ベベルの強さ</b> <i>0.0 - 1.0</i> | ベベルが元のシェイプからどれくらいリトラクトするかを設定します。 |
| <b>ベベル曲線</b> <i>-1.0 - 1.0</i> | ベベル効果の凸曲線または凹曲線を設定します。 値を0に設定すると、直線になり、曲線はなくなります。 |
| <b>ベベルをミラー</b> <i>False/True</i> | 切り替えて、シェイプの上と下にベベルを適用します。 |
| <b>マルチプライアをダウングレード</b> <i>0 - 2</i> | ダウンスケーリングを簡単に制御できます。 これを使用すると、アンチエイリアスをすばやく追加できます。ノードの解像度も上げることを確認してください。 |
| <b>位置</b> | 3D空間で結果を回転するためのメインコントロール。 2D ビュー内のインタラクティブギズモと相関します。 |
| <b>出力範囲</b> <i>[0, 1], [-1, 1]</i> | 出力の最小値と最大値を設定します。 rangeが[-1,1]に設定されている場合、負の値は黒で表示されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="shape-extrude.resources/shape-extrude-1.png" />
        </td>
    </tr>
</table>
