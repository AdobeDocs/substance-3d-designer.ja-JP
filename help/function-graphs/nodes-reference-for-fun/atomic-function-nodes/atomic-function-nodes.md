---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes.html"
breadcrumb-title: ''
description: カスタム関数を構築するためのSubstance関数グラフにおける最小ノード単位であるアトミックファンクションノードについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Atomic function nodes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: アトミック機能ノード
user-guide-description: ''
user-guide-title: ''
source-git-commit: 953b99bc5f48c431e7ace47a23b0b451cceaa0db
workflow-type: tm+mt
source-wordcount: '1108'
ht-degree: 17%

---


# アトミック機能ノード

Substanceグラフの[atomic nodes](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)と同様に、Substance関数グラフのatomic nodesは、その種類のグラフの最小ノード単位です。

目的に応じて、いくつかのカテゴリに分類できます。

| カテゴリ | ノード | 入力タイプ | 出力タイプ | 説明 |
|:---------------------------------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------|:------------------|:---------------------------------------------------------------------------------------------------|
| [定数](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md) | 浮動小数 | - | 浮動小数 | 定数の浮動値を定義します（例： 0.1） |
|                                                                                                                                        | Float2 | - | Float2 | 2つの浮動値の定数ベクトルを定義します（例： 0.1、0.2） |
|                                                                                                                                        | Float3 | - | Float3 | 3つの浮動値の定数ベクトルを定義します（例： 0.1、0.2、0.3） |
|                                                                                                                                        | Float4 | - | Float4 | 4つの浮動値の定数ベクトルを定義します（例： 0.1、0.2、0.3、0.4） |
|                                                                                                                                        | 整数 | - | 整数 | 定数値を定義します（例： 1） |
|                                                                                                                                        | Integer2 | - | Integer2 | 2つの整数値の定数ベクトルを定義します。例： (1, 2) |
|                                                                                                                                        | Integer3 | - | Integer3 | 3つの整数値の定数ベクトルを定義します。例： (1, 2, 3) |
|                                                                                                                                        | Integer4 | - | Integer4 | 4つの整数値から成る定数ベクトルを定義します。例： (1, 2, 3, 4) |
|                                                                                                                                        | ブーリアン | - | ブーリアン | 定数のブール値を定義します。例： TrueまたはFalse |
|                                                                                                                                        | 文字列 | - | 文字列 | 定数文字列値を定義します（例： &quot;Substance&quot;） |
| [ベクター](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md) | 浮動小数点ベクトル 2 | フロート1 | Float 2 | 2つの座標を使用して2つの浮動小数点をベクトルにキャストします |
|                                                                                                                                        | 浮動小数点ベクトル 3 | フロート1/フロート2 | 浮動小数 3 | 3座標のベクトルに2つの浮動小数点値をキャストします |
|                                                                                                                                        | 浮動小数点ベクトル 4 | フロート1 / 2 / 3 | 浮動小数 4 | 4座標のベクトルに2つの浮動小数点値をキャストします |
|                                                                                                                                        | スウィズル浮動小数 1 | ベクトル実数 | フロート1 | ベクトルから浮動座標を抽出します。 |
|                                                                                                                                        | スウィズル浮動小数 2 | ベクトル実数 | Float2 | ベクトルから2つの浮動座標を抽出します |
|                                                                                                                                        | スウィズル浮動小数 3 | ベクトル実数 | Float3 | ベクトルから3つの浮動座標を抽出します |
|                                                                                                                                        | スウィズル浮動小数 4 | ベクトル実数 | Float4 | ベクトルから4つの浮動座標を抽出します |
|                                                                                                                                        | 整数ベクトル 2 | Integer2 | 整数ベクトル 2 | 2つの座標を使用して2つの整数値をベクトルにキャストします |
|                                                                                                                                        | 整数ベクトル 3 | Integer3 | Integer3 | 3座標のベクトルに2つの整数値をキャストします |
|                                                                                                                                        | ベクトル整数 4 | Integer4 | Integer4 | 4座標のベクトルに2つの整数値をキャストします |
|                                                                                                                                        | スウィズル整数 1 | ベクトル整数 | Integer1 | ベクトルから整数座標を抽出します。 |
|                                                                                                                                        | スウィズル整数 2 | ベクトル整数 | Integer2 | ベクトルから2つの整数座標を抽出します。 |
|                                                                                                                                        | スウィズル整数 3 | ベクトル整数 | Integer3 | ベクトルから3つの整数座標を抽出します。 |
|                                                                                                                                        | スウィズル整数 4 | ベクトル整数 | Integer4 | ベクトルから4つの整数座標を抽出します。 |
| [変数](../../../function-graphs/variables/variables.md) | 設定 | 任意 | 入力タイプ | 変数を設定します |
|                                                                                                                                        | Integer1を取得 | - | Integer1 | 関数またはグラフの整数値入力を取得する |
|                                                                                                                                        | 整数 2 を取得 | - | Integer2 | 関数またはグラフInteger2値の入力を取得します。 |
|                                                                                                                                        | 整数 3 を取得 | - | Integer3 | 関数またはグラフのInteger3値の入力を取得します。 |
|                                                                                                                                        | 整数 4 を取得 | - | Integer4 | 関数またはグラフInteger4値の入力を取得します |
|                                                                                                                                        | Float1を取得 | - | フロート1 | 関数またはグラフ浮動小数点値の入力を取得する |
|                                                                                                                                        | 浮動小数 2 を取得 | - | Float2 | 関数またはグラフのFloat2値の入力を取得する |
|                                                                                                                                        | 浮動小数 3 を取得 | - | Float3 | 関数またはグラフのFloat3値入力を取得する |
|                                                                                                                                        | 浮動小数 4 を取得 | - | Float4 | 関数またはグラフのFloat4値入力を取得する |
|                                                                                                                                        | ブーリアンを取得 | - | ブーリアン | 関数またはグラフのブール値入力を取得する |
| サンプラ | サンプルグレー | 浮動小数点ベクトル 2 | Float4 | 指定されたUV座標(float2)での入力イメージのグレースケール値を返します。 |
|                                                                                                                                        | カラーをサンプル | 浮動小数点ベクトル 2 | Float4 | 指定されたUV座標(float2)での入力イメージのカラー値を返します。 |
| キャスト | 浮動小数へ | Integer1 | フロート1 | float型の整数を変換します。 |
|                                                                                                                                        | 浮動小数 2 へ | Integer2 | Float2 | Integer2をFloat2に変換します。 |
|                                                                                                                                        | 浮動小数 3へ | Integer3 | Float3 | Integer3をFloat3に変換します。 |
|                                                                                                                                        | 浮動小数 4 へ | Integer4 | Float4 | Float4にInteger4を変換します。 |
|                                                                                                                                        | 整数へ | フロート1 | Integer1 | 浮動小数点数を整数に変換します。 |
|                                                                                                                                        | 整数 2 へ | Float2 | Integer2 | Float2をInteger2に変換します。 |
|                                                                                                                                        | 整数 3 へ | Float3 | Integer3 | Float3をInteger3に変換します。 |
|                                                                                                                                        | 整数 4 へ | Float4 | Integer4 | Float4をInteger4に変換します。 |
| [演算子](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/operator-nodes/operator-nodes.md) | 追加 | ベクトル浮動小数点/整数 | aとbのタイプ | 同じ型の2つの値を加算します： a + b |
|                                                                                                                                        | 減算 | ベクトル浮動小数点/整数 | aとbのタイプ | 同じ型の2つの値を減算する： a - b |
|                                                                                                                                        | 積 | ベクトル浮動小数点/整数 | aとbのタイプ | 同じ型の2つの値を乗算します。 a \* b |
|                                                                                                                                        | スカラー積 | ベクトル実数 | Aの種類 | 値に浮動値を掛ける： \*スカラー |
|                                                                                                                                        | 除算 | Float1/Integer1 | aとbのタイプ | 同じ型の2つの値を除算します： a / b |
|                                                                                                                                        | 符号反転 | Float1/Integer1 | Aの種類 | 負の値を返します。 -a |
|                                                                                                                                        | 剰余 | Float1/Integer1 | Aの種類 | モジュロ値mod(a, divisor)を返します。 |
|                                                                                                                                        | ドット積 | ベクトル実数 | aとbのタイプ | 同じ型の2つの値のドット積を返します。 dot(a, b) |
| [論理](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/logical-nodes/logical-nodes.md) | And | ブーリアン | ブーリアン | 2つのブール値エントリがtrueの場合にtrueを返します。 エントリの1つがfalseの場合はfalseを返します。 |
|                                                                                                                                        | Or | ブーリアン | ブーリアン | 1つのブール型エントリがtrueの場合にtrueを返します。 両方ともfalseの場合はfalseを返します。 |
|                                                                                                                                        | Not | ブーリアン | ブーリアン | エントリの否定のブール値を返します。 !a |
| [比較](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/comparison-nodes/comparison-nodes.md) | 次と等しい | Float1/Integer1 | ブーリアン | a = bの場合はtrueを返します。 |
|                                                                                                                                        | 次と等しくない | Float1/Integer1 | ブーリアン | a != bの場合はtrueを返します。 |
|                                                                                                                                        | より大きい | Float1/Integer1 | ブーリアン | a > bの場合trueを返します。 |
|                                                                                                                                        | 以上 | Float1/Integer1 | ブーリアン | a >= bの場合にtrueを返します。 |
|                                                                                                                                        | より小さい | Float1/Integer1 | ブーリアン | a &lt; bの場合はtrueを返します。 |
|                                                                                                                                        | 以下 | Float1/Integer1 | ブーリアン | a &lt;= bの場合にtrueを返します。 |
| 関数 | 絶対値 | Float1/Integer1 | フロート1 | aの絶対値を返します。 abs(a) |
|                                                                                                                                        | 下限 | Float1/Integer1 | フロート1 | a:floor(a)以下の最大値を返します。 |
|                                                                                                                                        | 天井 | Float1/Integer1 | フロート1 | 最小値の上限aまたは等しいaを返します： ceil(a) |
|                                                                                                                                        | 余弦 | Float1/Integer1 | フロート1 | cos(a)のコサイン値を返します。 |
|                                                                                                                                        | 正弦 | Float1/Integer1 | フロート1 | sin(a)のサイン値を返します。 |
|                                                                                                                                        | 正接 | Float1/Integer1 | フロート1 | tan(a)のタンジェント値を返します |
|                                                                                                                                        | 逆正接 2 | 浮動小数点ベクトル 2 | フロート1 | vector2エントリの円弧tan 2の値を返します。 arctan2(xa, ya) |
|                                                                                                                                        | デカルト | フロート1 | Float2 | 2つの極座標をデカルト座標に変換します： carth(rho, theta) |
|                                                                                                                                        | 平方根 | Float1/Integer1 | フロート1 | 関数の平方根を返す |
|                                                                                                                                        | 対数 | Float1/Integer1 | フロート1 | log(a)の対数値を返します。 |
|                                                                                                                                        | 指数 | Float1/Integer1 | フロート1 | exp(a)の指数値を返します |
|                                                                                                                                        | Pow 2 | Float1/Integer1 | フロート1 | 関数の2乗を返す |
|                                                                                                                                        | リニア補間法 | Float1/Integer1 | フロート1 | 浮動小数点値に応じて、2つの値の間の線形補間を返します。 (1-x)a + x \* b |
|                                                                                                                                        | 最小 | Float1/Integer1 | aとbのタイプ | aからbまでの最小値を返します。 |
|                                                                                                                                        | 最大 | Float1/Integer1 | aとbのタイプ | aとbの間の最大値を返します |
| ランダム |                       | フロート1 | フロート1 | 0 ～ aの範囲で浮動小数値を生成します。 |
| [コントロール](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/control-nodes/control-nodes.md) | 順番 | 任意 | 入力の種類 | 2つの値の間で最初に計算する値を選択できます。 |
|                                                                                                                                        | If...Else | ブール演算式/ a &amp; b | aとbのタイプ | Ifの条件がtrueの場合にtrueを返します。 falseの場合、 falseを返します。 |
