---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs.html"
breadcrumb-title: ''
description: DesignerでSubstance関数グラフを作成および使用して、カスタム関数および再利用可能なノードネットワークを構築する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance function graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance関数グラフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '360'
ht-degree: 0%

---


# Substance関数グラフ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[![](function-graphs.resources/function-graphs-01.png){width="120px"}](https://substance3d.adobe.com/)

</td>
<td style="border: 0;" valign="top">

[Substance関数グラフ](https://substance3d.adobe.com/) <b>画像データ（ピクセルのセット全体）の代わりに単一値</b>を処理します（整数、浮動小数、ベクトル）。 関数はノードネットワークを持つグラフですが、[使用されるノード](../function-graphs/nodes-reference-for-fun/function-nodes-overview/function-nodes-overview.md)およびインターフェイスは[通常のSubstanceグラフ](../compositing-graphs/substance-compositing-graphs.md)とは異なります。 このワークフローは、<b>算術演算</b>に完全に基づいており、画像プレビューのサムネールが表示されることはありません。そのため、Substance 3D Designerを使用した<b>はるかに高度な作業</b>になります。

関数は、多くの異なるコンテキストで使用できます。主なコンテキストは、[公開されたパラメーター](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)の動作を変更すること、[ピクセルプロセッサ](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)または[FX-Maps](../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)の動作を作成すること、および[値をSubstanceグラフ](../compositing-graphs/values-compositing-graphs/values-in-substance-compositing-graphs.md)で使用することです。

</td>
</tr>
</table>

## 例

以下に、関数の一般的な使用例をいくつか示します。

### 単純関数

![](function-graphs.resources/function-graphs-02.png)

公開されたパラメーターのコンテキスト内の単純な関数です。 「Intensity」という入力float値を取得し、0 ～ 1（わかりやすい範囲）の範囲を決定し、0.1 ～ 0.8の設定範囲に再マップします。 つまり、ユーザが強度を0に設定すると、内部的には0.1が使用され、Uiが1に設定されると0.8が使用され、その間の値はリニアに補間されます。 この種類の関数は、[パラメーターを公開](../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)する際に一般的に使用されますが、カスタム関数を使用します。

この関数は、HLSLやGLSLに似た擬似コードで&#x200B;*lerp(0.1, 0.8, Intensity)*&#x200B;と記述することもできます。

### 高度な機能

![](function-graphs.resources/function-graphs-03.png){width="545px"}

この高度な関数は、2番目のグレースケールマスク入力の強度に基づいてカラーマップ入力の色相を調整するための[ピクセルプロセッサ](../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)の内部動作を示しています。

システム「$pos」変数を使用して両方の入力をサンプリングし、Alphaを取り除き、カラー値をHSLに変換します。次に、サンプリングしたグレースケール値を掛けて色相コンポーネントを変更します。 その後、ベクトルを再度組み立て、HSLをRGBに戻し、最終出力にAlphaを戻します。

疑似コードでは、これは1行では収まらない、より複雑な関数になります。
