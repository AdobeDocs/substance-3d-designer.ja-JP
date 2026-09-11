---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: クローンパッチ・ノードを使用して、スキャンしたマテリアルのアーチファクトを修復するために、テクスチャリージョンをクローニングおよびパッチします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアル クローンパッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '326'
ht-degree: 4%

---


# マテリアル クローンパッチ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](material-clone-patch.resources/clone-patch-material.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

[クローンパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)のマルチチャネルフルマテリアル版です。 マテリアルのすべてのチャンネルに対してクローンパッチを実行します。 [詳細については、元のバージョンを参照してください。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

これは、マテリアルのすべてのチャンネルからディテールを取り除く場合に非常に便利です。 複数のチャンネルのデバッグ画像を出力して、スマートパッチ領域がどのように見えるかを確認します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>マスク</b> <i>グレースケール入力</i> | ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>チャネル</b> | この領域でマテリアルチャンネルのオンとオフを切り替えます。例えば、メタリック/ラフネスの代わりにSpecular/光沢度マップを使用する場合などです。 |
| <b>図形</b> <i>正方形、ディスク</i> | スタンプシェイプを設定します。 ベースとしてのみ使用されます。 |
| <b>エッジ</b> |  |
| <b>しきい値（複数チャンネル）</b> <i>0.0 - 1.0</i> | ブレンド領域の範囲を設定します。 この効果は、ターゲット領域のシェイプに沿って段階的に大きくなるので、背景が均一の場合の効果はほとんどありません。 視覚的な不一致が生じる可能性があるため、チャンネル間でこの値を頻繁に変更するときは注意してください。 |
| <b>ぼかし</b> <i>0.0 - 2.0</i> | より緩やかな変化が必要な場合に備えて、スタンプ領域のエッジをぼかします。 |
| <b>Smoothness</b> <i>0.0 - 2.0</i> | スタンプシェイプのエッジを丸めて、スムーズに流れるアウトラインにします。 |
| <b>グリッドの解決</b> <i>1 - 11</i> | ブレンド解析の精度を設定します。 値が大きいほど、ブレンドの精度は高くなります。 |
| <b>変換</b> |  |
| <b>ソースマトリックス</b> <i>（変換行列）</i> | ソース（スケールと回転）を変形します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 |
| <b>ソースオフセット</b> <i>-0.5 - 0.5</i> | ソースの場所を移動します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 *このパラメーターは、変更するメインのパラメーターである可能性があります。* |
| <b>ターゲットマトリックス</b> <i>（変換行列）</i> | ターゲットの場所（スケールと回転）を変形します。 カンバス上のギズモを使用しても実行できます。 |
| <b>ターゲットオフセット</b> <i>-0.5 - 0.5</i> | 対象の場所を移動します。 カンバス上のギズモを使用しても実行できます。 |
