---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/normal-map/bent-normal.html"
breadcrumb-title: ''
description: '[曲げ法線]ノードを使用して、周囲のオクルージョンと間接照明を考慮した曲げ法線マップを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Normal Map > Bent Normal
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 法線を曲げる
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 2%

---


# 法線を曲げる

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![曲がった法線ノードアイコン](../../../../../../assets/rt-bent-normal.png "曲がった法線ノードアイコン")

<b>場所：</b> *フィルター/法線マップ*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

Heightマップ入力に基づいて曲げ法線マップを生成します。 曲げ法線マップは、[法線](../../../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)と[周囲オクルージョン(RTO)](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/ambient-occlusion-rtao/ambient-occlusion-rtao.md)の特殊バージョンで、周囲オクルージョンが埋め込まれた法線マップを作成します。\
これは、リアルタイムエンジンで使用して、たとえば金属のより正確なオクルージョン反射のために、アンビエントオクルージョンを法線マップにベイク処理することができます。

計算時間が長いため、このノードをCPU(SSE)エンジンと組み合わせて使用しないでください。

</td>
</tr>
</table>

## パラメーター

<b>物理サイズを使用</b> *ブール値*\
切り替えると、物理サイズ設定を使用してHeightスケールを指定できます。

<b>物理サイズ</b> *Float3* （<b>[物理サイズの使用]</b>が&#x200B;*True*&#x200B;に設定されている場合に使用可能）\
サーフェスの実際の物理サイズに基づいてHeightスケールを調整します。

<b>サンプル</b> *整数*\
曲がった法線の計算に使用されるレイの数。\
値を大きくすると、パフォーマンスは低下しますが、よりスムーズで正確な結果が得られます。

<b>Heightスケール</b> *浮動小数点（使用物理サイズがFalseに設定されている場合に使用可能）*\
Heightマップ入力の強度の乗数。

<b>配布</b> *整数*\
分布方法を設定します。 影の領域に向かって減衰します。

<b>最大距離</b> *フロート*\
光線が遮断される最大距離を設定します。

<b>広がり角度</b> *フロート*\
光線を照射する広がり角度を設定します。 値1は半球全体です。

<b>標準の形式</b> *整数*\
出力のグリーンチャンネルを反転します。

## サンプル画像

![曲がった法線ノード – 例1](../../../../../../assets/bent-normal-ex-1.jpg "曲がった法線ノード – 例1")
