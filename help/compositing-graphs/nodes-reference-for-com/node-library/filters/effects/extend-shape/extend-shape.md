---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/effects/extend-shape.html"
breadcrumb-title: ''
description: Extend Shapeノードを使用して、シェイプの境界を超えてシェイプを拡張し、拡張されたマスクおよびパターン効果を作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Effects > Extend Shape
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Extend Shape
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5c9ae53c1de18b1c09789a480cba6b1d70bd350d
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---


# Extend Shape

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapegrayscale.png){width="200px"}

</td>
<td style="border: 0;" valign="top">

![](extend-shape.resources/extendshapecolor.png){width="200px"}

</td>
</tr>
</table>

<b>イン:</b>フィルター/効果

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

<b>Extend Shape</b>ノードは、<b>入力</b>の<i>セクション</i>を設定された方向と距離に拡張します。

<b>ヘルパーの表示</b>パラメーターを使用すると、拡張セクションと拡張方向を視覚化できます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>モード</b> <i>整数</i> | 拡張機能の適用に使用する<i>パラメーター</i>を定義します： <br><br>- <i>双方向</i>: <b>拡張位置</b>および<b>拡張角度</b>で指定された<b>入力</b>のセクションは、<i>拡張距離</b>を超えて、<b>反対方向</i><br>- <i>一方向</i>: <b>拡張位置</b>および<b>入力</b>のセクションです<b>拡張角度</b>は、<i>単一方向</i><br>- <i>開始位置/終了位置</i>で<b>拡張距離</b>まで拡張されています：拡張<i>ベクトル</i>は、<b>開始位置</b>と<b>終了位置</b>で定義されています。 <b>開始位置</b>の<b>入力</b>の<i>垂線</i>セクションは、<b>終了位置</b>までこのベクトル</i>に<i>延長されます |
| <b>延長の距離</b> <i>浮動小数</i> | <b>延長位置</b>と<b>延長角度</b>で指定されたセクションを延長する距離です。 距離は、画像スパンの<i>比率</i>で表されます。 |
| <b>内線位置</b> <i>浮動小数</i> | 拡張するセクションのイメージ内の位置です。 値は、中心からの<i>オフセット</i>として表されます。 |
| <b>拡張角度</b> <i>浮動小数</i> | 開始点を考慮して拡張する必要があるセクションの角度は、<i>垂直セクション</i>です。 |
| <b>開始位置</b> <i>浮動小数2</i> | <i>拡張ベクター</i>の開始位置です。 |
| <b>終了位置</b> <i>浮動小数点2</i> | <i>拡張ベクター</i>の終了位置です。 |
| <b>開始輝度オフセット</b> <i>フロート</i> | 拡張セクションの前</i>のイメージ<i>の領域に輝度オフセットを適用します。 この輝度ーオフセットは、<i>セクション</i>に沿って、セクションに続くイメージの領域の輝度まで補間されます。<br><br><i>注</i>：このパラメーターは、ノードの<b>グレースケール</b>版でのみ使用できます。 |
| <b>終了輝度オフセット</b> <i>フロート</i> | 拡張セクション<i>に続く</i>画像の領域に輝度オフセットを適用します。 この輝度ーのオフセットは、<i>セクション</i>に沿って、セクションの前の画像の領域の輝度まで補間されます。<br><br><i>注</i>：このパラメーターは、ノードの<b>グレースケール</b>版でのみ使用できます。 |
| <b>ラムだ。 オフセットが黒ピクセルを無視します</b> <i>ブール値</i> | <i>True</i>に設定すると、輝度オフセットは<i>両方</i>で指定されます <b>開始輝度のオフセット</b>と<b>終了輝度のオフセット</b>は、<i>黒でない</i>ピクセル（つまり、値が0より大きいピクセル）にのみ適用されます。<br><br><i>注意</i>：このパラメーターは、ノードの<b>グレースケール</b>バージョンでのみ使用できます。 |
| <b>フィルターモード</b> <i>整数</i> | ピクセル間の<i>補間</i>が<br><br>- <i>最も近い</i>：で<i>同じ</i>値（高速）<br>- <i>バイリニア</i>：でバイリニアのフィルターが適用され、<i>より滑らかな</i>外観になるときに、サンプリングされた結果を処理する方法を定義します |
| <b>ヘルパーを表示</b> <i>ブール値</i> | <i>拡張セクション</i>をオーバーレイとして視覚化し、拡張の<i>方向</i>を示す矢印を付けます。 |

## 例

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="border: 0">
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape.gif" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-variant2.jpg" />
        </td>
        <td style="border: 0; background: transparent">
            <img src="extend-shape.resources/extendshape-node.png" />
        </td>
    </tr>
</table>
