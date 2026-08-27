---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/accessing-graphs-and-selections.html"
breadcrumb-title: ''
description: Substance 3D Designer Pythonスクリプトでグラフやノード選択にアクセスし、操作する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Accessing graphs and selections
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラフと選択範囲へのアクセス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '86'
ht-degree: 0%

---


# グラフと選択範囲へのアクセス

<b>SDApplication</b>クラスには、*現在アクティブ*&#x200B;グラフとその中の&#x200B;*現在の選択範囲*&#x200B;にアクセスできる便利なメソッドが含まれています。

```
import sd 

 

## Get the application and UI manager object.

ctx = sd.getContext() 

app = ctx.getSDApplication() 

uiMgr = app.getQtForPythonUIMgr() 

 

## Get the current graph.

g = uiMgr.getCurrentGraph() 

print("The current graph is %s" % g) 

 

## Get the currently selected nodes.

selection = uiMgr.getCurrentGraphSelectedNodes() 

for node in selection: 

 print("Node %s" % node)
```


*特定の*&#x200B;グラフビューで表示されているグラフには、<b>graphViewID</b>を使用してアクセスできます。

この方法は、カスタムグラフビューツールバーを作成する場合に便利です。 詳細については、「[ユーザーインターフェイス要素の作成](../../scripting/creating-user-interface/creating-user-interface-elements.md)」の章の<b>グラフビューのツールバーの作成</b>の例を参照してください。
