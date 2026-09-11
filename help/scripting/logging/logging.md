---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/logging.html"
breadcrumb-title: ''
description: Substance 3D Designer Pythonプラグインでログを使用してデバッグやモニタリングを行う方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Logging
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ログ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '44'
ht-degree: 4%

---


# ログ

ロギングには標準のPythonのloggingモジュールを使用することをお勧めします。

<b>sd</b>モジュールには、Designerのコンソールにログをリダイレクトするためのヘルパークラスが含まれています。

## Designerのコンソールパネルへのログイン

```
import logging 

import sd 

 

 

## Create a logger.

logger = logging.getLogger("MyLogger") 

 

 

## Add a handler to redirect logging to Designer's console panel.

ctx = sd.getContext() 

logger.addHandler(ctx.createRuntimeLogHandler()) 

 

 

## Do not propagate log messages to Python's root logger.

logger.propagate = False 

 

 

## Set the default log level if needed.

logger.setLevel(logging.DEBUG) 

 

 

## Use the logger

logger.info("Info message") 

logger.warning("Warning message") 

logger.error("Error message")
```
