---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/metal-edge-wear.html"
breadcrumb-title: ''
description: メタルEdge Wearノードを使用して、メッシュの曲率と位置に基づいてメタルエッジに摩耗マスクを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Metal Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 金属Edge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 7%

---


# 金属Edge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](metal-edge-wear.resources/metal-edge-wear.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、金属物体のエッジの摩耗を表現し、凸状の隆起エッジにスクラッチや切り屑が現れ、ベイクしたAO暗部によってマスクされる可能性があります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 |
| <b>経年劣化入力</b> <i>グレースケール入力</i> |  |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>ワールド空間標準</b> <i>カラー入力</i> |  |
| <b>位置</b> <i>カラー入力</i> |  |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>摩耗レベル</b> <i>0.0 - 1.0</i> | 徐々に明らかに摩耗の総量を設定します。 |
| <b>コントラストをつける</b> <i>0.0 - 1.0</i> | 最終結果のコントラストを設定します。 |
| <b>エッジのSmoothness</b> <i>0.0 - 16.0</i> | 曲率からのエッジからのフォールオフのSmoothnessを設定します。 |
| <b>経年劣化量</b> <i>0.0 - 1.0</i> | エッジ間でブレンドする経年劣化量を設定します。 |
| <b>経年劣化スケール</b> <i>1 - 16</i> | 経年劣化のスケールを設定します。 |
| <b>Ambient occlusionマスク</b> <i>0.0 - 1.0</i> | 最終的な効果（マスクされた暗い領域）に対するAOの効果の量を設定します。 |
| <b>曲率の太さ</b> <i>0.0 - 1.0</i> | 曲率の凸状のエッジが最終効果に与える効果の量を設定します。 |
| <b>カスタム経年劣化を使用する</b> <i>False/True</i> | カスタム経年劣化マップ入力スロットを有効にします。 |
| <b>三平面を使用</b> <i>False/True</i> | [平面のトリ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md) 投影を有効にして、シームを非表示にします。 |
| <b>3平面のブレンドコントラスト</b> <i>0.0 - 1.0</i> | トライプラナー投影の描画コントラストを設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="metal-edge-wear.resources/metal-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
