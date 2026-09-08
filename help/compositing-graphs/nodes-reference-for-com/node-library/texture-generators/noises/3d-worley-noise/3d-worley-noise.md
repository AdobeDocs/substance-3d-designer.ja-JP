---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/3d-worley-noise.html"
breadcrumb-title: ''
description: 3D Worley Noiseノードを使用して、3D位置に基づいてWorleyノイズを生成し、ボリュームテクスチャエフェクトを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > 3D Worley Noise
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dワーリーノイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 1f6cd80beb50560ef8711ff67335b0bb54df04ca
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 7%

---


# 3Dワーリーノイズ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/3d-worley.png){width="128px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ライブラリで最も汎用性が高く高度なノイズの1つで、入力ポジションマップに基づいて3D空間でワーリーノイズを生成します。 標準的な[セル](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/cells-1/cells-1.md)や[遠距離](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)ベースのノイズよりもはるかに強力な機能を備えた多くのオプションがあります。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>スケール</b> <i>1 - 64</i> | エフェクトのグローバルスケールを設定します。 |
| <b>サイズ</b> <i>0.0 - 1.0</i> | X、Y、Z軸に対して個別に不均等スケーリングを実行します。 |
| <b>モード</b> <i>ユークリッド、マンハッタン、チェビシェフ、ミンコフスキー</i> | 距離メトリックを変更します。 非常に異なる種類のノイズを使用できます。 |
| <b>ミンコフスキー数</b> <i>0.0 - 20.0</i> | Minkowski距離指標でのみ使用できます。 異なる種類のメトリクスをブレンドします。 |
| <b>スタイル</b> <i>F1, F2, F2-F1，境界線，ランダムカラー</i> | メートル法の組み合わせ計算を設定します。 さらに多くの組み合わせを使用できます。 |
| <b>境界線の幅</b> <i>0.0 - 1.0</i> | 境界線の組み合わせ数式がアクティブである場合、境界線の幅を制御します。 |
| <b>丸み</b> <i>0.0 - 1.0</i> | F1、F2、F2-F1モードでのみ使用できます。 レベルの中間位置を設定します。 |
| <b>反転</b> <i>False/True</i> | 結果を反転します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex04.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex03.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex02.png" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/3d-worley-ex01.png" />
        </td>
    </tr>
</table>
