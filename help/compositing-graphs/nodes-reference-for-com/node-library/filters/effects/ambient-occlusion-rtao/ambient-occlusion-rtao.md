---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/ambient-occlusion-rtao.html"
breadcrumb-title: ''
description: '[環境オクルージョン(RTAO)]ノードを使用して、リアルなシェーディングを実現するために、Heightマップからリアルタイムの環境オクルージョンマップを生成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Ambient Occlusion (RTAO)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境オクルージョン(RTAO)
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 0%

---


# 環境オクルージョン(RTAO)

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RTAOノードアイコン](../../../../../../assets/rt-ao.png "RTAOノードアイコン")

<b>場所：</b> *フィルター/効果*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

Heightマップの入力に基づいて環境オクルージョンマップを生成します。

このフィルターは、HBAOに比べて精度の高い結果が得られますが、計算時間の関係上、CPU(SSE)エンジンと組み合わせて使用しないでください。

[環境オクルージョン(HBAO) （フィルターノード）](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-hbao/ambient-occlusion-hbao-filter-node.md)を参照して、より高速で単純な代替手段を使用してください。

</td>
</tr>
</table>

## パラメーター

<b>物理サイズを使用</b> *ブール値*\
切り替えると、物理サイズ設定を使用してHeightスケールを指定できます。

<b>物理サイズ</b> *Float3* （<b>[物理サイズの使用]</b>が&#x200B;*True*&#x200B;に設定されている場合に使用可能）\
サーフェスの実際の物理サイズに基づいてHeightスケールを調整します

<b>サンプル&#x200B;</b>*整数*\
環境オクルージョンの計算に使用されるレイの数。\
値を大きくすると、パフォーマンスが低下しますが、よりスムーズで正確な結果が得られます。

<b>Heightスケール</b> *浮動小数点* （<b>物理サイズの使用</b>が&#x200B;*偽*&#x200B;に設定されている場合に使用可能）\
Heightマップ入力の強度の乗数。

<b>配布</b> *Integer*&#x200B;ディストリビューションメソッドを設定します。 影の領域に向かって減衰します。

<b>最大距離</b> *フロート*\
光線が遮断される最大距離を設定します。

<b>広がり角度</b> *フロート*\
光線を照射する広がり角度を設定します。 値1は半球全体です。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RTAOノード – 例1](../../../../../../assets/image2021-6-18-11-7-48.png "RTAOノード – 例1")

</td>
<td style="border: 0;" valign="top">

![RTAOノード – 例2](../../../../../../assets/image2021-6-18-11-9-0-1.png "RTAOノード – 例2")

</td>
</tr>
</table>
