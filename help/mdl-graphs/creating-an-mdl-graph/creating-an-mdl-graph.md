---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/creating-an-mdl-graph.html"
breadcrumb-title: ''
description: Substance 3D Designerでマテリアル定義言語グラフを作成して、カスタムのマテリアルを作成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Creating an MDL graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDL グラフの作成
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '588'
ht-degree: 0%

---


# MDL グラフの作成

ここでは、Substance 3D DesignerでMDL マテリアルを作成するMDL グラフを作成するプロセスについて説明します。

![MDL グラフ生成経路](creating-an-mdl-graph.resources/creating-an-mdl-graph-01.png "MDL グラフ生成経路")

*Designerのインターフェイスに新しいMDL グラフを作成するための経路*

## MDL グラフの作成方法

MDL グラフを作成するには、次のいずれかの方法を使用します。

* *メインメニューバー*&#x200B;の&#x200B;**ファイル/新規/MDL グラフ**&#x200B;オプションを選択します
* *メインツールバー*&#x200B;の「![](creating-an-mdl-graph.resources/creating-an-mdl-graph-02.png) **MDL グラフを追加**」ボタンをクリックします
* **エクスプローラー**&#x200B;パネルで&#x200B;*既存のパッケージ*&#x200B;を右クリックし、**新規/MDL グラフ**&#x200B;を選択します

**新しいMDL グラフ**&#x200B;ダイアログが表示されます（以下を参照）。

![新しいMDL グラフのダイアログ](creating-an-mdl-graph.resources/creating-an-mdl-graph-03.png "新しいMDL グラフのダイアログ")

*新しいMDL グラフダイアログ*

## 新規MDL グラフダイアログ

新しいMDL グラフの作成に使用する方法に関係なく、常に<b>新しいMDL グラフ</b>ダイアログが表示され、新しいグラフを構成できます。

### テンプレート

「<b>テンプレート</b>」セクションでは、グラフテンプレートを選択できます。テンプレートには、グラフをすばやく開始できるように事前に設定されたノードが含まれています。 事前設定されたノードには、出力ノード、これらの出力に値を渡す単純なノード（均一カラーなど）、およびテンプレートに応じた入力ノードが含まれます。

完全に&#x200B;*空白*&#x200B;テンプレートから開始するには、<b>空白</b> グラフを選択します。

<b>プロジェクト</b>オプションを使用すると、テンプレートの一覧をプロジェクトファイルでフィルター処理できます。 これにより、プロジェクトファイルのプロジェクト設定の<b>一般</b>セクションに追加された場所で、カスタムテンプレートを簡単に見つけることができます。

>[!WARNING]
>
> 間違ったグラフを選択した場合、テンプレートの作成後に&#x200B;*別のテンプレートに切り替えることはできません*。\
> 既存のグラフを別のテンプレートに移行するには、適切なテンプレートを使用して新しいグラフを作成し、そのテンプレートにグラフをコピー&amp;ペーストします。 必要に応じて、[ルート](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)ノードを含むノードを再接続します。

テンプレートのリストは、**プロジェクト**&#x200B;コンボボックスの横にある&#x200B;*ボタン*&#x200B;を使用して、さまざまなモードで表示できます。

* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-04.png)最近使用したテンプレートを表示**:リストをフィルターして、最後に使用したテンプレートを&#x200B;*最新のテンプレートから最新のテンプレートまで*&#x200B;順に表示します。一番上のアイテムが最新のテンプレートです
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-05.png)グラフの表示**:テンプレートは、テンプレートのディレクトリにある[Substance 3D](https://www.adobe.com/products/substance3d/3d-augmented-reality.html)ファイルの順に、*ラベルのみ*&#x200B;で表示されます
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-06.png)Substance 3Dファイルの表示**:テンプレートは、テンプレートのディレクトリ内のファイルの順に、*属するSubstance 3Dファイルの子*&#x200B;としてラベルに従って表示されます
* **![](creating-an-mdl-graph.resources/creating-an-mdl-graph-07.png)ディレクトリの表示**:テンプレートは、テンプレートのディレクトリ内のファイルの順序で、属するディレクトリの&#x200B;*子*&#x200B;としてラベルによって表示されます

### プロパティ

<b>グラフのプロパティ</b>セクションでは、新しいグラフに関する基本的な情報を設定できます。 これらはいずれも後からいつでも変更できますが、最初に注意を払い、ユースケースに合わせて適切に設定することは理にかなっています。

* <b>グラフ名</b>: グラフの識別子。 これは、指定されたパッケージに対して一意である必要があり、スペースや一部の特殊文字を含めることはできません。
* <b>パッケージにグラフを作成</b>：このコンボボックスを使用して、新しいグラフ用の&#x200B;*新しい*&#x200B;パッケージを作成するか、エクスプローラーパネルに既に読み込まれている&#x200B;*既存の*&#x200B;パッケージに新しいグラフを追加できます。\
  注意：メソッド<b>4</b>を使用して作成プロセスを開始した場合（上記を参照）、このパラメーターは、プロセスの開始元である既存のパッケージの&#x200B;*プリセット*&#x200B;です。
* <b>テンプレートの詳細</b>：このセクションでは、テンプレートの特性と目的について簡単に説明します
