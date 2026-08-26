---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/control-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer機能グラフのアクセス制御ノードは、フローおよび実行ロジックを制御します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: コントロール
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '557'
ht-degree: 1%

---


# 制御ノード

このページでは、*実行フロー*&#x200B;を制御することを目的とする[関数グラフ](../../../../function-graphs/the-function-graph/the-function-graph.md)のノードについて説明します。

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![If...Elseノード](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/IfElse_Node.jpg "If...Elseノード")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## If...Else

プログラミング言語と同様に、If...Elseノードでは、事前に定義された条件に従って結果をフィルタリングできます。

</td>
</tr>
</table>

このノードを[論理ノード](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md)および[比較ノード](../../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md)と組み合わせて使用すると、チェックする条件を構築するのに役立ちます。

+++入力コネクタ
<b>条件</b> *ブール値*\
ノードの出力を制御する条件。

<b>If</b> *変数の型*<b>条件</b>が&#x200B;*真*&#x200B;の場合にノードによって出力される値。

<b>Else</b> *変数の型*<b>条件</b>が&#x200B;*False*&#x200B;の場合にノードによって出力される値。

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![シーケンスノード](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/Sequence_Node.jpg "シーケンスノード")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 順番

グラフの一部が別の部分の前に計算されるようにします。

</td>
</tr>
</table>

これは、作成、読み取り、更新される変数の状態を制御するために重要です。

シーケンスノードの詳細については、このドキュメントの[Using the Set/Sequence nodes](../../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md)ページを参照してください。

+++入力コネクタ
<b>インチ</b> *変数の型*\
最初に計算されるグラフの部分

<b>最後</b> *変数の型*\
グラフの最後に計算される部分

+++

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Whleループノード](https://helpx.adobe.com/content/dam/substance-3d-designer/function-graphs/nodes/atomic-function-nodes/control/WhileLoop-Node.jpg "Whle Loopノード")

</td>
<td width="100.00%" style="border: 0;" valign="top">

## While ループ

<b>Init</b>分岐を1回実行し、<b>Exit Cond.</b>に対して繰り返し実行します。 <b>本体をループ</b>する操作は、<b>Exit Cond.</b>まで実行されます。 branchは&#x200B;*True*&#x200B;を返します。

ループが完了すると、ノードは<b>ループ本文</b>の最後の反復処理の結果を出力します。

</td>
</tr>
</table>

ループは暗黙の最大反復回数を持ち、-1に設定することで無効にできます。

変数は反復処理を行っても値を保持し、終了条件（終了条件）でアクセスできます。\
つまり、反復ごとにインデックス値を追加し、終了条件でその値をチェックして、必要なループの数を制御できます。

>[!IMPORTANT]
>
> <b>Exit Cond.</b>に接続されているノード また、<b>ループ本文</b>の分岐は、グラフの他の分岐に接続できません。

+++入力コネクタ
<b>初期化</b> *変数の型*\
最初の反復の前に計算されるグラフの部分、つまりループの開始。

<b>続行を終了</b> *ブール値*\
ループを停止するためにtrueとなる必要がある条件。 反復処理ごとに再計算されます。\
*注意：*&#x200B;繰り返しの最大数は、引き続き<b>最大繰り返し</b>パラメーターに制限されています。

<b>ループ本文</b> *変数の型*\
ループから得られるグラフ。 反復処理ごとに再計算されます。

+++

+++パラメーター
<b>最大 反復</b> *整数*\
ノードが実行する最大反復回数。\
この最大数に達するか、終了条件がtrueになったときに、次のいずれかの条件が最初に満たされると、ノードの反復が停止します。\
この最大値は、値を&#x200B;*-1*&#x200B;に設定することで無効にできます。 この時点では、終了条件のみが反復を停止できます。

&#39;Maxを設定しています。 iterationsを–1に設定すると、追跡と更新を行うカウンタが1つ少なくなるため、小さなループでのパフォーマンスが向上します。

ただし、<b>無限ループ</b>を生成してDesignerが応答しなくなる可能性があるため、ノードの構成には注意してください。

+++

While Loopノードに関するこのチュートリアルをご覧ください。
