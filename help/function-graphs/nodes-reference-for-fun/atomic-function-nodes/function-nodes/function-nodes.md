---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/atomic-function-nodes/function-nodes.html"
breadcrumb-title: ''
description: Substance 3D Designer関数グラフの関数ノードにアクセスして、カスタム関数グラフを呼び出して実行します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 関数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '451'
ht-degree: 5%

---


# 関数ノード

関数ノードは、入力値を表す数学関数に従って変形します。

これらの入力コネクターは通常は入力されませんが、すべての値の型をサポートしているわけではありません。

## ノードリスト

+++Pow
![Powノードアイコン](../../../../assets/Pow_Node.jpg "Powノードアイコン")



2番目の入力の累乗で累乗された最初の入力を返します： <b>X^Y</b>。

+++

+++2Pow
![2Powノードアイコン](../../../../assets/2Pow_Node.jpg "2Powノードアイコン")



入力値<b>2^X</b>のべき乗に2を返します。

+++

+++平方根
![平方根ノードアイコン](../../../../assets/SquareRoot_Node.jpg "平方根ノードアイコン")



入力値<b>√X</b>の平方根を返します。

+++

+++指数
![指数ノードアイコン](../../../../assets/Exponential_Node.jpg "指数ノードアイコン")



入力値の指数値を返します： <b>e^X</b>

<b>e</b>は約2.7182818と等しくなります。

+++

+++対数
![対数ノードアイコン](../../../../assets/Logarithm_Node.jpg "対数ノードアイコン")



入力値<b>ln(X)</b>の自然対数を返します。

+++

+++対数の底 2
![対数ベース2ノードアイコン](../../../../assets/LogarithmBase2_Node.jpg "対数ベース2ノードアイコン")



入力値<b>log2(X)</b>の底2の対数を返します。

+++

+++絶対値
![絶対ノードアイコン](../../../../assets/Absolute_Node.jpg "絶対ノードアイコン")



入力の絶対値を返します： <b>abs(X)</b>。

+++

+++天井
![Ceilノードアイコン](../../../../assets/Ceil_Node.jpg "Ceilノードアイコン")



入力値を切り上げます。 X以上の最小の整数値を返します： <b>ceil(X)</b>。

+++

+++下限
![下限ノードアイコン](../../../../assets/Floor_Node.jpg "下限ノードアイコン")



入力値を切り捨てます。 X以下の最大整数値を返します： <b>floor(X)</b>。

+++

+++リニア補間
![リニア補間ノードアイコン](../../../../assets/LinearInterpolation_Node.jpg "リニア補間ノードアイコン")



浮動値の関数で2つの値の間の線形補間を返します： <b>(1 - X)\*A + X\*B</b>

+++

+++最小
![最小ノードアイコン](../../../../assets/Minimum_Node.jpg "最小ノードアイコン")



次の2つの入力値のうち最小値を返します： <b>min(A, B)</b>。

+++

+++最大
![最大ノードアイコン](../../../../assets/Maximum_Node.jpg "最大ノードアイコン")



次の2つの入力値のうち最も高い値を返します： <b>max(A, B)</b>。

+++

+++余弦
![コサインノードアイコン](../../../../assets/Cosine_Node.jpg "コサインノードアイコン")



入力値のコサインをラジアンで返します： <b>cos(X)</b>。

+++

+++正弦
![サインノードアイコン](../../../../assets/Sine_Node.jpg "サインノードアイコン")



入力値のサインをラジアンで返します： <b>sin(X)</b>。

+++

+++正接
![接線ノードアイコン](../../../../assets/Tangent_Node.jpg "接線ノードアイコン")



入力値のタンジェントをラジアンで返します： <b>tan(X)</b>。

+++

+++逆正接 2
![Arc Tangent 2ノードアイコン](../../../../assets/ArcTangent2_Node.jpg "Arc Tangent 2ノードアイコン")



入力された2Dベクトルと水平間の角度を返します。

<b>デカルト関数</b>の逆数です。

通常の<b>atan2</b>関数のように、入力ベクトルのX成分とY成分を切り替える必要はありません。

+++

+++デカルト
![絶対ノードアイコン](../../../../assets/Absolute_Node.jpg "絶対ノードアイコン")



極座標を直交座標に変換します。

<b>Arc tangent 2 </b>関数の逆数です： <b>Length \* Float2(cos(Angle), sin(Angle).</b>

極座標は原点からの距離で、水平からの角度はラジアンです。

+++

+++ランダム
![ランダムノードアイコン](../../../../assets/Random_Node.jpg "ランダムノードアイコン")



0から入力値<b>X</b>までの間のランダムな値を返します。

+++
