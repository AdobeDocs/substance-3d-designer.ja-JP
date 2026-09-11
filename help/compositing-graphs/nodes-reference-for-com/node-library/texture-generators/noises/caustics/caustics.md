---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/noises/caustics.html"
breadcrumb-title: ''
description: コースティクスノードを使用して、水中および屈折ライティングエフェクトを作成するためのコースティクスライトパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Noises > Caustics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: コースティクス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 77626800e9c3434a519ca045aad1e185d9dc1476
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 5%

---


# コースティクス

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](caustics.resources/rt-caustics-grayscale.png){width="128px"}

<b>内：</b> テクスチャジェネレータ> ノイズ

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高さマップとライトの方向に基づいて投影されたコースティクスを生成します。グレースケールとカラーの両方のバージョンがありますが、違いは微妙ですが、カラーバージョンでは色分散効果が追加されます。 光は1つの点からキャストされ、環境マップは使用されません。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>出力カラースペース</b> <i>Raw, sRGB</i> | 出力カラースペースを設定します。 |
| <b>フォトングリッドサイズ</b> <i>自動、512、1024、2048、4096</i> | グリッドサイズを調整して画質を設定しますが、デフォルトでは一致する入力に設定されます。 計算の高速化に使用できます。 |
| <b>サーフェスHeightスケール</b> <i>0.0 - 1.0</i> | Heightの変換方法を指定する乗数。 |
| <b>サーフェスHeightの位置</b> <i>0.0 - 1.0</i> | 投影する屈折サーフェスの距離を設定します。 |
| <b>サーフェスIOR</b> <i>1.0 - 2.0</i> | 屈折率を設定します。カラーバージョンでは、これによりカラーの分散が大きくなります。 |
| <b>フォトンのサイズ</b> <i>1.0 - 50.0</i> | フォトンサイズは効果の鮮明さに影響します。 |
| <b>分散</b> <i>0.0 ～ 0.01 （カラーバージョンのみ）</i> | カラー分散のみに影響します。 IORが低い場合は表示されません。 |
| <b>ジッター</b> <i>0.0 - 1.0</i> | キャストフォトンのパーティクルに不規則なジッターを加えます。 |
| <b>明るい位置</b> | ライトの位置を移動します。 また、2D ビューのギズモを介して行われます。 |
| <b>背景色</b> <i>（カラー値） （カラーバージョンのみ）</i> | 背景色を変更します。 グレースケール版では黒に制限されます。 |
| <b>非正方形拡張</b> <i>False/True</i> | スカッシュとストレッチの非正方形の比率での補正を有効にします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="caustics.resources/rt-caustics-grayscale-1.png" />
        </td>
    </tr>
</table>
