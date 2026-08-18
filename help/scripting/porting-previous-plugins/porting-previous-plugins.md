---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/porting-previous-plugins.html"
breadcrumb-title: ''
description: 以前のバージョンのSubstance Designerのプラグインを現在のPython APIに移植する方法を説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Porting previous plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 以前のプラグインの移植
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '193'
ht-degree: 0%

---


# 以前のプラグインの移植

Python用Qtをサポートするために行われた変更のため、**以前のプラグインは動作しなくなります**。\
特に、次のことに注意してください。

## プラグインのロードとアンロード

アプリケーション<b>の開始時</b>にプラグインが読み込まれ、<b>終了時</b>にアンロードされるようになりました。\
そのため、プラグインが&#39;*sdplugins.Plugin*&#39;から継承する必要はありません&#x200B;**。

詳細については、[プラグインの基本](../../scripting/plugin-basics/plugin-basics.md)のセクションを確認してください。

## ユーザーインターフェイス要素の作成

プラグイン&#x200B;*は、&#39;* sdplugins.PluginDesc *&#39;を定義する必要はありません*。\
代わりに、プラグインは<b>個の新しい[UI manager](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/scripting-api-next-172825023.html)オブジェクト</b>と<b>Qt for Python</b>を使用して、必要なユーザーインターフェイス要素を作成できます。

小さなコードサンプルは、[ユーザーインターフェイス要素の作成](../../scripting/creating-user-interface/creating-user-interface-elements.md)セクションにあります。

## 場所コンテキストの使用の置換

&#39;*SDLocationContext*&#39;クラスがPython APIから&#x200B;*削除*&#x200B;されました。\
プラグインは<b>[UI manager](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/scripting-api-next-172825023.html)オブジェクト</b>を使用して、現在アクティブなグラフと選択範囲にアクセスできます。

[グラフや選択範囲へのアクセス](../../scripting/accessing-graphs-and-sel/accessing-graphs-and-selections.md)セクションで例を見つけることができます。
