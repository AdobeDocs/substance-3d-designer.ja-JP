---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables.html"
breadcrumb-title: ''
description: Substance 3D Designer関数グラフで変数を使用して、値を効率的に保存および再利用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 変数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 1%

---


# 変数

>[!NOTE]
>
> 変数ノードの作成および使用方法の詳細については、*[変数ノードセクション](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)*&#x200B;を参照してください。

## 定義

プログラミングの知識が少なければ、変数の概念に精通しているかもしれません。

そうでない場合は、次のように簡単に定義します。

>[!NOTE]
>
> 変数は、値を含む特定の名前を持つ単なる「コンテナ」です。
> 
> 変数に含まれている値を名前を付けて呼び出すことで、その値を使用できます。

## 変数の種類

Substance 3D Designerには、NumericsとBooleansという2種類の変数があります。

## 数値変数

数値変数は基本的に数値です。 でも、ここでは2種類の数字をはっきりと区別する。

* 整数： 0 | 1 | -1 | 203568など…
* フロート： 0.23 | 1.0 | -0.3546 |など

>[!WARNING]
>
> Designerでは、整数とフロートを明確に区別しています。デフォルトでは一緒に操作できません。
> 
> 幸いなことに、*To Integer*&#x200B;またはTo Floatノードを使用して、型変換を実行できます。

### 同じ変数に複数の数値が含まれている

必要に応じて、同じ変数内に最大4つの数値を累積できます。

ここでも、すべての値は同じ型からのものである必要があります。

そのためには、次のいずれかの数値を選択します。

![](variables.resources/variables-01.png)

## ブーリアン

ブール値は純粋なバイナリ値です。つまり、値は&#x200B;*True*&#x200B;または&#x200B;*False*&#x200B;である必要があります（0または1と言うこともできます）。
