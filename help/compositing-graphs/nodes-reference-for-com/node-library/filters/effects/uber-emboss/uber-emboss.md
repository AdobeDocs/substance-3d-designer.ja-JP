---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/uber-emboss.html"
breadcrumb-title: ''
description: Uber Embossノードを使用すると、カスタマイズ可能な深度、角度、照明のコントロールを使用して高度なエンボス効果を作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Uber Emboss
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Uber Emboss
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 9%

---


# Uber Emboss

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/uber-emboss.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[エンボス](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/emboss/emboss.md)の機能豊富な高度なバージョンです。 ハイトマップに基づいて精巧な2Dのフェイクライティングエフェクトを実行します。

多くの制御が必要な場合に、特定のテクスチャリングスタイル用にベイクイン照明を作成するときに便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>色</b> <i>カラー入力</i> | 変更するベースイメージ。 |
| <b>Height</b> <i>グレースケール入力</i> | エフェクトのドライバーとして使用されるHeightmap。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>周囲光の色</b> <i>（カラー値）</i> | 影の領域で使用するカラー。 |
| <b>Diffuseの色</b> <i>（カラー値）</i> | 明るい領域で使用するカラー。 |
| <b>Specularの色</b> <i>（カラー値）</i> | Specularの反射に使用される色 |
| <b>光の強さ</b> <i>0.0 - 1.0</i> | （偽装された）ライトの強度。 |
| <b>光源の角度</b> <i>0.0 - 1.0</i> | （偽）光の入射角 |
| <b>Specularの適用度</b> <i>0.0 - 1.0</i> | Specular反射の強さ。 |
| <b>光沢度</b> <i>0.0 - 1.0</i> | Specularハイライトのサイズ。 |
| <b>ラフネス</b> <i>0.0 - 1.0</i> | 拡散反射光ライトの計算に使用されるラフネス。 |
| <b>シャドウの不透明度</b> <i>0.0 - 1.0</i> | シャドウが適用された領域のブレンド不透明度。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/uberemboss-ex.png" />
        </td>
    </tr>
</table>
