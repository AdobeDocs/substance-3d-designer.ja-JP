---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/multi-directional-warp.html"
breadcrumb-title: ''
description: 多方向ワープノードを使用して、ワープエフェクトを複数の方向に適用し、複雑なゆがみパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Multi Directional Warp
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 多方向ワープ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2ea5b90ca7a4cbcd0b0049b156e8ded334aa0ceb
workflow-type: tm+mt
source-wordcount: '297'
ht-degree: 3%

---


# 多方向ワープ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-directional-warp.resources/multi-directional-warp-color.png)![](multi-directional-warp.resources/multi-directional-warp-grayscalepng.png)

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

多方向ワープは、置き換えられたテクスチャはそのままで、[方向ワープ](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/directional-warp/directional-warp.md)を反対方向に複数回適用します。 これは、複数の方向にプッシュできる点で標準の方向ワープとは異なりますが、アトミックバージョンでは1つしかプッシュできません。 このようにして、従来の問題である、方向ワープが画像を単一の方向に押し出しすぎるのが常のようで、単一の方向ではなく複数の方向または軸に沿って動作するという問題を解決します。

これは主に[Non Uniform Directional Warp](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/non-uniform-directional/non-uniform-directional-warp.md)とは異なり、少し制限が加えられています。ワープの方向はパラメーターによってのみ制御され、入力マップでは設定できません。 利点は、少し使いやすく、用途に応じてより正確になることです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール/カラー入力</i> | ワープが適用されるベースマップ。 カラーまたはグレースケールを指定できます。 |
| <b>強度入力</b> <i>グレースケール入力</i> | ワープ効果の強度を制御する必須のマスクマップは、グレースケールにする必要があります。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>適用度</b> <i>0.0 - 20.0</i> | ワープ効果の強度を設定します。ピクセルを押し出す範囲を指定します。 |
| <b>ワープ角度</b> <i>0.0 - 1.0</i> | ワープ効果を適用する角度または方向を設定します。 |
| <b>モード</b> <i>平均、最大、最小、チェーン</i> | 連続パスの描画モードを設定します。 方向が2または4の場合にのみ効果があります。 |
| <b>道順</b> <i>1, 2, 4</i> | ワープが機能する軸の数を設定します。 1は角度の方向に移動することを意味し、2は角度の軸、垂直軸の順に移動することを意味し、4は前の軸、および45度の傾斜を意味します。 |
