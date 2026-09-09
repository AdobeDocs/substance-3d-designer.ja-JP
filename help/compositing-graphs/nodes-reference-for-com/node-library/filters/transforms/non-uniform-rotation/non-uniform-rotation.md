---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/transforms/non-uniform-rotation.html"
breadcrumb-title: ''
description: 非均一回転ノードを使用して、非均一回転変換を適用し、らせん効果および渦効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Transforms > Non-Uniform Rotation
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 不均等な回転
user-guide-description: ''
user-guide-title: ''
source-git-commit: caf740432682ed82eb55ad2f84bc9dd6ed15ad14
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 1%

---


# 不均等な回転

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/nonuniformrotationgrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](non-uniform-rotation.resources/nonuniformrotationcolor.png){width="200px"}

</td>
</tr>
</table>

<b>イン：</b>フィルター/変形

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**Non-Uniform Rotation**&#x200B;ノードは、**回転マップ**&#x200B;入力を使用して&#x200B;**入力**&#x200B;を回転します。

画像の値は、*ターン数*&#x200B;を表します。 **ピボットの位置**&#x200B;の値または&#x200B;**ピボットの位置マップ**&#x200B;の入力で指定された場所を基準にして回転が行われます。\
**回転マップ**&#x200B;の正の値を入力すると、*時計回り*&#x200B;に回転します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>入力</b> <i>グレースケール/カラー</i> | 回転する入力グレースケールイメージ。 |
| <b>回転マップ</b> <i>グレースケール</i> | 回転量の制御に使用するマップです。*ターン数*&#x200B;単位です。 サンプリングされた値は、**回転角度乗数**&#x200B;に対して乗算されます。 負の値を指定すると、*反時計回り*&#x200B;に回転します。 |
| <b>回転ピボットの位置マップ</b> <i>色</i> | 回転&#x200B;*ピボット*&#x200B;の位置を指定するために使用される画像です。 **X/Y**&#x200B;位置は、画像の&#x200B;**R/G**&#x200B;チャネルにマップされます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>回転角度乗数</b> <i>フロート</i> | **回転マップ**&#x200B;入力の強さを調整します。 |
| <b>回転角度のオフセット</b> <i>フロート</i> | 指定した追加回転量を適用します。 |
| <b>ピボットの位置マップを使用する</b> <i>ブール値</i> | *ビットマップ入力*&#x200B;を使用して、回転ピボットの位置を指定します。 **X/Y**&#x200B;位置は、**位置マップ**&#x200B;入力の&#x200B;**R/G**&#x200B;チャネルにマップされます。 |
| <b>ピボットの位置</b> <i>浮動小数点2</i> | 画像を回転するピボットの位置。 |
| <b>背景色</b> <i>フロート/フロート4</i> | タイリングが&#x200B;**高さと高さのタイリング**&#x200B;に設定されていない場合に、画像の境界の&#x200B;*外側*&#x200B;に表示される背景色です。 |
| <b>フィルターモード</b> <i>整数</i> | ピクセル間の&#x200B;*補間*&#x200B;が<br><br>- *最も近い*：で&#x200B;*同じ*&#x200B;値（高速）<br>- *バイリニア*：でバイリニアのフィルターが適用され、*より滑らかな*&#x200B;外観になるときに、サンプリングされた結果を処理する方法を定義します |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-demo-02-resized.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-variant-png.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="non-uniform-rotation.resources/nonuniformrotation-node.png" />
        </td>
    </tr>
</table>
