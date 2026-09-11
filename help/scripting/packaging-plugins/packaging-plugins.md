---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/scripting/packaging-plugins.html"
breadcrumb-title: ''
description: Substance 3D Designer用Pythonプラグインをパッケージ化して配布およびインストールする方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Packaging plugins
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パッケージプラグイン
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '307'
ht-degree: 3%

---


# パッケージプラグイン

## プラグインパッケージの内容

パッケージは、プラグインに関するメタデータを含む&#x200B;**pluginInfo.json**&#x200B;ファイルを含む、zipアーカイブ内の単一ファイルです。

プラグインコード、およびプラグインが動作するために必要なその他のファイルやリソース。

**PluginInfo.jsonエントリ：**

| エントリ | 説明 | デフォルト値 | メモ |
| --- | --- | --- | --- |
| metadata\_format\_version | メタデータファイルの形式。 | 1 | 必須。現在は1に設定する必要があります。 |
| 名前 | プラグイン名。 |  | 必須。プラグインコードを含むPythonモジュールの名前と一致する必要があります |
| version | プラグインのバージョン。 |  | オプション。 |
| author | プラグインの作成者。 |  | オプション。 |
| 電子メール | プラグイン作成者のメールアドレス。 |  | オプション。 |
| min\_designer\_version | プラグインの動作に必要な最小バージョンのアプリケーション。 | 2019.2 | オプション。 |
| プラットホーム | プラグインを実行するプラットフォーム。 | 任意 | オプション。コンパイル済みコードを含むプラグインの場合、このエントリを使用して、サポートされていないプラットフォームでプラグインを無効にできます。有効な値は、win、linux、osx、anyです。 |

## 新規プラグインパッケージプロジェクトの作成

プラグインパッケージプロジェクトの作成を簡素化するために、[Cookiecutter](https://cookiecutter.readthedocs.io/en/latest/)テンプレートプロジェクトを提供しています。

直接使用することも、必要に応じて変更することもできます。

テンプレートは、アプリケーションディレクトリの<b>plugins/tools/pkgplugintemplate</b>にあります。

1. <b>Pythonがまだシステムにインストールされていない場合は、インストールしてください</b>

   CookiecutterはPython 2とPython 3の両方に対応しています
1. <b>Cookiecutterがまだインストールされていない場合はインストールしてください</b>

   通常は、pipを使用して次の操作を実行できます。

   ```
   pip install cookiecutter
   ```


   Cookiecutterをインストールする別の方法またはCookiecutterの詳細については、<https://cookiecutter.readthedocs.io/en/latest/installation.html>のドキュメントを確認してください
1. <b>新しいプラグインパッケージプロジェクトの作成</b>

   ターミナルウィンドウで、次のコマンドを実行します。

   ```
   cookiecutter path/to/pkgplugintemplate -o path/to/new/project
   ```


   必要な情報を入力します。 指定したディレクトリに新しいプロジェクトが作成されます。
1. <b>開発が完了したら、プラグインをパッケージ化します</b>

   ターミナルウィンドウで、次のコマンドを実行します。

   ```
   python makepackage.py
   ```

1. プラグインパッケージがbuildディレクトリに生成されます
