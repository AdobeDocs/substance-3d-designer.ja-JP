---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/texture-generators/patterns/3d-volume-mask.html"
breadcrumb-title: ''
description: 3Dボリュームマスクノードを使用して、3Dポジションに基づくボリュームマスクを作成し、高度なマテリアルエフェクトを実現します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Texture Generators > Patterns > 3D Volume Mask
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dボリュームマスク
user-guide-description: ''
user-guide-title: ''
source-git-commit: db5ad9a6ad1d03fedcc3d760cc8886501d16b87f
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 1%

---


# 3Dボリュームマスク

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](3d-volume-mask.resources/3dvolumemask.png){width="256px"}

<b>イン：</b>ジェネレーター>パターン

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

**3Dボリュームマスク**&#x200B;ノードは、**位置** 入力マップに基づいて&#x200B;*プリミティブシェイプ*&#x200B;の表現を生成します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>位置</b> <i>色</i> | プリミティブを表す&#x200B;*3D空間座標*&#x200B;を表すマップ。<br><br>**X/Y/Z**&#x200B;座標は、それぞれ&#x200B;**R/G/B**&#x200B;チャンネルにマップされます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>図形</b> <i>整数</i> | 表現する必要があるプリミティブ図形： <br><br>- *立方体*<br>- *円柱*<br>- *球* |
| <b>スケール</b> <i>フロート</i> | プリミティブの&#x200B;*グローバル*&#x200B;尺度を定義します。すべての軸に&#x200B;*均一*&#x200B;に適用されます。 |
| <b>サイズ</b> <i>浮動小数点3</i> | 各軸のシェイプのサイズを指定します。 |
| <b>位置の入力</b> <i>整数</i> | *Position **入力を使用してスペース*を表現する**&#x200B;メソッド： <br><br>- *UV位置*: *UVマップ*&#x200B;を使用します。 X/Y(U/V)座標は、それぞれR/Gチャンネルにマッピングされる。 Z軸は&#x200B;*直交前方*&#x200B;ベクトルと想定されます。<br>- *ワールド空間位置*: *位置マップ*&#x200B;を使用して、プリミティブを3D空間にマップします。 X/Y/Z座標は、それぞれR/G/Bチャンネルにマップされます。 |
| <b>位置UV</b> <i>浮動小数点2</i> | UV空間のプリミティブの位置です。<br><br>*注意*：このパラメーターは、**Position Input**&#x200B;パラメーターが&#x200B;*UV位置*&#x200B;に設定されている場合にのみ使用できます。 |
| <b>位置</b> <i>浮動小数点3</i> | ワールド空間のプリミティブの位置です。<br><br>*注意*：このパラメーターは、**Position Input**&#x200B;パラメーターが&#x200B;*ワールド空間の位置*&#x200B;に設定されている場合にのみ使用できます。 |
| <b>回転</b> <i>浮動小数点3</i> | ワールド空間でのシェイプの回転を定義します。 |
| <b>ぼかしの幅</b> <i>フロート</i> | プリミティブのサーフェスから内側に&#x200B;*フェードするグラデーション*&#x200B;の幅を調整します。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant3.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="3d-volume-mask.resources/3dvolumemask-variant4.jpg" />
        </td>
    </tr>
</table>
