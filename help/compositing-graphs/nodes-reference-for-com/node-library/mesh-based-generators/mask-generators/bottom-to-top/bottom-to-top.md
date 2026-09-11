---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
breadcrumb-title: ''
description: 下から上ノードを使用して、メッシュのワールド位置に基づいて下から上にグラデーションマスクを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Bottom To Top
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 下から上
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '199'
ht-degree: 5%

---


# 下から上

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](bottom-to-top.resources/bottom-to-top.png){width="128px"}

<b>In:</b> メッシュベースのジェネレーター> マスクジェネレーター

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/home)の[スマートマスク](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/features/smart-materials-and-masks)に似ています。

これにより、モデルの下部から上部に白から黒へのトランジションが生成され、ジオメトリベースのフォールオフや選択を行う場合に便利です。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>位置</b> <i>カラー入力</i> | ベイク処理された位置マップ。 必須！ |
| <b>粗さ</b> <i>グレースケール入力</i> | これはPBRの粗さとは関係ありませんが、トランジションを分割するための（オプションの）バリエーションマップです。 粗さが0より大きい値に設定されている場合にのみ表示されます。 |
| <b>マスク（オプション）</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>レベル</b> <i>0.0 - 1.0</i> | 明るさの調整のように、結果の平均レベルを黒または白の間でシフトします。 |
| <b>コントラスト</b> <i>0.0 - 1.0</i> | トランジションのコントラストを調整します。 |
| <b>ラフネス_バリエーション</b> <i>0.0 - 1.0</i> | 変動のためにブレンドするラフネスマップの量を指定します。 これを0より大きくすると、マップスロットが表示されます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="bottom-to-top.resources/bottom-to-top-ex.gif" />
        </td>
    </tr>
</table>
