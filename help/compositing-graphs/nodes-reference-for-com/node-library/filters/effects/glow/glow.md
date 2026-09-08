---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/glow.html"
breadcrumb-title: ''
description: 「光彩」ノードを使用して、テクスチャに光彩効果を加え、明るさとemissiveマテリアルのアピアランスを作り出します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Glow
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 光彩
user-guide-description: ''
user-guide-title: ''
source-git-commit: a4ccdbff5343e3ece0312bd9b3318fb236f07308
workflow-type: tm+mt
source-wordcount: '178'
ht-degree: 5%

---


# 光彩

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/glow-greyscale.png){width="128px"}

![](../../../../../../assets/glow-3.png){width="128px"}

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

他の一般的な画像編集ソフトウェアに見られるように、「光彩（外側）」タイプの効果を実行します。 基本的に、入力の周りにフェードグラデーションのアウトラインを追加します。

この機能は、アルファチャンネルを含む画像に対しては適用されません。 カラー版でも、入力としてバイナリ、黒、白のマスクのみを必要とします。色付きの光彩を使用することのみが可能です。 透明度のある画像で動作するバージョンを使用している場合は、[シェイプグロー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/shape-glow/shape-glow.md)を参照してください。

重要：入力に適したバージョンを使用してください。 カラー入力には「グロー」を、グレースケール入力には「グローのグレースケール」を使用します。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>光彩の量</b> <i>0.0 - 1.0</i> | グロー効果の不透明度を指定します。 |
| <b>金額のクリア</b> <i>0.0 - 1.0</i> | 光彩効果をカットするタイミングを指定します。 半透明領域に便利です。 |
| <b>光彩サイズ</b> <i>0.0 - 20.0</i> | グロー効果の範囲を指定します。 |
| <b>光彩の色</b> <i>（カラー値） （カラーバージョンのみ）</i> | 光彩効果のカラーを設定します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="../../../../../../assets/glow-ex.png" />
        </td>
    </tr>
</table>
