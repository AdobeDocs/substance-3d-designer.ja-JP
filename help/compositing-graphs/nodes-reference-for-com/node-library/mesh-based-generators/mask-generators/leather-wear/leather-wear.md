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
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 1%

---


# レザーウェア

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/leather-wear.png){width="128px"}

## レザーウェア

**イン：** *メッシュベースのジェネレーター**/マスクジェネレーター*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

ベイク済みマップとユーザー設定に基づいて白黒マスクを生成します。 [Painter](https://support.allegorithmic.com/documentation/display/SPDOC/Substance+Painter)の[スマートマスク](https://support.allegorithmic.com/documentation/display/SPDOC/Smart+Materials+and+Masks)に似ています。

このマスクは、レザーのパターンで磨耗を表現し、曲率に基づいてエッジの磨耗を増やします。 機能が[ファイバーグラスEdge Wear](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/mesh-based-generators/mask-generators/fiber-glass-edge-wear/fiber-glass-edge-wear.md)と似ており、パラメーターはほとんど同じです。

## パラメーター

### 入力

* **曲率**: *グレースケール入力*\
  エッジの配置に使用するベイク済みマップ。 必須！
* **環境オクルージョン**: *グレースケール入力*\
  特定の領域を閉塞するベイク済みマップを使用する。 推奨されますが、必須ではありません。
* **経年劣化入力**: *グレースケール入力*\
  「カスタム経年劣化を使用」パラメーターで切り替えることができる、オプションの経年劣化マップ入力スロット。
* **マスク（オプション）**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。

### パラメーター

* **磨耗のレベル**: *0.0 ～ 1.0*&#x200B;全体的な磨耗のレベルを設定し、徐々に明らかにします。
* **磨耗のコントラスト**: *0.0 ～ 1.0*&#x200B;効果のコントラストを設定します。
* **経年劣化量**: *0.0 ～ 1.0*&#x200B;エッジ間でブレンドする経年劣化の量（既定のレザーパターン）を設定します。
* **アンビエントオクルージョンマスク**: *0.0 ～ 1.0* AOが摩耗効果をマスクする範囲を設定します。
* **曲率の重み**: *0.0 ～ 1.0*&#x200B;曲率のエッジが最終結果に影響する範囲を設定します。 0に設定しても、曲率マップは必要です。
* **カスタム経年劣化の使用**: *False/True*&#x200B;組み込みの既定のレザーパターンの上書きを有効にします。 代わりにカスタム入力スロットを使用してください。

## サンプル画像

![](../../../../../../assets/leather-wear-ex.gif)

</td>
</tr>
</table>
