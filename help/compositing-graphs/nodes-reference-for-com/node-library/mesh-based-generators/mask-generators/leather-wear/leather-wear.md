---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leather-wear.html"
breadcrumb-title: ''
description: Leather Wearノードを使用して、メッシュの曲率と接点に基づいてレザーサーフェスに摩耗マスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leather Wear
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: レザーウェア
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 5%

---


# レザーウェア

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leather-wear.resources/leather-wear.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、レザーのパターンで磨耗を表現し、曲率に基づいてエッジの磨耗を増やします。 機能が[ファイバーグラスEdge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md)と似ており、パラメーターはほとんど同じです。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>曲線</b> <i>グレースケール入力</i> | エッジの配置に使用するベイク済みマップ。 必須！ |
| <b>環境オクルージョン</b> <i>グレースケール入力</i> | 特定の領域を閉塞するベイク済みマップを使用する。 推奨されますが、必須ではありません。 |
| <b>経年劣化入力</b> <i>グレースケール入力</i> | 「カスタム経年劣化を使用」パラメーターで切り替えることができる、オプションの経年劣化マップ入力スロット。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>摩耗レベル</b> <i>0.0 - 1.0</i> | グローバルな摩耗レベルを設定し、徐々に明らかにします。 |
| <b>コントラストをつける</b> <i>0.0 - 1.0</i> | 効果のコントラストを設定します。 |
| <b>経年劣化量</b> <i>0.0 - 1.0</i> | エッジ間でブレンドする経年劣化の量（既定のレザーパターン）を設定します。 |
| <b>Ambient occlusionマスク</b> <i>0.0 - 1.0</i> | AOマスクが摩耗効果を除去する範囲を設定します。 |
| <b>曲率の太さ</b> <i>0.0 - 1.0</i> | 曲率のエッジが最終結果に影響する範囲を設定します。 0に設定しても、曲率マップは必要です。 |
| <b>カスタム経年劣化を使用する</b> <i>False/True</i> | 組み込みの既定のレザーのパターンの上書きを有効にします。 代わりにカスタム入力スロットを使用してください。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leather-wear.resources/leather-wear-ex.gif" />
        </td>
    </tr>
</table>
