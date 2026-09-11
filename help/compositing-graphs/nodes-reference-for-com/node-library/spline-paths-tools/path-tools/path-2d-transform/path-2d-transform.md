---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/path-2d-transform.html"
breadcrumb-title: ''
description: パス2D変形ノードを使用して、直線移動、回転、スケーリングの各操作でパスを変形します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Path 2D Transform
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 経路2D変形
user-guide-description: ''
user-guide-title: ''
source-git-commit: f9ae596767e754b5c0f62ed6bdb6f16dd33bb799
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 2%

---


# 経路2D変形

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](path-2d-transform.resources/path-2d-transform-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

ギズモを使用してパスを変形します。

</td>
</tr>
</table>

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | エンコードされたセグメントパスのリスト。 この入力を[マスクの結果にパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/mask-to-paths/mask-to-paths.md)または別のパス処理ノードに接続します。 |

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>パス</b> <i>色</i> | 変形パス。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)を使用して、結果がどんな結果になるかを把握したり、別のパス処理ノードを使用したり、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)に入力して、さらにスプラインとして処理したりすることができます。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>マトリックスの変形</b> <i>浮動小数4</i> | スプラインに適用される変換行列。 マトリックスパラメーターは、次の3つの方法で編集できます。<br>*– 変換ギズモ：*&#x200B;スプライン2D変形ノードが選択された場合、[2D ビュー](../../../../../../interface/2d-view/2d-view.md)に表示されたギズモのハンドルを微調整します。<br>*– 回転/伸縮:*&#x200B;スプラインの回転と伸縮を個別に制御します。 値は常に現在の変換に対して相対的に適用されることに注意してください。 例えば、50%の幅を2回適用すると、幅が25%になります。<br>*– 行列の値：* <b>行列の値を編集</b>ボタンをクリックして、行列の生の数値を直接入力します。 |
| <b>オフセット</b> <i>浮動小数2</i> | 位置オフセットをX（水平）およびY（垂直）のスプラインに適用します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>前</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant1.jpg" alt="Paths2DTransform-Variant1">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="path-2d-transform.resources/PathsPolygon_Variant1.jpg" alt="PathsPolygon_Variant1">
      <br><i>前</i>
    </td>
    <td>
      <img src="path-2d-transform.resources/Paths2DTransform-Variant2.jpg" alt="Paths2DTransform-Variant2">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>
