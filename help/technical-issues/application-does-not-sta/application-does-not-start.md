---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/technical-issues/application-does-not-start.html"
breadcrumb-title: ''
description: Substance 3D Designerを起動できない問題のトラブルシューティングを行い、アプリケーションを起動する方法を確認します。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Application does not start
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: アプリケーションが起動しない
user-guide-description: ''
user-guide-title: ''
source-git-commit: 734525cdd187aac666168f8a9e1f9e49f3dad03e
workflow-type: tm+mt
source-wordcount: '828'
ht-degree: 1%

---


# アプリケーションが起動しない

このページでは、Substance 3D Designerが正常に起動しない一般的な原因の一覧を示し、各トラブルシューティング手順をオペレーティングシステム別に分類しています。

[Designer 15.0以降](#version-15-0)

[Windows 10/11](#windows-10-11)

[Windows 7/8/8.1](#windows-7-8)

[Linux](#linux)

## Designer 15.0以降

<b>![（エラー）](application-does-not-start.resources/error.svg)問題</b>

統合GPU(iGPU)とディスクリートGPU(dGPU)の両方を搭載したシステムで、バージョン15.0以降のDesignerを起動できない。

<b>![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ</b>

iGPUのグラフィックドライバーを更新します。 最新のドライバーは、次の場所で確認できます： [Intel](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)  | [AMD](https://www.amd.com/en/support/download/drivers.html)

## Windows 10/11

**![（エラー）](application-does-not-start.resources/error.svg)問題**

Windows 10またはWindows 11を使用しているシステムでSubstance 3D Designerを起動できない。

**![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ**

ライセンス検証プロセスで&#x200B;*古い* `libeay32.dll`ライブラリが使用されているため、古いバージョンのDesignerをWindows 10またはWindows 11で開始できない場合があります。

次の手順に従って、ライブラリを&#x200B;*更新されたバージョン*&#x200B;に置き換えることができます。たとえば、[ここ](https://support.networkoptix.com/hc/en-us/articles/115015730007-Nx-Software-crashes-due-to-libeay32-dll-on-Windows) （32ビットWindows用にファイルを選択）で配布されたバージョンなどです。

1. Designerのインストールディレクトリで`libeay32.dll`ファイルを探します
1. 後で復元する必要がある場合は、ファイルを安全な場所にバックアップします
1. 更新されたバージョンでファイルを置換する
1. Designerを開始

>[!WARNING]
>
> サポートされていない設定
> 
> Windows 10はサポートされていません。 詳しくは、[必要システム構成](../../getting-started/system-requirements/system-requirements.md)ページをご覧ください。
> 
> メンテナンス期間が終了しているバージョンのDesignerはサポートされていません。 これらのバージョンは、OSのアップグレードなど、システムに対して大幅な変更が行われた場合、確実に実行できなくなる可能性があります。

## Windows 7/8/8.1

**![（エラー）](application-does-not-start.resources/error.svg)問題**

Windows 7、Windows 8またはWindows 8.1を使用しているシステムでSubstance 3D Designerを起動できない。

**![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ**

バージョン&#x200B;**11.3.0**&#x200B;の更新プログラムの一部として、複数のライブラリ、ツール、およびSDKがアップグレードされました。*互換性が壊れました* Windows 10より前のバージョンのWindowsです。

Microsoft自体は、メインストリーム向けに以前のバージョンのWindowsをサポートしなくなったため、*強く* Windows 10にアップグレードすることをお勧めします（[ここ](https://www.microsoft.com/en-us/windows/windows-7-end-of-life-support-information)および[ここ](https://docs.microsoft.com/en-us/lifecycle/faq/windows#windows-8.1)を参照）。 したがって、これらのバージョンを引き続き使用すると、*セキュリティの問題*&#x200B;が発生します。\
Windows 10にアップグレードできない場合は、Designer *過去*&#x200B;バージョン&#x200B;**11.2.2**&#x200B;のインストールを&#x200B;*更新しない*&#x200B;でください。

>[!WARNING]
>
> サポートされていない設定
> 
> 注意： Windows 7、Windows 8、およびWindows 8.1は&#x200B;*正式にはサポートされていません*。 詳しくは、[必要システム構成](../../getting-started/system-requirements/system-requirements.md)ページをご覧ください。

## Linux

<b>![（エラー）](application-does-not-start.resources/error.svg)問題</b>

ホーム画面を閉じてメインウィンドウを表示しているときにクラッシュが発生しました。

<b>![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ</b>

Designerは、システムの<b>libffi.so</b>ライブラリを読み込むため、Pythonコンポーネントを読み込めません。

Designerが独自のライブラリを読み込むようにするには、Designerのインストールディレクトリで次のコマンドを使用し、`%command%`をDesignerを実行するコマンドに置き換えます。

```
LD_PRELOAD=./plugins/pythonsdk/lib/python3.11/lib-dynload/libffi.so.6 %command%
```


Pythonのバージョン番号は、実行するDesignerのバージョンによって異なります。

* 14.0.0より前： python3.9
* 12.1.0より前： python3.7

+++Steam起動オプション
SteamからDesignerを起動するLinuxをご利用のお客様は、以下に示すように、Designerの起動オプションでLD\_PRELOADコマンドを設定できます。

これが完了すると、以降のすべてのセッションでDesignerがSteamから正常に起動する可能性があります。

![Steamの起動オプション](application-does-not-start.resources/steam_linux_launch_option.jpg "Steamの起動オプション")



+++

**![（エラー）](application-does-not-start.resources/error.svg)問題**

SteamエディションのDesignerはで始まることができず、エラーメッセージは表示されません。

**![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ**

代わりにSteamアプリケーションをログに記録すると、エラーメッセージを取得できます。

[こちら](https://github.com/ValveSoftware/steam-for-linux/issues/7114#issuecomment-629634260)をお勧めします。Steamを完全に閉じてから、ターミナルから次のコマンドを実行してください（またはこのコマンドのショートカットを作成します）:

```
steam 2>&1 | tee /path/to/logfile
```


<b>![（エラー）](application-does-not-start.resources/error.svg) Issu</b><b>e</b>

`<b>xcb</b>`プラグインを読み込めません。 コマンドラインに次のメッセージが表示されます。

```
qt.qpa.plugin: Could not load the Qt platform plugin "xcb" in "" even though it was found. 

This application failed to start because no Qt platform plugin could be initialized. Reinstalling the application may fix this problem. 

 

Available platform plugins are: minimal, offscreen, xcb. 

 

Aborted (core dumped)
```


**![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ**

必要なパッケージの一部が見つかりません。 Designerインストールディレクトリから次のコマンドを実行します。

```
ldd libQt5XcbQpa.so.5
```


印刷された一覧で`not found`として報告されたパッケージを確認し、これらの不足している各パッケージに対して次のコマンドを実行してください：

```
apt-get install <package-name>
```


E.g.

```
apt-get install libxcb-xinput0
```


<b>![（エラー）](application-does-not-start.resources/error.svg)問題</b>

Designerの起動時に次のエラーが発生します。

```
error while loading shared libraries: libcrypt.so.1: cannot open shared object file: No such file or directory
```


Designerによって読み込まれたシステムライブラリは、Designer独自の<b>libcrypto.so.1.1</b>ライブラリと互換性がありません。

<b>![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ</b>

Designerのインストールディレクトリから<b>`libcrypto.so.1.1`</b>ライブラリを削除して、代わりにシステムのライブラリが使用されるようにします。

>[!NOTE]
>
> この回避策は、システムに独自のlibcrypto.so.1ライブラリがある場合にのみ動作します。 最近のディストリビューションでは、<b>libxcrypt-compat</b>などの互換性パッケージをインストールする必要がある場合があります。

<b>![（エラー）](application-does-not-start.resources/error.svg)問題</b>

Substance 3D Designerは、Linuxの&#x200B;*Archベース*&#x200B;のディストリビューションを使用しているシステムでは起動できません。

**![（ティック）](application-does-not-start.resources/check.svg)推奨ステップ&#x200B;*(![（警告）](application-does-not-start.resources/warning.svg)不安定、AMD GPUのみ！)***

**progl** （[AMDGPU-PRO](https://wiki.archlinux.org/title/AMDGPU_PRO)ドライバーの一部）をインストールして、Designerを起動してみてください。 これは、アプリケーション起動コマンドで`progl`プレフィックスを使用して実行できます。

```
progl <designer-application-path>
```


`progl`が不安定になる可能性があることに注意してください。 このため、*最後の手段*&#x200B;として試行する必要があります。

>[!WARNING]
>
> ArchベースのLinuxディストリビューションは&#x200B;*サポートされていません*&#x200B;ことに注意してください。 詳しくは、[必要システム構成](../../getting-started/system-requirements/system-requirements.md)ページをご覧ください。
