---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/variables/system-variables.html"
breadcrumb-title: ''
description: 高度なワークフロー用のSubstance 3D Designerの関数グラフに組み込まれているシステム変数について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Built-in variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ビルトイン変数
user-guide-description: ''
user-guide-title: ''
source-git-commit: c002fea6f396f09ccb3218bd290db812d8367dc4
workflow-type: tm+mt
source-wordcount: '549'
ht-degree: 3%

---


# ビルトイン変数

組み込み変数を[Substance関数グラフ](../../../function-graphs/function-graphs.md)で使用して、特定の値にアクセスできます。 常に`$` （ドル）記号で始まります。

特定のコンテキストでのみ使用できる変数もあります。

<b>すべてのノード</b>

システム変数

| 名前 | タイプ | 目的 |
| --- | --- | --- |
| $size | Float2 | 現在のノードのサイズをピクセル単位で返します。   [Output Size](../../../compositing-graphs/output-size/output-size.md)パラメーターで使用されている場合、*Relative to...* [継承メソッド](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されている場合、*継承された値*&#x200B;を返します。 |
| $sizelog2 | Float2 | 上記と同様ですが、サイズは2の累乗値として返されます（例： 2048\*2048画像の場合、`$sizelog2`は11を返します）。   [Output Size](../../../compositing-graphs/output-size/output-size.md)パラメーターで使用されている場合、*Relative to...* [継承メソッド](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されている場合、*継承された値*&#x200B;を返します。 |
| $pixelratio | 整数 | 現在のノードのピクセル比（継承または絶対）に対応する整数値を返します： 0：伸長1：正方形 |
| $tiling | 整数 | 現在のノードのタイリングモード（継承または絶対）に対応する整数値を返します。 0:タイリングなし1：水平タイリング2：垂直タイリング3: HおよびVタイリング |
| $physicalsize | Float3 | [グラフの](../../../compositing-graphs/graph-parameters/graph-parameters.md) <b>物理サイズ</b>プロパティ値を返します。 |
| $uvtile | Integer2 | UDIMワークフローを使用している場合、この変数は現在のudimのインデックスをUとVで返します。   例えば、タイル1003の場合は(2, 0)、タイル1118の場合は(7, 11)、... |

<b>FX-Map</b>

システム変数

| 名前 | タイプ | 目的 |
| --- | --- | --- |
| $pos | Float2 | パターンの発生位置を返します。 原点(0, 0)はイメージの左上隅にあります。 |
| 深度($C) | 浮動小数 | [FX-Map](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)ノードのオクターブ（レベル）番号を返します。 これにより、ノードが表すクアッドツリーのレベルに応じてノードの動作を変更できます。 |
| $depthpow2 | 浮動小数 | 上記と同様ですが、オクターブ（レベル）数の累乗に引き上げられた2の逆数(1/（2^オクターブ）を返します。 これは、一般的な計算に役立つヘルパー値です。 |
| $number | 浮動小数 | 描かれたパターンの番号を返します。 これは、[Iterate](../../../function-graphs/fxmaps/using-functions-in-fxmaps/iterate-and-number-var/iterate-and-number-variable.md)ノードを制御する動的関数グラフでアクセスして、各繰り返しステップでの動作を変更できます。   `$number`は1ではなく0からカウントを開始することに注意してください。   Iterateノードのチェーンを使用する場合、`$number`変数は、使用される関数パラメーターの前に接続された最後のIterateノードからの反復番号を返します。 複数のIterateノードから反復番号を取得する場合は、[Set](../../../function-graphs/fxmaps/using-functions-in-fxmaps/using-the-set-sequence/using-the-set-sequence-nodes.md)ノードから「カスタム変数」を使用する必要があります。 |

<b>ピクセルプロセッサ</b>

システム変数

| 名前 | タイプ | 目的 |
| --- | --- | --- |
| $pos | Float2 | 評価対象のピクセルの位置を返します。 |

<b>グローバル</b>

システム変数

| 名前 | タイプ | 目的 |
| --- | --- | --- |
| $time | 浮動小数 | この変数は、Substance engineが起動してからの時間を秒単位で返します。 グラフで使用する場合は、経過時間に応じて結果が変化します。  **注意：**&#x200B;現在、Designerではこの値を変更する方法はありませんが、アニメーションの[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)、[動的ストローク](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/painting/dynamic-strokes/creating-custom-dynamic-strokes)の[Substance 3D Painter](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/home)など、Substance engineを統合するアプリケーションでは、この値を利用できます。 |
| $normalformat | 整数 | 現在の環境で使用される標準のフォーマット（DirectXまたはOpenGL）。  **注意：**&#x200B;このSubstance engineは、Designerには影響を与えません。変数を組み込む他のアプリケーションで使用される可能性があります。 |
