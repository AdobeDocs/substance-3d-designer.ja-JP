---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/bottom-to-top.html"
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
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 1%

---


# 下から上

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/bottom-to-top.png){width="128px"}

## 下から上

**イン：** *メッシュベースのジェネレーター/マスクジェネレーター*

**単純**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/home)の[スマートマスク](https://experienceleague.adobe.com/en/docs/substance-3d-painter/using/features/smart-materials-and-masks)に似ています。

これにより、モデルの下部から上部に白から黒へのトランジションが生成され、ジオメトリベースのフォールオフや選択を行う場合に便利です。

## パラメーター

### 入力

* **位置**: *カラー入力*\
  ベイク処理された位置マップ。 必須！
* **粗さ：** *グレースケール入力*\
  これはPBRの粗さとは関係ありませんが、トランジションを分割するための（オプションの）バリエーションマップです。 粗さが0より大きい値に設定されている場合にのみ表示されます。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  明るさの調整のように、結果の平均レベルを黒または白の間でシフトします。
* **コントラスト**: *0.0 ～ 1.0*\
  トランジションのコントラストを調整します。
* **粗さ\_バリエーション**: *0.0 ～ 1.0*&#x200B;変動に対してブレンドする粗さマップの量を決定します。 これを0より大きくすると、マップスロットが表示されます。

## サンプル画像

![](../../../../../../assets/bottom-to-top-ex.gif)

</td>
</tr>
</table>
