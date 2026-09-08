---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/variables/create-a-variable.html"
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
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---


# 変数の作成

Substance 3D Designerで変数を作成するには、いくつかの方法があります。

* 入力パラメーターの使用
* Setノードを使用します。

## 入力パラメーターの使用

変数を作成すると、入力パラメーターが作成され、それに関連付けられます。 この変数は、グラフの任意の関数で再利用できます。

したがって、1つの表示されるパラメーターがグラフの複数の部分に影響を与える可能性があります。

## Setノードの使用

Setノードは、関数グラフでのみ使用できるノードです。

これにより、ユーザーはカスタム変数を作成できます。

* 名前はパラメーターで宣言されます。
* 値は入力によって定義されます。

### *Set*&#x200B;ノードの使用方法

Setノードの使用は少し特殊です。

宣言すると、グラフ内でだけ有効になります。デフォルトでは実際には役に立ちません（つまり、その値はすでにリンク付きで出力できます）。

したがって、このグラフ以外でこの新しい変数を宣言する必要があります。

これを行うには、シーケンスノードを使用して、次の手順を実行する必要があります。

* 実際の出力ノードをシーケンスノードの「最後の」入力にリンクします
* 設定ノードをシーケンスノードの「In」入力にリンクします。
* シーケンスを出力ノードとして設定します

この操作を行うと、同じノードの別の関数グラフで変数を使用できるようになります。

>[!WARNING]
>
> ノードがSubstance エンジンによって処理されると、それらのパラメーター（およびそれらを制御できる関数）が上から下に読み取られます。 したがって、Setノードにアクセスできるのは、node parameters スタックーでその下に配置されているパラメータだけです。

>[!NOTE]
>
> 作成する変数が複数ある場合は、*Set*&#x200B;と&#x200B;*Sequence*&#x200B;のノード作成操作を繰り返し、最後のシーケンスノードを出力ノードとして設定します。
> 
> ![](../../../assets/image2015-12-18-18-43-8.png)
