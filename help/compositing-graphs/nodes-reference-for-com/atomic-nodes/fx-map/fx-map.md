---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/fx-map.html"
breadcrumb-title: ''
description: FX-Mapノードを使用して、プロシージャパターンおよびプロシージャエフェクトを作成するために、テクスチャに関数グラフを適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > FX-Map
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: FX-Map
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 2%

---


# FX-Map

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomicノード： FX-Map](../../../../assets/fxmap.png "Atomicノード： FX-Map"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

FX-Mapは、画像やパターン入力を繰り返し複製し再分割し、パラメータや論理関数によって各パターンの分布を制御することができます。

これは、アプリケーションで利用可能な最も強力なアトミックノードの1つであり、最も複雑なノードです。

</td>
</tr>
</table>

[ピクセルプロセッサ](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)と同様に、このノードの動作と出力を決定する関数を定義および作成する操作はユーザーが行います。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> FX-Mapプロセスについて詳しく理解するには、[専用ガイド](../../../../function-graphs/fxmaps/fxmaps.md)を参照してください。

>[!IMPORTANT]
>
> FX-Mapノードを使用する前に、ソフトウェアに関するあらゆる側面について十分に理解し、パラメーター用の[数学関数](../../../../function-graphs/function-graphs.md)を作成することに問題がないことを確認することをお勧めします。

## 例

## パラメーター

他のノードとは異なり、FX-Mapの動作の大部分はパラメーターによって決定されるのではなく、内部のFX-Map関数[&#128279;](../../../../function-graphs/fxmaps/fxmaps.md)を編集することによって決定されることに注意してください。

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | グレースケールとカラー出力画像を切り替えます。 カラーは、グレースケールよりもはるかに低速になります。 |
| <b>背景</b> *フロート/フロート4* | 結果を合成する背景色を設定します。 |
| <b>領域のレンダリング</b> *浮動小数点4* | FX-Mapの各側面の開始ピクセル範囲を設定し、結果としてストレッチ効果を作成できます。 |
| <b>タイル領域</b> *浮動小数点4* | FX-Mapのタイリング距離をオフセットします。 |
| <b>外側をカリング</b> *ブール値* | 通常の範囲から外れる[カリング](../../../../glossary/glossary.md)パターンで最適化を実行します。 |
| <b>粗さ</b> *フロート* | 深度と不透明度の乗数として機能します。 FXマップのブレンドプロセスにバイアスを適用します。 |
| <b>グローバル不透明度</b> *フロート* | FX-mapの出力のグローバル不透明度を設定します。 |

## FX-Mapガイド

*近日公開。*

## 入力コネクタ

|  |  |
| --- | --- |
| <b>背景</b> *グレースケール/カラー*&#x200B;プライマリ | 出力画像の背景色です。 |
| <b>入力画像#</b> *グレースケール/カラー* |  |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

![](../../../../assets/image2015-9-10-17-28-32.png)
