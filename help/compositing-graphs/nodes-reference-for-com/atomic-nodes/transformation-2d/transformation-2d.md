---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/transformation-2d.html"
breadcrumb-title: ''
description: 変換2Dノードを使用して、移動、回転、スケーリングなどのテクスチャに2D変換を適用します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Transformation 2D
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 変形 2D
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9aaf135d4c336ea0cff865524ad1ccd5dcc225bd
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 5%

---


# 変形 2D

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![アトミックノード：変換2D](transformation-2d.resources/comp_transformation_1.png "アトミックノード：変換2D"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

画像に変換、回転、スケーリング、対称、シアーの 2D 変形行列を適用します。

これは、Substance 3D Painterのトランスフォーム(Ctrl+T)や、Photoshopの2Dマッピングマニピュレータとよく似ています。

</td>
</tr>
</table>

これは非常に便利で広く適用されているノードであり、タイリングを増やす、タイリングを削除する、画像を特定の位置に配置する、入力を伸縮または収縮させるなどの操作を実行できます。

ただし、特定のアプリケーションでは完全に一致しないことがあるため、次のノードが適している場合があります。[セーフトランスフォーム](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/safe-transform/safe-transform.md)、[非正方形トランスフォーム](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/non-square-transform/non-square-transform.md)、[クワッドトランスフォーム](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/quad-transform/quad-transform.md)および[台形トランスフォーム](../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/transforms/trapezoid-transform/trapezoid-transform.md)。

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
> タイル表示を無効にする
> 
> &#39;タイリングモード&#39; [基本パラメーター](../../../../glossary/glossary.md)の[継承メソッド](../../../../glossary/glossary.md)を&#39;絶対&#39;に設定すると、パラメーター値を&#39;タイリングなし&#39;に設定できます：
> 
> ![](transformation-2d.resources/tilingmode.png)

>[!NOTE]
>
> ノードのプロパティのスケールと回転の値は、現在の変換に対する&#x200B;*相対値*&#x200B;であり、[適用]ボタンをクリックするまで2Dビューには適用されません。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>変換行列</b> *浮動小数点4* | 直接編集する基になるマトリックスの変形を開きます。 回転とスケールを変更できます。 2Dビューのギズモを使用して調整することもできます。   警告：ビューに直接関連付けられるものではなく、ステップごとに適用できる相対調整です。 |
| <b>オフセット</b> *浮動小数点2* | イメージの2Dディスプレイスメントを定義します。 位置またはオフセットを変更できます。また、2Dビューのギズモを使用して調整することもできます。   2Dビューの出力に直接関連します。 |
| <b>Mipmapモード</b> *整数* | 手動[mipmap](../../../../glossary/glossary.md)レベルに切り替えることができます。これにより、テクスチャフィルターを使用して画像の斑点を減らすことができます。 |
| <b>ミップマップレベル</b> *整数* | 使用する[ミップマップ](../../../../glossary/glossary.md)レベルを設定します。     *&#39;ミップマップモード&#39;が&#39;手動&#39;に設定されている場合に使用可能* |
| <b>マットの色</b> *浮動小数4* | 変形のタイリングが無効な場合に背景として使用される色です。 つまり、変形された入力が出力の一部を覆っていない場合に使用するカラーを設定します。   RGBAカラーで作業している場合は、透明にすることができます。 |
| <b>フィルタリング</b> *整数* | 使用するダウンサンプリング方法を設定します。 ミップマップレベル量を減らしても特に効果がありません。 |

## 入力コネクター

|  |  |
| --- | --- |
| <b>入力</b> *グレースケール/カラー*&#x200B;プライマリ | 変形する画像。 |

## 出力コネクター

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
