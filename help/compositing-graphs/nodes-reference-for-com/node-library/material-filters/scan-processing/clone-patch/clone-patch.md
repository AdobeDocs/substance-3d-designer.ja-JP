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
source-git-commit: ca90755a159a7e0297bb26d1e3522b0cfeb6f2ac
workflow-type: tm+mt
source-wordcount: '456'
ht-degree: 3%

---


# コピーパッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch.png){width="128px"}

![](../../../../../../assets/clone-patch-grayscale.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

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

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>標準（色のみ）</b> <i>False/True</i> | 入力がノーマルマップであるかどうか、およびブレンドをノーマルマップとして扱うかどうかを設定します。 |
| <b>図形</b> <i>正方形、ディスク</i> | スタンプシェイプを設定します。 ベースとしてのみ使用されます。 |
| <b>エッジ</b> |  |
| <b>しきい値</b> <i>0.0 - 1.0</i> | ブレンド領域の範囲を設定します。 これは、ターゲット領域のシェイプに沿って段階的に大きくなり、背景が均一の場合の効果はほとんどありません。<i>。</i> |
| <b>ぼかし</b> <i>0.0 - 2.0</i> | より緩やかな変化が必要な場合に備えて、スタンプ領域のエッジをぼかします。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | スタンプシェイプのエッジを丸めて、スムーズに流れるアウトラインにします。 |
| <b>グリッドの解決</b> <i>1 - 11</i> | ブレンド解析の精度を設定します。 値が大きいほど、ブレンドの精度は高くなります。 |
| <b>変換</b> |  |
| <b>ソースマトリックス</b> <i>（変換行列）</i> | ソース（スケールと回転）を変形します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 |
| <b>ソースオフセット</b> <i>-0.5 - 0.5</i> | ソースの場所を移動します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 <i>このパラメーターは、変更するメインのパラメーターである可能性があります。</i> |
| <b>ターゲットマトリックス</b> <i>（変換行列）</i> | ターゲットの場所（スケールと回転）を変形します。 カンバス上のギズモを使用しても実行できます。 |
| <b>ターゲットオフセット</b> <i>-0.5 - 0.5</i> | 対象の場所を移動します。 カンバス上のギズモを使用しても実行できます。 |
