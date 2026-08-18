---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/using-color-management.html"
breadcrumb-title: ''
description: Substance 3D Designer Pythonスクリプティングでカラーマネジメント機能を使用して、正確なカラーを再現する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Using color management
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラーマネジメントの使用
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 0%

---


# カラーマネジメントの使用

<b>SDApplication</b>クラスからアクセスできる<b> SDColorManagementEngine </b>クラスには、*現在のカラーマネジメント設定*&#x200B;に関する情報が含まれています。

## カラーマネジメントエンジンへのアクセスと照会

```
import sd 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

 

## Access the color management engine.

cm = app.getColorManagementEngine() 

 

## Currently getName can return "legacy", "ace" or "ocio"

## depending on the color management settings in the preferences.

cmName = cm.getName()  

print(cmName) 

 

print(cm.getWorkingColorSpaceName()) 

print(cm.getRawColorSpaceName()) 

 

if cmName == "ocio": 

## If OpenColorIO is enabled, print the config file name.

    print(cm.getOCIOConfigFileName()) 

 

## List all color spaces.

colorSpaces = cm.getColorSpaces() 

for cs in colorSpaces: 

    print(cs.get())
```


また、Pythonからビットマップリソースに&#x200B;*カラースペースを割り当てる*&#x200B;こともできます。

### ビットマップリソースのカラースペースの設定

```
import sd 

import sd 

from sd.api.sdproperty import * 

from sd.api.sdresourcebitmap import SDResourceBitmap 

from sd.api.sdvaluestring import SDValueString 

from sd.api.sdvaluebool import SDValueBool 

 

ctx = sd.getContext() 

app = ctx.getSDApplication() 

pkgMgr = app.getPackageMgr() 

cm = app.getColorManagementEngine() 

 

colorSpaces = cm.getColorSpaces() 

 

## Get all the resources in the first package.

pkg = pkgMgr.getPackages()[0] 

resources = pkg.getChildrenResources(isRecursive=True) 

 

for res in resources: 

 if isinstance(res, SDResourceBitmap): 

  props = res.getProperties(SDPropertyCategory.Annotation) 

 

## Print the current color space for the resource.

  p0 = res.getPropertyFromId("bitmap_color_space", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_color_space") 

  print(cs.get()) 

 

## Print the current premultiplied alpha setting for the resource.

  p1 = res.getPropertyFromId("bitmap_premultiplied_alpha", SDPropertyCategory.Annotation) 

  cs = res.getAnnotationPropertyValueFromId("bitmap_premultiplied_alpha") 

  print(cs.get()) 

 

## Assign new values for the color space and premultiplied alpha properties.

  res.setPropertyValue(p0, colorSpaces[2]) 

  res.setPropertyValue(p1, SDValueBool.sNew(False))
```


## カラースペース変換を使用したSDTextureの記述

**SDTexture**&#x200B;クラスの&#x200B;**save**&#x200B;メソッドで、オプションの&#x200B;**outputColorSpace**&#x200B;パラメーターを使用できるようになりました。 指定すると、画像を保存する前にカラースペースの変換が&#x200B;*適用されます*。

カラーマネジメントモードが埋め込みICCプロファイル&#x200B;*および*&#x200B;をサポートしている場合、出力先のファイル形式もそれらをサポートしているため、カラースペースICCプロファイルは&#x200B;*結果の画像ファイルに埋め込まれます*。
