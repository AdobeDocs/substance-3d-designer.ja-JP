---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/clone-patch.html"
breadcrumb-title: ''
description: 「コピーパッチ」ノードを使用して、スキャンしたマテリアル内の領域をコピーおよびパッチし、斑点や欠陥を除去します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: コピーパッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '465'
ht-degree: 0%

---


# コピーパッチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

## コピーパッチ/コピーパッチのグレースケール

**イン：** *マテリアルフィルター/スキャン処理*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

[クローンパッチ]は、手続き型のパラメトリックな「コピースタンプ」ノードです。 入力した領域のコピーが別の領域に作成され、不要なディテールが隠されます。 ブラシベースのアプリケーションで使い慣れたツールを使用するほど迅速かつ簡単ではありませんが、ノードベースのワークフローで非破壊的に作業できるという主な利点があります。 さらに、このノードは、ターゲット領域とソース領域の両方をスマートに分析し、コントラスト、値、形状に基づいて物事をできるだけブレンドしようとします。

これは主に、不要なディテールが他に存在する場合に備えて、特定の領域を手動で修正する、まれな場面を想定しています。

これは、標準のシンプルな「スタンプ」ブラシとは異なることに注意してください。 ブレンド領域のシェイプは、作業中の領域のシェイプと値に基づいています。つまり、非常に重いノードで、根気が必要ですが、優れた結果が得られます。

また、ギズモを使用してターゲット領域を移動することはできますが、「ソースマトリックス」パラメータを変更してソース領域を設定する必要があることも理解しておく必要があります。

>[!NOTE]
>
> マテリアル全体に適用する場合（ほとんどの場合）は、[マテリアルコピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)を参照してください。
> 
> この操作を複数の入力に対して同時に実行する場合は（マテリアルではない場合）、[マルチクローンパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-clone-patch/multi-clone-patch.md)を参照してください。

## パラメーター

* **標準（色のみ）**: *False/True*\
  入力がノーマルマップであるかどうか、およびブレンドをノーマルマップとして扱うかどうかを設定します。
* **シェイプ**: *正方形、ディスク*&#x200B;スタンプのシェイプを設定します。 ベースとしてのみ使用されます。
* **エッジ**
  * **しきい値**: *0.0 ～ 1.0*&#x200B;ブレンドした領域が到達する範囲を設定します。 この効果は、ターゲット領域のシェイプに沿って段階的に大きくなり、背景が均一の場合は効果がほとんどありません*。*
  * **ぼかし**: *0.0 ～ 2.0*&#x200B;より緩やかな変化が必要な場合に備えて、スタンプ領域のエッジをぼかします。
  * **Smoothness**: *0.0 ～ 2.0*&#x200B;印鑑の形状のエッジを丸めて、アウトラインの流れを滑らかにします。
  * **グリッドの解像度**: *1 - 11*&#x200B;ブレンド解析の解像度を設定します。 値が大きいほど、ブレンドの精度は高くなります。
* **変換**
  * **ソースマトリックス**: *（変換マトリックス）*ソースを変換します（スケールと回転）。 カンバス上では実行できません。これらのパラメーターのみを変更してください。
  * **ソースオフセット**: *-0.5 - 0.5*&#x200B;ソースの場所を変換します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 *このパラメーターは、変更するメインのパラメーターである可能性があります。*
  * **ターゲット行列**: *（変換行列）*ターゲットの場所（スケールと回転）を変形します。 カンバス上のギズモを使用しても実行できます。
  * **ターゲットオフセット**: *-0.5 - 0.5*&#x200B;ターゲットの場所を変換します。 カンバス上のギズモを使用しても実行できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
