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
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---


# RTシャドウ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![RTシャドウノードアイコン](rt-shadow.resources/rt-shadow-01.png "RTシャドウノードアイコン")

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

高さマップ入力からレイトレースシャドウを生成します。

計算時間が長いため、このノードをCPU(SSE)エンジンと組み合わせて使用しないでください。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>サンプル</b> <i>整数</i> | シャドウの計算に使用するレイの数です。<br>値を大きくすると、パフォーマンスを犠牲にして、より滑らかで正確な結果が得られます。 |
| <b>モード</b> <i>整数</i> | サーフェスにシャドウを描画する方法。 |
| <b>Heightスケール</b> <i>フロート</i> | 入力Heightマップの強度の乗数。 |
| <b>明るい位置</b> <i>浮動小数点2</i> | 表面を囲む球体上の光源の位置：<br><br>- <b>X</b>：水平位置、ターン数；<br>- <b>Y</b>：垂直位置。0.5は天頂、0/1は水平線です。 |
| <b>光の強さ</b> <i>浮動小数</i> | 光源の強度。 |
| <b>明るいサイズ</b> <i>浮動小数点2</i> | （<b>モード</b>が<i>シェーディング</i>に設定されている場合に使用可能）光源のサイズを長方形で示します。 |
| <b>ライトスケール（ソフトシャドウ）</b> <i>フロート</i> | 光線の方向に対する<b>ライトサイズ</b>の貢献度の乗数。<br>値が大きいほど、影が滑らかになります。 |
| <b>地平線より明るさを維持</b> <i>ブール値</i> | <b>光源の位置</b>が水平線の下に光を置くように設定されている場合、このパラメータは、光がしきい値を超えないようにします。つまり、Y値は[0;1]の範囲に固定されます。 |
| <b>シャドウの不透明度</b> <i>フロート</i> | サーフェス上に描画される影の不透明度の乗数。 |
| <b>シャドウの減衰</b> <i>フロート</i> | シャドウがキャスターから離れるほど、シャドウの減衰の乗数が大きくなります。<br>値を0にすると、均一なシャドウが生成されます（ソフトシャドウは引き続き適用されます）。 |
| <b>シャドウの最大長</b> <i>フロート</i> | キャスターから影を引き出せる最大距離です。<br>値0を指定すると、影は表示されません。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-02.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-03.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="rt-shadow.resources/rt-shadow-04.jpg" />
        </td>
    </tr>
</table>
