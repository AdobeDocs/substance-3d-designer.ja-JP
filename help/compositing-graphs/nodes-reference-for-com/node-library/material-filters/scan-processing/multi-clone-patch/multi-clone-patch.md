---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/multi-clone-patch.html"
breadcrumb-title: ''
description: マルチクローンパッチノードを使用すると、スキャンしたマテリアルアーティファクトを修復するために、複数のテクスチャチャンネルをクローンしてパッチすることができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Multi Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マルチクローンパッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 5%

---


# マルチクローンパッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](multi-clone-patch.resources/clone-patch-multi.png){width="128px"}

![](multi-clone-patch.resources/clone-patch-multi-grayscale.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

このノードは、[クローンパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)の複数入力バージョンです。 最大8個の入力をリンクし、これらすべての入力に対してまったく同じクローン・パッチ操作を実行します。 主に、マルチアングルの写真での使用が意図されています。この写真を[マルチアングルからアルベド](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-albedo/multi-angle-to-albedo.md)または[マルチアングルから標準](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/multi-angle-to-normal/multi-angle-to-normal.md)と組み合わせます。

>[!NOTE]
>
> 詳細については、[コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)を参照してください。マテリアルバージョンについては、[マテリアルコピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/material-clone-patch/material-clone-patch.md)を参照してください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>入力数</b> <i>1 - 8</i> | 同じパッチ操作を受け取る入力の量を設定します。 |
| <b>標準（色のみ）</b> <i>False/True</i> | 入力がノーマルマップであるかどうか、およびブレンドをノーマルマップとして扱うかどうかを設定します。 |
| <b>図形</b> <i>正方形、ディスク</i> | スタンプシェイプを設定します。 ベースとしてのみ使用されます。 |
| <b>エッジ</b> |  |
| <b>しきい値</b> <i>0.0 - 1.0</i> | ブレンド領域の範囲を設定します。 これは、ターゲット領域のシェイプに沿ってステップで大きくなります。背景が均一の場合、ほとんど効果がありません。 |
| <b>ぼかし</b> <i>0.0 - 2.0</i> | より緩やかな変化が必要な場合に備えて、スタンプ領域のエッジをぼかします。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | スタンプシェイプのエッジを丸めて、スムーズに流れるアウトラインにします。 |
| <b>グリッドの解決</b> <i>1 - 11</i> | ブレンド解析の精度を設定します。 値が大きいほど、ブレンドの精度は高くなります。 |
| <b>変換</b> |  |
| <b>ソースマトリックス</b> <i>（変換行列）</i> | ソース（スケールと回転）を変形します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 |
| <b>ソースオフセット</b> <i>-0.5 - 0.5</i> | ソースの場所を移動します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 *このパラメーターは、変更するメインのパラメーターである可能性があります。* |
| <b>ターゲットマトリックス</b> <i>（変換行列）</i> | ターゲットの場所（スケールと回転）を変形します。 カンバス上のギズモを使用しても実行できます。 |
| <b>ターゲットオフセット</b> <i>-0.5 - 0.5</i> | 対象の場所を移動します。 カンバス上のギズモを使用しても実行できます。 |
