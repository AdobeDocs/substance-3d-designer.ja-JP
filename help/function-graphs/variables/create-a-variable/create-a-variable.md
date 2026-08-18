---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/function-graphs/variables/create-a-variable.html"
breadcrumb-title: ''
description: 再利用可能な値やパラメーターを使用するために、Substance 3D Designer関数グラフでカスタム変数を作成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Variables > Create a variable
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 変数の作成
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# 変数の作成

Substance 3D Designerで変数を作成するには、いくつかの方法があります。

* 入力パラメーターの使用
* Setノードを使用します。

## 入力パラメーターの使用

入力パラメーターを作成すると、変数が作成され、それに関連付けられます。 この変数は、グラフの任意の関数で再利用できます。

そのため、1つの公開パラメーターが、グラフの複数の部分に影響を与える可能性があります。

## Setノードの使用

セットノードは、関数グラフでのみ使用できるノードです。

これにより、ユーザーはカスタム変数を作成できます。

* 名前はパラメーターで宣言されます。
* 値は入力によって定義されます。

### *Set*&#x200B;ノードの使用方法

Setノードの使用は少し特殊です。

これを宣言すると、グラフ内でのみ使用可能になります。デフォルトでは実際には役に立ちません（つまり、その値はすでにリンクで出力できます）。

したがって、このグラフの外側でこの新しい変数を宣言する必要があります。

これを行うには、シーケンスノードを使用して、次の手順を実行する必要があります。

* 実際の出力ノードをシーケンスノードの「最後の」入力にリンクします
* 設定ノードをシーケンスノードの「In」入力にリンクします。
* シーケンスを出力ノードとして設定します

これを行うと、変数は同じノードの別の関数グラフで使用できるようになります。

>[!WARNING]
>
> ノードがSubstance Engineで処理されると、そのパラメーター（およびノードを制御できる関数）が上から下に読み上げられます。 したがって、Setノードにアクセスできるのは、ノードパラメータスタックでその下に配置されているパラメータだけです。

>[!NOTE]
>
> 作成する変数が複数ある場合は、*Set*&#x200B;と&#x200B;*Sequence*&#x200B;のノード作成操作を繰り返し、最後のシーケンスノードを出力ノードとして設定します。
> 
> ![](../../../assets/image2015-12-18-18-43-8.png)
