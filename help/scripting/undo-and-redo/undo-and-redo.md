---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/undo-and-redo.html"
breadcrumb-title: ''
description: Substance 3D Designer Pythonスクリプトでユーザーのアクションを取り消したり、やり直したりする機能を実装する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Undo and redo
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 取り消しとやり直し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '71'
ht-degree: 0%

---


# 取り消しとやり直し

<b>SDHistoryUtils.UndoGroup</b>クラスを使用すると、ユーザーは1つのコマンドですべてのアクションを&#x200B;*取り消しまたはやり直し*&#x200B;するために、*アクションをグループ化*&#x200B;できます。

これらのグループは、ユーザーによって&#x200B;*名前*&#x200B;が付けられ、ユーザーインターフェイスの取り消し/やり直しリストにその名前で表示されます。  これにより、多数のアクションを管理しやすくなります。

```
import sd 

from sd.api.sdhistoryutils import * 

 

## Get the application and package manager objects.

cxt = sd.getContext() 

app = cxt.getSDApplication() 

pkgMgr = app.getPackageMgr() 

 

## Group one or more changes into an undo group.

with SDHistoryUtils.UndoGroup("My Undo Group"): 

## Create two new packages.

    pkgMgr.newUserPackage() 

    pkgMgr.newUserPackage()
```
