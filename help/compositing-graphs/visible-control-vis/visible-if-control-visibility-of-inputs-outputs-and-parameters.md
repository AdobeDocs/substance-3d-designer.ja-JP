---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/visible-if-control-visibility-of-inputs-outputs-and-parameters.html"
breadcrumb-title: ''
description: Substance 3D Designerでvisible if式を使用し、条件に基づいてパラメーターの表示を制御する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Visible if expressions
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: If式の表示
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 1%

---


# If式の表示

&#39;Visible if&#39;式を使用すると、グラフの入力、出力、およびパラメーターの<b>表示/非表示</b>を制御できます。

[パラメーターを公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)する場合、他のパラメーターの状態に基づいて、パラメーターまたはノードコネクタを非表示または表示することができます。 たとえば、ブールパラメータボタンが`true`に設定されている場合にのみスライダーが表示されます。それ以外の場合は効果がなく、ユーザーを混乱させる可能性があるためです。

これを行うには、*論理式*&#x200B;を次の<b>Visible if</b>プロパティに入力します：

* グラフの[入力パラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md);
* グラフの[入力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)ノード；
* グラフの[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードです。

![入力パラメーターの表示を切り替えています](visible-if-control-visibility-of-inputs-outputs-and-parameters.resources/visible-if-example.gif "入力パラメーターの表示を切り替えています"){width="512px"}

論理式が`true`と評価される場合、パラメーター、入力または出力は、現在のグラフを表すすべての[インスタンスノード](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)に表示されます。 それ以外の場合は、*非表示*&#x200B;になります。

これらの条件を記述する論理式が有効であれば、複雑な条件を使用することもできます。

>[!NOTE]
>
> 注意事項
> 
> * この機能&#x200B;*のみ*&#x200B;は、パラメーターまたはコネクタがユーザーインターフェイスに表示されるかどうかに影響し、グラフの計算や結果には&#x200B;*影響しません*。
> * &#39;Visible if&#39;ステートメントで使用されるパラメーターに関数を公開または適用する場合、これらのステートメントは&#x200B;*無視*&#x200B;され、既定では&#39;true&#39;になります。

>[!IMPORTANT]
>
> この機能はSubstance 3Dエコシステム内で動作しますが、一部の統合ではサポートされていない場合があります。 サポートされていない場合、表示条件の既定値は`true`です。

## 「Visible if」式の記述

### 入力パラメータへのアクセス

Visible If Expressionが少なくとも1つの入力を使用する必要がある場合は、次の構文を使用して実行できます。

```
input.identifier 

input["identifier"]
```


>[!WARNING]
>
> **識別子**&#x200B;は、既存の入力パラメーターの&#x200B;**識別子**&#x200B;プロパティの&#x200B;*完全一致*&#x200B;の名前である必要があります。また、*大文字と小文字を区別*&#x200B;して入力する必要があります。 *パラメーターをラベルで参照することはできません*。\
>  参照されたパラメーターが存在しない場合、または論理式が無効な場合、*警告*&#x200B;が&#x200B;**Visible if**&#x200B;プロパティに表示されます。

### 使用可能な演算子

「次の場合に表示」フィールドには、次のパラメーターを使用できます。

* Boolean、Float、およびIntegerの入力。
* `true`と`false`の値（大文字と小文字を区別、大文字と小文字を区別しない）
* `.x` :サブパラメーターにアクセスします
* `&&`<b> </b>：および
* `||`<b> </b>：または
* `!`<b> </b>：なし
* `<`<b>, </b>`>`<b>, </b>`<=`<b>, </b>`>=`<b>, </b>`==`<b>, </b>`!=` ：比較
* `()` ：大括弧

### ブール値に評価する必要があります

「IF」ステートメントの条件としてVisible If式が使用されます。つまり、常に`true`または`false`になる必要があります。

* ブール値は、条件として直接評価できます。 ブール値を持つ単純なボタンを使用するには、この値を超える値を指定する必要はありません。 以下の例（最初の例）を参照してください。
* 通常、ブール以外のパラメーターには&#x200B;*比較*&#x200B;操作が必要です。 比較演算子については上記を、例については以下を参照してください。
* 非ブール値の中には&#x200B;*truthy*&#x200B;または&#x200B;*falsy*&#x200B;になるものがあります。つまり、例えば`false`の`true`として評価できます。 整数値`0`はfalseと評価されます。

## 例

| 条件(「If」) | 数式 | メモ |
| --- | --- | --- |
| 真 | ` input["my_input"]   input.my_input `  ` input["my_input"] == true   input.my_input == true ` | my\_inputはブール値です |
| 偽 | ` !input["my_input"]   !input.my_input `  ` input["my_input"] == false   input.my_input == false `  ` input["my_input"] != true   input.my_input != true ` | my\_inputはブール値です |
| より低い | ` input["my_input"] < 3   input.my_input < 3 ` | my\_inputは整数値です |
| 次と等しい | ` input["param1"] == 2   input.param1 == 2 ` | param1は浮動小数点値または整数値です |
| より低い | ` input["my_input"].y < 3   input.my_input.y < 3 ` | my\_inputは、1つ以上の要素を持つ実数または整数値です – 例： float2(x, y), 整数3(x, y, z) |
| Or | ` input["param1"] \|\| input["param2"]   input.param1 \|\| input.param2 ` | param1とparam2はブール値です |
| And | ` input["param1"] > 0 && input["param2"] > 1   input.param1 > 0 && input.param2 > 1 ` | param1とparam2は浮動小数点値または整数値です |
