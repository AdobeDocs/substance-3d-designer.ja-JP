---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/plugin-basics.html"
breadcrumb-title: ''
description: Substance 3D Designer用のPythonプラグインを作成してアプリケーションの機能を拡張する方法の基本を説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin basics
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: プラグインの基本
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '95'
ht-degree: 0%

---


# プラグインの基本

プラグインは、<b>initializeSDPlugin()</b>関数を定義するPythonファイルまたはPythonモジュールです。

プラグインの読み込み時に<b>initializeSDPlugin()</b>関数が呼び出されます。\
この関数では、ユーザインタフェース要素を作成したり、コールバックを登録したり、その他の必要な機能を使用することができます。

オプションで、プラグインは、プラグインがアンロードされたときに呼び出される<b>uninitializeSDPlugin()</b>関数を定義できます。\
この関数を使用すると、リソースを解放したり、ネットワーク接続を閉じたりすることができます。

```
## Plugin entry point. Called by Designer when loading a plugin.

def initializeSDPlugin(): 

 print("Hello!") 

 

## If this function is present in your plugin,

## it will be called by Designer when unloading the plugin.

def uninitializeSDPlugin(): 

 print("Bye!")
```
