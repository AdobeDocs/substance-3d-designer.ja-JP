---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/cannot-create-load-a-project.html"
breadcrumb-title: ''
description: Substance 3D Designerでのプロジェクトの作成または読み込みに関する問題をトラブルシューティングして、解決策を見つけます。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Cannot createload a project
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: プロジェクトを作成できません
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '1105'
ht-degree: 0%

---


# プロジェクトを作成できない／読み込めない

Substance 3D Designerでプロジェクトを作成または読み込めない一般的な原因とそのトラブルシューティング手順を示します。

## アプリケーションが古すぎるため、URLを開けません

**![（エラー）](../../assets/error.svg)問題**

**Substance 3Dファイル(SBS)**&#x200B;は、*そのフォーマットをサポートしていない* Substance 3D Designerのバージョンで読み込まれています。 Substance 3Dファイルは、更新されたフォーマットを使用する&#x200B;*新しいバージョン*&#x200B;で保存されている可能性があります。

**![（ティック）](../../assets/check.svg)推奨ステップ**

Substance 3D Designerの進化に伴い、Substance 3Dファイルフォーマット(SBS)も進化します。 多くの場合、ソフトウェアの新しいバージョンは、最新機能をサポートできるように&#x200B;*ファイルを更新*&#x200B;する必要があります。

新しいバージョンで&#x200B;*初めてファイルを読み込む*&#x200B;ときに、この更新を実行するように&#x200B;*プロンプト*&#x200B;が表示されます。

>[!WARNING]
>
> 更新プログラムが適用された&#x200B;*後*&#x200B;にファイルを保存すると、形式のバージョンも変更されます。 この時点で、Substance 3D Designerの&#x200B;*以前のバージョン*&#x200B;に読み込むことはできません。
> 
> この制限は、[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)にも適用されます。

まず、現在のライセンスで許可されている最新バージョンのSubstance 3D Designerを使用していることを確認します。 各エディションのアップデートには、以下のアクセスポイントがあります。

