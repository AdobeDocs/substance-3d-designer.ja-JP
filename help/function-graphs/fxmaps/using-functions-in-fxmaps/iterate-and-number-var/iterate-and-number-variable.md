---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-variable.html"
breadcrumb-title: ''
description: FXMapで反復変数と数値変数を使用して、ループパターンとプロシージャルバリエーションを作成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > FXMaps > Using Functions in FXMaps > Iterate and number variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 反復変数および数値変数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 65a0ec6dc38e7595406c0c531be72ad1670dfb86
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---


# 反復処理して`$number`変数

![](iterate-and-number-variable.resources/iterate-1.jpg)

Iterateノードは、右側にコネクトされたノードをIterations値で指定された時間だけレンダーします。

| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r0-column-c0_image" src="iterate-and-number-variable.resources/1-iteration.png"/></div> | 1回繰り返し：ガウスパターンは1回レンダリングされます |
| --- | --- |
| <div><img class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dx_table_row-r1-column-c0_image" src="iterate-and-number-variable.resources/10-iterations.png"/></div> | 10 反復：ガウスパターンは同じ場所に10回レンダリングされます |

Iterateノードを使用する場合、`$number`変数を使用して現在の反復値を取得できます。 `$number`は浮動小数値で、0から始まります。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/position-function.jpg){width="300px"}

</td>
<td style="border: 0;" valign="top">

![](iterate-and-number-variable.resources/10-iterations-position-function.png){width="300px"}

</td>
</tr>
</table>

Pattern Offsetパラメーターで設定されたこの関数は、パターンごとに1つずつ、10回実行されます。

最初のパターンの`$number`の値は0で、次に(0, 0)座標でレンダリングされます。 2番目のパターンの`$number`の値は1で、次のパターンでは(0.1, 0)座標(1 x 0.1 = 0.1)でレンダリングされます。
