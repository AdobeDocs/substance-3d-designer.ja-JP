---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/mesh-based-generators/mask-generators/leaks.html"
breadcrumb-title: ''
description: Leaksノードを使用して、水の汚れや流体エフェクトを作成するためのメッシュジオメトリに基づいてリークパターンを生成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Mesh Based Generators > Mask Generators > Leaks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: リーク
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 1%

---


# リーク

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leaks.png){width="128px"}

## リーク

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

この結節は、鋭利な縁からDirtと灰汁が漏れ出た縞状に見える。 [位置]をベイク処理してストリークを生成すると、常に下方に走ります。

バリエーションマスクを必ず変更してください。ストリークの配置を制御するため、他のマスクジェネレーターよりもはるかに大きな影響を与える可能性があります。

## パラメーター

### 入力

* **位置**: *グレースケール入力*\
  ベイク処理された位置マップ。筋の方向に使用されます。 必須！
* **曲率**: *グレースケール入力*\
  筋の留置にベイク済みマップを使用。 必須！
* **環境オクルージョン**: *グレースケール入力*\
  内部エフェクトおよびマスクに使用されるベイク済みマップ。 推奨されますが、代わりにフラットホワイトを使用することもできます。
* **標準のワールドスペース**: *カラー入力*\
  ストリーク方向に使用する、ベイク処理されたワールド空間の法線マップ。 必須！
* **バリエーションマスク**: *グレースケール入力*\
  オプションのバリエーションマスク。オーバーライドをTrueに設定して有効にします。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **レベル**: *0.0 ～ 1.0*\
  結果の合計レベル。 徐々に効果を明らかにして、長さに影響を与えます。 長い滴り落ちるようにかなり高く設定する必要があります。
* **コントラスト**: *0.0 ～ 1.0*\
  結果のコントラストを調整します。
* **バリエーション**: *0.0 ～ 1.0*&#x200B;縞模様をマスクするために使用する大規模なバリエーションの量を設定します。 この値を0に設定すると、線が完全に均一になるので、これは避けてください。
* **長さ**: *0.0 ～ 8.0*&#x200B;筋の長さがしたたり。 小さなスケールでこの値を大きくしすぎると、目に見えるステッピングになります。 レベルも変えてみましょう。
* **閉塞**: *X、Y、Z、なし* AOが影響する方向を設定します。
* **バリエーションマスクの上書き**: *False/True*&#x200B;バリエーションマスクをカスタム入力スロットで上書きできるようにします。 スパーサーマスクやデンサーマスクは、効果的な方法で効果を発揮し、しずくを抑えることができます。

## サンプル画像

![](../../../../../../assets/leaks-ex.gif)

</td>
</tr>
</table>
