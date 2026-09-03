---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/diffusion-uv.html"
breadcrumb-title: ''
description: 拡散UVノードを使用してUV空間に拡散エフェクトを適用し、カラーの変化を滑らかにしてブレンドを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Diffusion UV
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 拡散UV
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 2%

---


# 拡散UV

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](diffusion-uv.resources/diffusion-uv-01.png){width="200px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

指定された&#x200B;**マスク**&#x200B;画像入力に従って&#x200B;**ソース**&#x200B;画像入力のUV座標に誤差拡散処理を適用し、**ソース**&#x200B;からの値の間の座標を補間します。

マスクに一致するピクセルのUVだけが拡散され、他のピクセルは拡散されません。

タイリングは特別な方法で処理されます：タイリングが&#x200B;*有効* （デフォルトでは有効）の場合、隣接する座標は0/1の制限を超えて平均することができます。

たとえば、あるピクセルでU座標値が0.1、別のピクセルで0.8の場合、座標の&#x200B;*タイリング*&#x200B;と仮定されるため、平均値は0.45ではなく0.95になります。 これは、実際のピクセル位置とは関係ありません。座標値は、画像全体で同じように処理されます。

このフィルターを&#x200B;*テクスチャ変形*&#x200B;に使用すると、望ましくない結果が生じる可能性があります。 その場合は、マスクで「コントロールカーブ/ポイント」が&#x200B;*テクスチャの長さの半分*&#x200B;以内に定義されていることを確認してください。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>ソース</b> <i>色</i> | 拡散するUV。 このフィルターでは、タイル表示が特別な方法で処理されることに注意してください（<i>説明</i>を参照）。 |
| <b>マスク</b> <i>グレースケール</i> | 拡散マスク：白のピクセルが<i>ソース</i>でサンプリングされ、黒のピクセルで拡散されます。 画像は白黒である必要があります。 マスクにグラデーションが含まれている場合、カットオフ値は0.5です。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>反復回数</b> <i>0.0 - 64.0</i> | 実行する反復の数（大きい方が望ましいが遅い）。 有効な値は[8, 48]の範囲です。<br>数学的に正しい値を求めない場合は、小さい値でも問題ありません。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-03.jpg" />
        </td>
    </tr>
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-04.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="diffusion-uv.resources/diffusion-uv-05.jpg" />
        </td>
    </tr>
</table>
