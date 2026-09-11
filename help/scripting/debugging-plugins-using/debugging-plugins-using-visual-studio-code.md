---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/scripting/debugging-plugins-using-visual-studio-code.html"
breadcrumb-title: ''
description: Visual Studio Codeを使用してSubstance 3D Designer Pythonプラグインをデバッグし、効率的な開発を行う方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Scripting > Debugging plugins using Visual Studio Code
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Visual Studioコードを使用したプラグインのデバッグ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---


# Visual Studioコードを使用したプラグインのデバッグ

多くの開発者のワークフロー標準として、**Visual Studio Code IDE**&#x200B;を使用してPythonプラグインをデバッグできます。

>[!WARNING]
>
> <b>debugpy.listen()</b>メソッドを使用すると、指定したポートに接続できるユーザーは、デバッグされたプロセス内で任意のコードを実行できます。
> 
> したがって、デバッグは、*セキュリティで保護されたネットワーク*&#x200B;上で&#x200B;*<b>のみ</b>*&#x200B;設定および実行する必要があります。

Visual Studio CodeとSubstance 3D Designer間の相乗効果を設定するには、次の手順に従います。

1. **[Visual Studioコード](https://code.visualstudio.com/)**&#x200B;と&#x200B;**[Python拡張機能](https://marketplace.visualstudio.com/items?itemName=ms-python.python)**&#x200B;をインストールします。
1. **[デバッグ可能なPythonモジュール](https://github.com/microsoft/debugpy)**&#x200B;をインストールします。

   >[!NOTE]
   >
   > DesignerのPythonインタプリタが&#39;*debugpy*&#39;モジュールを見つけられることを確認してください。 最も簡単な方法は、&#39;*debug*&#39;モジュールが存在するディレクトリを&#x200B;**PYTHONPATH**&#x200B;環境変数に追加することです。 別の方法として、スクリプト内のsys.pathを変更してデバッグモジュールにパスを追加することもできます。
1. アプリケーションを起動し、Python Editorを開き、**次のコードを実行します**。

   ```
   import sys 
   
   
   
   debugpy_path = '/path/to/debugpy/module' 
   
   debugpy_port = 5678 
   
   designer_py_interpreter = '/path/to/python/executable/bundled/in/designer' 
   
   
   
   if not debugpy_path in sys.path: 
   
       sys.path.append(debugpy_path) 
   
   
   
   import debugpy 
   
   
   
   debugpy.configure(python=designer_py_interpreter) 
   
   debugpy.listen(debugpy_port)
   ```

1. Visual Studio Codeでプロジェクトを開き、**launch.json**&#x200B;ファイルを作成します。 ファイルに以下を追加します。

   ```
   { 
   
       "name": "Attach to Designer", 
   
       "type": "python", 
   
       "request": "attach", 
   
       "port": <port number used in the script above>, 
   
       "host": "127.0.0.1" 
   
   }
   ```

1. <b>デバッグ</b>アイコンをクリックし、必要に応じてデバッガー構成を作成または編集します。
1. **Python: Designerに接続**&#x200B;コンフィギュレーションを選択し、**[デバッグの開始]**&#x200B;をクリックします。

   これで、ブレークポイントの設定、コードのステップ実行、およびVisual Studio Codeのデバッガーの他のすべての機能の使用が可能になります。
