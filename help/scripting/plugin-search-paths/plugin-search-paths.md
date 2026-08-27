---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/plugin-search-paths.html"
breadcrumb-title: ''
description: Substance 3D Designerでプラグイン検索パスを設定し、Pythonプラグインの配置場所を指定します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Plugin search paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: プラグイン検索パス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '133'
ht-degree: 0%

---


# プラグイン検索パス

Designerは、特定のディレクトリ（検索パスなど）でプラグインを検索します。 このページでは、これらのパスを設定する方法について説明します。

ユーザーは、ソフトウェアの環境設定で手動で&#x200B;*カスタムディレクトリ*&#x200B;を追加するか、環境変数を使用してカスタムディレクトリを指定できます。

## プラグイン検索パスの手動追加

1. <b>編集/環境設定…</b>に移動
1. <b>プロジェクト</b>カテゴリを選択
1. 編集する<b>プロジェクトファイル</b>を選択します
1. <b>Python</b>タブで、*<b>+</b>*ボタンをクリックして、プラグインを含むディレクトリを追加します
1. 「<b>OK</b>」をクリックして検証します

![Pythonプラグイン検索パスの設定プロジェクト設定](../../assets/image-70.png "Pythonプラグイン検索パスの設定プロジェクト設定")

## 環境変数の使用

アプリケーションは、<b>SBS\_DESIGNER\_PYTHON\_PATH </b>環境変数を使用して指定されたすべてのパスでプラグインを検索します。
