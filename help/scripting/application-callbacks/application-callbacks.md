---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/application-callbacks.html"
breadcrumb-title: ''
description: Substance 3D Designer Pythonプラグインでアプリケーションコールバックを使用して、アプリケーションイベントに応答する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Application callbacks
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: アプリケーションコールバック
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '65'
ht-degree: 0%

---


# アプリケーションコールバック

特定のイベントが発生したときにDesignerが呼び出すApplicationオブジェクトに、<b>Pythonコールバック</b>を登録できます。

メニューやボタンなどのユーザーインターフェイスオブジェクトは、<b>Qt for Python</b>ライブラリを使用してコールバックをトリガーできます。 詳細については、[ユーザーインターフェイス要素の作成](../../scripting/creating-user-interface/creating-user-interface-elements.md)を参照してください。

```
import sd 

 

## Our callbacks.

def onBeforeFileLoadedCallback(filePath): 

    print("Before file loaded, file: %s" % filePath) 

 

def onAfterFileLoadedCallback(filePath, succeed, updated): 

    print("After file loaded, file: %s, succeed: %s, updated: %s" % (filePath, succeed, updated)) 

     

def onBeforeFileSavedCallback(filePath, parentPackagePath): 

    print("Before file saved, file: %s, parentPackage: %s" % (filePath, parentPackagePath)) 

 

def onAfterFileSavedCallback(filePath, succeed): 

    print("After file saved, file: %s, succeed: %s" % (filePath, succeed)) 

 

## Get the application.

app = sd.getContext().getSDApplication() 

 

## Register our callbacks.

beforeFileLoadedCallbackID = app.registerBeforeFileLoadedCallback(onBeforeFileLoadedCallback) 

afterFileLoadedCallbackID = app.registerAfterFileLoadedCallback(onAfterFileLoadedCallback) 

beforeFileSavedCallbackID = app.registerBeforeFileSavedCallback(onBeforeFileSavedCallback) 

afterFileSavedCallbackID = app.registerAfterFileSavedCallback(onAfterFileSavedCallback) 

 

## Unregister callbacks when no longer needed.

app.unregisterCallback(beforeFileLoadedCallbackID) 

app.unregisterCallback(afterFileLoadedCallbackID) 

app.unregisterCallback(beforeFileSavedCallbackID) 

app.unregisterCallback(afterFileSavedCallbackID)
```
