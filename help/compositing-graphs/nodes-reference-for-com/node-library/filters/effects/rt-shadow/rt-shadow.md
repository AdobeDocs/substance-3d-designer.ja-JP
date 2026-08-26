---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/rt-shadow.html"
breadcrumb-title: ''
description: RT Shadowsノードを使用して、ジオメトリからリアルタイムシャドウ情報を計算し、ダイナミックなライティング効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > RT Shadows
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: RTシャドウ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 0%

---


# RTシャドウ

<table>
<tr style="border: 0;">
<td width="41.60%" style="border: 0;" valign="top">

![RTシャドウノードアイコン](../../../../../../assets/rt-shadow.png "RTシャドウノードアイコン")

<b>場所：</b> *フィルター/効果*

</td>
<td width="58.30%" style="border: 0;" valign="top">

## 説明

Heightマップ入力からレイトレースシャドウを生成します。

計算時間が長いため、このノードをCPU(SSE)エンジンと組み合わせて使用しないでください。

</td>
</tr>
</table>

## パラメーター

<b>サンプル</b> *整数*\
シャドウの計算に使用されるレイの数。\
値を大きくすると、パフォーマンスは低下しますが、よりスムーズで正確な結果が得られます。

<b>モード</b> *整数*\
サーフェスにシャドウを描画する方法。

<b>Heightスケール</b> *フロート*\
入力Heightマップの強度の乗数。

<b>光源の位置&#x200B;</b>*Float2*\
サーフェスを囲む球上の光源の位置：
* <b>X</b>：水平位置、ターン数；
* <b>Y</b>：垂直位置。0.5が天頂で、0/1が水平線です。

<b>光の強さ</b> *フロート*\
光源の強度。

<b>明るいサイズ</b> *Float2* （<b>Mode</b>が&#x200B;*Shaded*&#x200B;に設定されている場合に使用可能）\
光源のサイズを長方形で指定します。

<b>ライトスケール（ソフトシャドウ）</b> *フロート*\
光線の方向に対する<b>光のサイズ</b>の寄与度の乗数。\
値を大きくすると、シャドウが滑らかになります。

<b>地平線より明るさを維持</b> *ブール値*\
<b>光源の位置</b>が水平線の下に光を置くように設定されている場合、このパラメータは、光がしきい値を超えないようにします。つまり、Y値は[0;1]の範囲に固定されます。

<b>シャドウの不透明度</b> *フロート*\
サーフェス上に描画される影の不透明度の乗数。

<b>シャドウの減衰</b> *フロート*\
シャドウがキャスターから離れるほど減衰する乗数。\
値を0に設定すると、均一なシャドウになります（ソフトシャドウは適用されます）。

<b>シャドウの最大長</b> *フロート*\
キャスターからシャドウを描画できる最大距離です。\
値を0に設定すると、シャドウは表示されません。

## サンプル画像

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![RTシャドウノード – 例1](../../../../../../assets/RTShadows-01.jpg "RTシャドウノード – 例1")

</td>
<td style="border: 0;" valign="top">

![RTシャドウノード – 例2](../../../../../../assets/RTShadows-02.jpg "RTシャドウノード – 例2")

</td>
<td style="border: 0;" valign="top">

![RTシャドウノード – 例3](../../../../../../assets/RTShadows-03.jpg "RTシャドウノード – 例3")

</td>
</tr>
</table>
