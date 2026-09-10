---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear.html"
breadcrumb-title: ''
description: '[ファイバーグラス]Edge Wearノードを使用して、メッシュの曲率に基づいてファイバーグラスのエッジに摩耗マスクを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Fiber Glass Edge Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 繊維ガラスEdge Wear
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 6%

---


# 繊維ガラスEdge Wear

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](fiber-glass-edge-wear.resources/fiber-glass-edge-wear.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

グラスファイバーのタイプの摩耗を特に意図したマスクを表し、おそらく布に使用することができます。 繊維はタイル状で繰り返し使用されるため、必要に応じてトリプレーナ混合を有効にすることができます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | エッジのハイライトに使用するベイク済みマップ。 必須！ |
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 閉塞領域のマスクに使用するベイク済みマップ。 必須ではありませんが、間違いなくお勧めします。 |
| <b>経年劣化入力</b> <i>グレースケール入力</i> | ファイバパターンをオーバーライドするオプションのカスタムスロット。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |
| <b>ワールド空間標準</b> <i>カラー入力</i> | Triplanarにのみ使用されます。 |
| <b>位置</b> <i>カラー入力</i> | Triplanarにのみ使用されます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>摩耗レベル</b> <i>0.0 - 1.0</i> | [ヒストグラムスキャン](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/histogram-scan/histogram-scan.md)のように、徐々に磨耗を明らかにします。 |
| <b>コントラストをつける</b> <i>0.0 - 1.0</i> | エフェクト全体のコントラストを設定します。 |
| <b>エッジのSmoothness</b> <i>0.0 - 16.0</i> | ハイライトされたエッジから裁ち落としとブラーを設定します。 |
| <b>経年劣化量</b> <i>0.0 - 1.0</i> | エッジ間でブレンドするファイバーエフェクトの量を設定します。 これをWear Levelと一緒に調整して、最大限に制御します。 |
| <b>Ambient occlusionマスク</b> <i>0.0 - 1.0</i> | AOがエフェクトを非表示にどれだけ影響するかを設定します。 |
| <b>曲率の太さ</b> <i>0.0 - 1.0</i> | 曲率からの凸状エッジの影響量を設定します。 |
| <b>カスタム経年劣化を使用する</b> <i>False/True</i> | 組み込みファイバーをカスタムマップで上書きします。 |
| <b>三平面を使用</b> <i>False/True</i> | [トリ平面](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/utilities-mesh-based-gen/tri-planar/tri-planar.md)を有効にしてシームを非表示にします。 |
| <b>3平面のブレンドコントラスト</b> <i>0.0 - 1.0</i> | トリプラナーエフェクトのコントラストをコントロールします。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="fiber-glass-edge-wear.resources/fiber-glass-edge-wear-ex.gif" />
        </td>
    </tr>
</table>
