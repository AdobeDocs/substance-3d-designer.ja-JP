---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Leaksノードを使用して、水の汚れや流体エフェクトを作成するためのメッシュジオメトリに基づいてリークパターンを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: リーク
user-guide-description: ''
user-guide-title: ''
source-git-commit: 78cf3f307bd33c6d8b399043ff1c5e5d1764b606
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 3%

---


# リーク

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](leaks.resources/leaks.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて、黒と白のマスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)と同様。

この結節は、鋭利な縁からDirtと灰汁が漏れ出た縞状に見える。 ベイクされた位置で筋が生成されるため、常に下に向かって走ります。

バリエーションマスクを変えてみてください。ストリークの配置を制御するため、他のマスクジェネレーターよりもはるかに大きな影響を与える可能性があります。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>位置</b> <i>グレースケール入力</i> | ストリーク方向に使用するベイク位置マップ。 必須！ |
| <b>曲率</b> <i>グレースケール入力</i> | 筋の留置にベイク済みマップを使用。 必須！ |
| <b>Ambient occlusion</b> <i>グレースケール入力</i> | 内部エフェクトおよびマスクに使用されるベイク済みマップ。 推奨されますが、代わりにフラットホワイトを使用することもできます。 |
| <b>通常のワールド空間</b> <i>カラー入力</i> | 筋の方向に使用するワールド空間法線マップ。 必須！ |
| <b>バリエーションマスク</b> <i>グレースケール入力</i> | オプションのバリエーションマスク。オーバーライドをTrueに設定して有効にします。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | 結果の合計レベル。 徐々に効果を明らかにして、長さに影響を与えます。 長い滴り落ちるようにかなり高く設定する必要があります。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | 結果のコントラストを調整します。 |
| <b>バリエーション</b> <i>0.0 - 1.0</i> | 縞のマスクに使用する大きな変化の量を設定します。 この値を0に設定すると、線が完全に均一になるので、これは避けてください。 |
| <b>長さ</b> <i>0.0 - 8.0</i> | 筋の長さが滴る。 小さなスケールでこの値を大きくしすぎると、目に見えるステッピングになります。 レベルも変えてみましょう。 |
| <b>隠す</b> <i>X、Y、Z、なし</i> | AOが作用する方向を設定します。 |
| <b>バリエーションマスクの上書き</b> <i>False/True</i> | カスタム入力スロットでバリエーションマスクを上書きできるようにします。 スパーサーマスクやデンサーマスクは、効果的な方法で効果を発揮し、しずくを抑えることができます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="leaks.resources/leaks-ex.gif" />
        </td>
    </tr>
</table>
