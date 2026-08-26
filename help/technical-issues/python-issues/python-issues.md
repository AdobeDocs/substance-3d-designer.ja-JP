---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/python-issues.html"
breadcrumb-title: ''
description: プラグインやAPIの問題など、Substance 3D DesignerでのPythonスクリプト作成に関する問題をトラブルシューティングします。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Python issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Pythonの問題
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 0%

---


# Pythonの問題

このページでは、Substance 3D Designerの[Python API](../../scripting/scripting.md)に関する技術的な問題とPythonで実装されている機能を一覧表示し、それぞれのトラブルシューティング手順を示します。

Pythonで実装されている機能には、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)のツールバーにある[Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[送信先](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)のアクションや、グラフの未使用のノードを削除するツールがあります。

## &#39;QtForPython&#39;モジュールのロードに失敗します

<b>![（エラー）](../../assets/error.svg)問題</b>

&#39;QtForPython&#39; Pythonモジュールの読み込みに失敗します。これにより、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)のツールバーにある[Publish](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)/[送信先](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)のアクションや、グラフの未使用のノードを削除するツールなど、Pythonで実装されている機能が見つからなくなります。

さらに、多くの[Pythonプラグイン](../../scripting/plugin-basics/plugin-basics.md)が読み込みに失敗したり、予期したとおりに動作しなくなったりします。

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

DesignerのQtForPythonのインストールとその依存関係、およびシステム上の既存のインストールとの間に競合が発生している可能性があります。

[QtForPython](https://doc.qt.io/qtforpython-5/index.html) ([PySide2](https://pypi.org/project/PySide2/))と[Shiboken2](https://pypi.org/project/shiboken2/)の他のシステムインストールを削除します。

または、QtForPythonをシステム全体にインストールする代わりに、Python *仮想環境*&#x200B;や&#x200B;*パッケージマネージャー* （[rez](https://github.com/AcademySoftwareFoundation/rez)など）を使用することもできます。
