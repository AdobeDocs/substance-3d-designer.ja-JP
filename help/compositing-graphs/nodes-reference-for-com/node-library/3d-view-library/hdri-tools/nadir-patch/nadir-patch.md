---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/3d-view-library/hdri-tools/nadir-patch.html"
breadcrumb-title: ''
description: Nadir Patchノードを使用して、HDRIパノラマの最下部のアーティファクトを修正するために最下部の領域にパッチを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > 3D View (Library) > HDRI Tools > Nadir Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Nadir Patch
user-guide-description: ''
user-guide-title: ''
source-git-commit: 43dd5433948c89f68426040a2a2d76282072c75d
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 5%

---


# Nadir Patch

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/panorama-nadir-patch.png){width="200px"}

<b>内：</b> 3D ビュー > HDRI ツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、球状にマッピングされたイメージの中央のグラウンドポイント（床面）にパッチを適用する機能を提供します。 汚い床面や、目に見えるカメラや三脚を非表示または「クローン作成」するために使用できます。 [コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)のように機能しますが、球面にマップされた画像に調整を適用します。 画像内の別の場所でポイントを選択します。つまり、コピーして元のディレクトリでブレンドしたポイントです。 1つのHDRI以外に処理に他の外部入力は必要ありませんが、外部マスクをパッチエフェクトのアルファとして使用することができます。

[Nadir Extract](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/3d-view-library/hdri-tools/nadir-extract/nadir-extract.md)を使用すると、効果をすばやく確認して検証できます。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>カラー入力</i> |  |
| <b>マスク入力</b> <i>グレースケール入力</i> | パッチのマスクに使用するオプションのマスクスロット。 アルファのように機能します。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>有効にする</b> <i>False/True</i> | パッチ適用エフェクトを有効または無効にします。 |
| <b>ヘルパーを表示</b> <i>False/True</i> | デバッグ用にヘルパー行を表示または非表示にします。 |
| <b>Thickness</b> <i>0.0 - 1.0</i> | ヘルパー行のThickness。 |
| <b>パッチスケール</b> <i>0.0 - 1.0</i> | パッチのグローバルな均一スケール。 ソースとターゲットの両方に影響します。 |
| <b>パッチサイズ</b> <i>0.0 - 1.0</i> | パッチのサイズが均一ではありません。 |
| <b>パッチの回転</b> <i>0.0 - 1.0</i> | パッチの回転。 ソースとターゲットに影響します。 |
| <b>パッチAlpha</b> <i>正方形、ガウス、マスク入力</i> | パッチを背景とブレンドするときに使用するアルファを設定します。 |
| <b>パッチ硬さ</b> <i>0.0 - 1.0</i> | アルファの硬さ/コントラストを設定します。 |
| <b>ソースの回転オフセット</b> <i>0.0 - 1.0</i> | パッチのソースの回転のみ。 |
| <b>位置の座標</b> |  |
| <b>ソースの位置</b> | ソースの位置。 2Dビューにハンドルがあります。 |
| <b>パッチの位置</b> | ターゲットの位置。 2Dビューにハンドルがあります。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/nadir-patch-ex.gif" />
        </td>
    </tr>
</table>
