---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/resources/warnings-from-dependencies.html"
breadcrumb-title: ''
description: Substance 3D Designerのリソースの依存関係に関する警告とその解決方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Resources > Warnings from dependencies
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 依存関係からの警告
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1158'
ht-degree: 0%

---


# 依存関係からの警告

ここでは、Substance 3D Designerの依存関係によって発生する可能性のある警告とエラーメッセージの一覧を示し、それぞれの一般的なトラブルシューティング手順について説明します。

依存関係は、Substance 3Dファイル(SBS)によって参照される&#x200B;*その他のファイル*&#x200B;です。 これらのファイルには、[resources](../../resources/resources.md)および[graphインスタンス](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)ノードによって参照される他のSubstance 3Dファイルが含まれます。

## ![（エラー）](warnings-from-dependencies.resources/error.svg)依存パッケージが無効です

依存関係パッケージを読み込めません。パッケージが見つからないか、壊れているか、使用中のDesignerのバージョンと互換性がありません。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

この問題を修正するには、主に次の2つの方法があります。

1. <b>依存関係を正常に読み込む</b>

   警告メッセージで指定された場所に依存パッケージが存在することを確認してください。 見つからない場合は、ファイルを見つけて元の場所に戻すか、その場所に再作成します。 ファイルが存在する場合は、Designerで&#x200B;*そのファイルを読み込んでみます*&#x200B;そのパッケージに関連する警告やエラーを確認します。 これらの特定の問題については、トラブルシューティングの手順を参照し、適宜修正してください。

   次に、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルでホストパッケージのRMBをクリックし、コンテキストメニューの<b>再読み込み</b>オプションを選択して、ホストパッケージを再読み込みします。

   ![&#39;無効な依存パッケージ&#39;ソリューション1](warnings-from-dependencies.resources/warnings-from-dependencies-01.gif "&#39;無効な依存パッケージ&#39;ソリューション1")
1. <b>パッケージ内の依存関係を再配置します</b>

   [依存関係マネージャー](../../interface/dependency-manager/dependency-manager.md)を使用して、依存関係を再配置できます。 [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルのホストパッケージで「RMB」をクリックし、コンテキストメニューの<b>依存関係マネージャー</b>オプションを選択します。

   依存関係マネージャーの一覧で見つからない依存関係を探し、その依存関係のRMBをクリックして、[<b>再配置…</b>]オプションを選択します。 ファイルブラウザーダイアログを使用して依存関係パッケージを見つけ、[<b>開く</b>]をクリックします。

   次に、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルでホストパッケージのRMBをクリックし、コンテキストメニューの<b>再読み込み</b>オプションを選択して、ホストパッケージを再読み込みします。

   ![&#39;無効な依存パッケージ&#39;ソリューション2](warnings-from-dependencies.resources/warnings-from-dependencies-02.gif "&#39;無効な依存パッケージ&#39;ソリューション2")

## ![（エラー）](warnings-from-dependencies.resources/error.svg)エイリアス&#x200B;*&#39;X&#39;*&#x200B;がプロジェクトで定義されていることを確認してください

パッケージの依存関係またはリソースの1つは、警告で報告されたエイリアスの下のSubstance 3Dファイル(SBS)データで[エイリアス](../../interface/preferences-window/project-settings/project-settings.md)の場所から読み込まれています。エイリアスは現在の[プロジェクトファイル](../../interface/preferences-window/project-settings/project-settings.md)では定義されていません。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

[プロジェクトファイル](../../interface/preferences-window/project-settings/project-settings.md)の少なくとも1つは、警告で報告されるエイリアスを定義する必要があります。

![&#39;エイリアスのチェックが定義されています&#39;ソリューション](warnings-from-dependencies.resources/warnings-from-dependencies-03.gif "&#39;エイリアスのチェックが定義されています&#39;ソリューション")

## ![（エラー）](warnings-from-dependencies.resources/error.svg)このリソースに一致するファイルが見つかりません

[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)の&#x200B;*UDIMテンプレート*&#x200B;に一致するファイルが見つかりません。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)がリンクされ、Designerのファイル名に&#x200B;*UDIM名前付けタクソノミ*&#x200B;が見つかった場合（例： `my_texture_0x1.png`の`0x1`）、DesignerでUDIMワークフローを使用している場合に、[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードがそのタクソノミを使用してUDIMセット内の他のビットマップに&#x200B;*自動的に切り替えることができるように、* UDIMテンプレート&#x200B;*としてリンクします。*&#x200B;その場合、Designerは、UDIM番号付けテンプレートを考慮して&#x200B;*異なる方法*&#x200B;でビットマップリソースをリンクします。

この問題を修正するには、主に次の2つの方法があります。

1. <b>ファイルの復元</b>

   リソースの<b>ファイルパス</b>属性で指定された場所に移動し、テンプレートに続くファイルが存在することを確認してください。 そうでない場合は、復元または再作成します。

   ![&#39;リソース&#39;ソリューション1](warnings-from-dependencies.resources/warnings-from-dependencies-04.gif "に一致するファイルがありません&#39;リソース&#39;ソリューション1")に一致するファイルはありません
1. <b>ファイルの場所を変更する</b>

   ファイルが移動または名前変更された場合は、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルのリソース項目で「元に戻す」をクリックしてファイルを再配置し、<b>再配置</b>オプションを選択して、そのリソースを同じ種類のUDIM画像のセット&#x200B;*最初のファイル*&#x200B;にリンクします。

   ![&#39;リソース&#39;ソリューション2](warnings-from-dependencies.resources/warnings-from-dependencies-05.gif "に一致するファイルはありません。&#39;リソース&#39;ソリューション2")に一致するファイルはありません

## ![（エラー）](warnings-from-dependencies.resources/error.svg)リンクファイルが見つかりません

リンクされたリソースによって参照されているファイルは、<b>File Path</b>属性で指定された場所に存在しません。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

この問題を修正するには、主に次の2つの方法があります。

1. <b>ファイルの復元</b>

   リソースの<b>ファイルパス</b>属性で指定された場所に移動し、ファイルが存在することを確認してください。 表示されない場合は、復元または再作成します。

   ![&#39;リンクされたファイルが見つかりません&#39;ソリューション1](warnings-from-dependencies.resources/warnings-from-dependencies-06.gif "&#39;リンクされたファイルが見つかりません&#39;ソリューション1")
1. <b>ファイルの場所を変更する</b>

   ファイルが移動または名前変更された場合は、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルのリソース項目で「元に戻す」をクリックしてファイルを再配置し、<b>再配置</b>オプションを選択して、そのリソースを同じ種類の別のファイルにリンクします。

   ![&#39;リンクされたファイルが見つかりません&#39;ソリューション2](warnings-from-dependencies.resources/warnings-from-dependencies-07.gif "&#39;リンクされたファイルが見つかりません&#39;ソリューション2")

## ![（エラー）](warnings-from-dependencies.resources/error.svg)カラースペースが見つかりません

[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)は、現在の[カラーマネジメント](../../color-management/color-management.md)環境にないカラースペースを参照しています。 ICCプロファイルまたはOCIO設定のカラースペースを指定できます。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

カラースペース属性のオプションのリストに、使用可能な有効なカラースペースが自動的に入力されます。 そのリソースのカラースペースの値を、リスト内の他のエントリに変更します。

または、そのカラースペースを現在の[カラーマネジメント](../../color-management/color-management.md)環境に追加し、Designerを再起動します。 ICCプロファイルまたはOCIO設定のカラースペースを指定できます。

>[!NOTE]
>
> この警告は、**従来**&#x200B;以外のカラーマネジメントモードを使用している場合にのみトリガーされます（これはカラーマネジメントを無効にすることに似ています）。 カラーマネジメントは、[プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)の&#x200B;**カラーマネジメント**&#x200B;セクションで有効にすることができます。

![&#39;カラースペースが見つかりません&#39;ソリューション](warnings-from-dependencies.resources/warnings-from-dependencies-08.gif "&#39;カラースペースが見つかりません&#39;ソリューション")

## ![（エラー）](warnings-from-dependencies.resources/error.svg)参照リソースが見つかりません

[3D シーンリソース](../3d-scene-resource/3d-scene-resource.md)のUVタイルに割り当てられたグラフが、警告で報告された場所に見つかりません。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

この問題を修正するには、主に次の2つの方法があります。

1. <b>グラフの復元</b>

   [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルのパッケージの内容で、<b>UV タイル</b>の一覧で指定されているグラフを確認してください。 存在しない場合は、復元または再作成します。

   ![&#39;参照リソースが見つかりません&#39;ソリューション1](warnings-from-dependencies.resources/warnings-from-dependencies-09.gif "&#39;参照リソースが見つかりません&#39;ソリューション1")
1. <b>別のグラフを選択</b>

   パッケージ内の別のグラフをUVタイルに割り当てます。

   ![&#39;参照リソースが見つかりません&#39;ソリューション1](warnings-from-dependencies.resources/warnings-from-dependencies-10.gif "&#39;参照リソースが見つかりません&#39;ソリューション2")

## ![（エラー）](warnings-from-dependencies.resources/error.svg) UVタイルが複数回割り当てられています

[UVリソース](../3d-scene-resource/3d-scene-resource.md)の3D シーンタイルは、[Substance グラフ](../../compositing-graphs/substance-compositing-graphs.md)に複数回割り当てられています。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

3Dメッシュリソースの各UVセットに対して、<b>UVタイル</b>リストに&#x200B;*複数回存在する* UDIMインデックスがないことを確認してください。

![&#39;UVタイルが複数回割り当てられています&#39;解決策](warnings-from-dependencies.resources/warnings-from-dependencies-11.gif "&#39;UVタイルが複数回割り当てられています&#39;解決策")

## ![（エラー）](warnings-from-dependencies.resources/error.svg)無効なUVタイル

[3Dシーンリソース](../3d-scene-resource/3d-scene-resource.md)にリストされたUVタイルが、メッシュで定義されていないか、破損しています。

<b>![(tick)](warnings-from-dependencies.resources/check.svg)ソリューション</b>

3Dメッシュリソースの各UVセットに対して、<b>UVタイル</b>リストのすべての項目が、リンクされたリソースに&#x200B;*存在*&#x200B;するUDIMを参照していることを確認してください。

>[!NOTE]
>
> この警告は、*only*&#x200B;がリンクされたリソースで検出されたUDIMを一覧表示するため、ユーザーインターフェイスを通じてトリガーすることはできません。 Substance 3Dファイル(SBS) *直接*&#x200B;のデータを変更した場合にのみ、この警告がトリガーされます。

![&#39;無効なUVタイル&#39;ソリューション](warnings-from-dependencies.resources/warnings-from-dependencies-12.gif "&#39;無効なUVタイル&#39;ソリューション")