* <b>AdobeのSubstance 3Dサブスクリプション：</b> [Adobe Creative Cloudデスクトップ](https://creativecloud.adobe.com/en/apps/download/creative-cloud)アプリケーションの[アプリ]タブの[更新]セクションに移動します
* <b>[Substance3d.com](http://Substance3d.com)サブスクリプション:</b> Substance 3D Designerでプロンプトが表示されたら更新するか、[Substance3d.com](http://substance3d.com) webサイトの[ライセンス](https://store.substance3d.com/user)セクションで最新のインストーラーをダウンロードします
* <b>Steam:</b>アプリケーションは既定で自動更新されます。 Substance 3D Designerを起動するか、ダウンロード画面に移動して、手動でアップデートをトリガーできます

>[!WARNING]
>
> 更新されたファイルを保存&#x200B;*する前に、以前のバージョンのSubstance 3D Designer*&#x200B;でファイルを読み込む必要がないことを確認してください。
> 
> または、新しいバージョンのSubstance 3D Designerに読み込む&#x200B;*前に、ファイルの*&#x200B;コピー&#x200B;*を作成することができます。そのため、以前のバージョンのソフトウェアを使用する必要がある場合は、常に1つのファイルに戻ることができます。*

## プロジェクトの作成または読み込み中のクラッシュ

<b>![（エラー）](../../assets/error.svg)問題</b>

プロジェクトの作成または読み込み中にクラッシュが発生する場合は、ワークスペースの設定中に[3D ビュー](../../interface/3d-view/3d-view.md)を初期化しているときにエラーが発生することがあります。

システムがラップトップの場合、サードパーティ製のアプリケーションによって&#x200B;*電源管理プラン*&#x200B;が適用され、システムのGPUが3D ビューで使用できなくなることがあります。 その代わりに他のGPUデバイスで処理を実行できない場合は、クラッシュが発生する可能性があります。

*表示設定またはスケーリング*&#x200B;がセッション間で変更され、3D ビューレンダリングフレームが無効な座標で作成された場合にも、クラッシュが発生する可能性があります。

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

このクラッシュの考えられる原因が複数あることを考えると、次のトラブルシューティング手順を順番に実行することをお勧めします。

グラフィックドライバーの更新

まず、グラフィックドライバーが最新であることを確認します。 ご使用のGPUの最新バージョンは、[こちら](https://www.nvidia.com/Download/index.aspx?lang=en-us) (NVIDIA)、[こちら](https://www.amd.com/en/support) (AMD)または[こちら](https://downloadcenter.intel.com/product/80939/Graphics-Drivers) (Intel)で確認できます。

最高のパフォーマンスを強制

システムの&#x200B;*電源プラン*&#x200B;を管理するソフトウェア（ASUS Armory Crateなど）を探します。特にラップトップの場合に便利です。

一部の電源管理アプリケーションは、システムのGPUへの他のアプリケーションのアクセスを制限したり、GPUのパフォーマンスを妨げたりすることがあり、その結果クラッシュが発生する場合があります。 電源管理アプリケーションが存在し、アクティブである場合は、最高のパフォーマンスを実現するプランに切り替えます。

ディスクリートGPUを使用する

お使いのシステムに&#x200B;*切り替え可能なグラフィック*&#x200B;が搭載されている場合は、Substance 3Dアプリケーション用にディスクリートGPU(dGPU)の使用を強制することを検討してください。

ほとんどの場合、これはGPU設定を制御する専用アプリケーションで実行されます。 例えば、NVIDIA GPUの場合、「NVIDIAコントロールパネル」アプリケーションでこれを実行できます。

レジストリに保存されているユーザーインターフェイスをリセットする

このクラッシュの原因が表示設定の変更やスケーリングである場合は、Designerの既存のレジストリエントリを削除して、特にユーザーインターフェイスを完全にリセットしてみてください。

オペレーティングシステムごとにこのリセットを実行する手順は、以下の通りです。

+++Windows
* Designerを閉じる

Designerを閉じる

* <b>コマンドプロンプト</b>アプリケーションを開きます

<b>コマンドプロンプト</b>アプリケーションを開きます

* 次のコマンドを入力して、<b>Enter</b>を押してください：

  <b>Creative Cloudデスクトップ</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Adobe\Adobe Substance 3D Designer" /f
  ```


  <b>蒸気/Substance版</b>

  ```
  reg delete "HKEY_CURRENT_USER\Software\Allegorithmic\Substance Designer" /f
  ```


次のコマンドを入力して、<b>Enter</b>を押してください：

<b>Creative Cloudデスクトップ</b>

<b>蒸気/Substance版</b>

* 2台目のモニターをシステムから取り外し、再度接続します（*複数のディスプレイを接続していない*&#x200B;場合は、この手順を無視してください）。

2台目のモニターをシステムから取り外し、再度接続します（*複数のディスプレイを接続していない*&#x200B;場合は、この手順を無視してください）。

* Designerを起動しますが、プロジェクトを&#x200B;*作成したり開いたりしないでください*

Designerを起動しますが、プロジェクトを&#x200B;*作成したり開いたりしないでください*

* トップバーで、<b>ウィンドウ</b>メニューを開き、<b>新しい3Dビュー</b>オプションを選択します

トップバーで、<b>ウィンドウ</b>メニューを開き、<b>新しい3Dビュー</b>オプションを選択します

* <b>3Dビュー</b>が正しく初期化されていることを確認し、パネルのトップバーの<b>シーン</b>メニューで別のプレビューメッシュを試してください

<b>3Dビュー</b>が正しく初期化されていることを確認し、パネルのトップバーの<b>シーン</b>メニューで別のプレビューメッシュを試してください

* マテリアルを作成または開く

マテリアルを作成または開く

+++

+++macOS
* Designerを閉じる

Designerを閉じる

* <b>ターミナル</b>アプリケーションを開く

<b>ターミナル</b>アプリケーションを開く

* 次のコマンドを入力して、<b>Enter</b>を押してください：

  <b>Creative Cloudデスクトップ</b>

  ```
  rm ~/Library/Preferences/com.adobe.Adobe\ Substance\ 3D\ Designer.plist
  ```


  <b>蒸気/Substance版</b>

  ```
  rm ~/Library/Preferences/com.allegorithmic.Substance\ Designer.plist
  ```


次のコマンドを入力して、<b>Enter</b>を押してください：

<b>Creative Cloudデスクトップ</b>

<b>蒸気/Substance版</b>

* 2台目のモニターをシステムから取り外し、再度接続します（*複数のディスプレイを接続していない*&#x200B;場合は、この手順を無視してください）。

2台目のモニターをシステムから取り外し、再度接続します（*複数のディスプレイを接続していない*&#x200B;場合は、この手順を無視してください）。

* Designerを起動しますが、プロジェクトを&#x200B;*作成したり開いたりしないでください*

Designerを起動しますが、プロジェクトを&#x200B;*作成したり開いたりしないでください*

* トップバーで、<b>ウィンドウ</b>メニューを開き、<b>新しい3Dビュー</b>オプションを選択します

トップバーで、<b>ウィンドウ</b>メニューを開き、<b>新しい3Dビュー</b>オプションを選択します

* <b>3Dビュー</b>が正しく初期化されていることを確認し、パネルのトップバーの<b>シーン</b>メニューで別のプレビューメッシュを試してください

<b>3Dビュー</b>が正しく初期化されていることを確認し、パネルのトップバーの<b>シーン</b>メニューで別のプレビューメッシュを試してください

* マテリアルを作成または開く

マテリアルを作成または開く

+++
