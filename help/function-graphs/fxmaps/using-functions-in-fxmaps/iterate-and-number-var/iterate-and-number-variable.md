---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: FXMapで反復変数および数値変数を使用して、ループパターンおよび手続き型バリエーションを作成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 反復変数および数値変数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 0%

---


# 反復処理および$number変数

![](../../../../assets/iterate-1.jpg)

Iterateノードは、右側にコネクトされたノードをIterations値で指定された時間だけレンダーします。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="../../../../assets/1-iteration.png"/></div> | 1回繰り返し：ガウスパターンは1回レンダリングされます |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="../../../../assets/10-iterations.png"/></div> | 10回繰り返す：ガウスパターンは同じ場所に10回レンダリングされます |

Iterateノードを使用する場合は、 $number変数を使用して現在の反復値を取得できます。 $numberはfloat値で、0から始まります。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../assets/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](../../../../assets/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Pattern Offsetパラメーターで設定されたこの関数は、パターンごとに1つずつ、10回実行されます。

最初のパターンは、0に等しい$number値を持ち、次に(0, 0)座標でレンダリングされます。 2番目のパターンの$number値は1で、次のパターンでは(0.1, 0)座標(1 x 0.1 = 0.1)でレンダリングされます。

サンプルのダウンロード： [iterate\_node.sbs](https://helpx.adobe.com/content/dam/help/en/substance-3d/documentation/sddoc/files/102400023/102367299/1/1423458106000/iterate-node.sbs)
