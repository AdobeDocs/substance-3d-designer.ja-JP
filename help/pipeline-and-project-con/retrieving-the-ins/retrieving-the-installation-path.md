---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/retrieving-the-installation-path.html"
breadcrumb-title: ''
description: スクリプト作成や自動処理のためにSubstance 3D Designerのインストールパスを取得する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Retrieving the installation path
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: インストールパスの取得
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '282'
ht-degree: 8%

---


# インストールパスの取得

バージョンとプラットフォームに応じて、[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)のインストールパスを取得する方法について説明します。

## Windows

### Creative Cloud デスクトップ

1. <b>Windowsレジストリエディター</b> (regedit)を開きます
1. 次のレジストリキーに移動します： <b>HKEY\_LOCAL\_MACHINE\Software\Microsoft\Windows\CurrentVersion\App Paths\&lt;/b>
1. <b>Adobe Substance 3D Designer.exe</b>というサブキーを開きます
1. キーの値には、インストールされているアプリケーションの実行可能ファイルへのパスが含まれています

>[!NOTE]
>
> このレジストリキーは、バージョン11.2以降でのみ使用できます。\
> 古いバージョンの場合、インストールパスは、 HKEY\_CURRENT\_USER\Software\Microsoft\Windows\CurrentVersion\ Explorer\FileExtsのファイル関連付けから取得できます

### Substance版（スタンドアロン）

1. <b>Windowsレジストリエディター</b> (regedit)を開きます
1. レジストリキー<b>HKEY\_LOCAL\_MACHINE\ SOFTWARE\Microsoft\Windows\CurrentVersion\Uninstall</b>に移動します
1. アプリケーションバージョンの<b>AppID</b>に一致するサブキーを検索します（以下の表を参照）
1. キーの値には、アプリケーションのインストール場所へのパスが含まれています

| バージョン | AppId |
| --- | --- |
| **バージョン5.x** | {25E7D16D-1FBA-49EA-BF36-E2D6B20A9206} |
| **バージョン6.x** | {09a302b1-8da8-4f62-b0cb-a208faa210f9} |
| **バージョン7.x (2017.x)から11.1** | {e9e3d6d9-3023-41c7-b223-11d8fdd691b9} |
| **バージョン11.2以降** | {662bb79f-5616-44e6-a84d-b3d6abebe002} |

### Steam 版

アプリケーションは、Steamインストールフォルダーのsteamapps/common/サブフォルダーにインストールされます。

## macOS

Macでは、アプリケーションは次の場所にインストールされます。

| バージョン | パス |
| --- | --- |
| **11.2以降** | **/Applications/Adobe Substance 3D Designer.app** |
| **レガシ** | **/Applications/Substance Designer.app** |

## Linux

Linuxでは、rpmパッケージは次のパスにインストールされています。

| バージョン | パス |
| --- | --- |
| **11.2以降** | **/opt/Adobe/Adobe\_Substance\_3D\_Designer** |
| **レガシ** | **/opt/Allegorithmic/Substance\_Designer** |
