---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph.html"
breadcrumb-title: ''
description: Substance 3D DesignerでSubstance合成グラフを作成し、プロシージャルテクスチャワークフローを構築する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Creating a Substance graph
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance グラフの作成
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 1%

---


# Substance グラフの作成

Designerでのテクスチャのオーサリングは、最初に作成済みのSubstanceまたは空のグラフからテンプレートグラフを作成します。

<a name="create-graph"></a>

## グラフの作成

新しい[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)を作成するには、次のいずれかの方法を使用します。

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  ホーム画面で、<b>新規グラフ</b>ボタンをクリックします。

  </td>
  <td style="border: 0;" valign="top">

  ![新しいSubstanceグラフダイアログ – ホーム画面から作成](creating-a-substance-compositing-graph.resources/newGraphDialog-create-homeScreen.png "新しいSubstanceグラフダイアログ – ホーム画面から作成"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)の&#x200B;*既存*&#x200B;のパッケージ項目で、<b>RMB</b>をクリックし、コンテキストメニューの<b>新規/Substanceグラフ</b>に移動します。

  </td>
  <td style="border: 0;" valign="top">

  ![新しいSubstanceグラフダイアログ – エクスプローラーから作成](creating-a-substance-compositing-graph.resources/newGraphDialog-create-explorer.png "新しいSubstanceグラフダイアログ – エクスプローラーから作成"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  メインツールバーで、![](creating-a-substance-compositing-graph.resources/image2021-6-22-20-36-44.png) <b>新規Substanceグラフ</b>をクリックします。

  </td>
  <td style="border: 0;" valign="top">

  ![新しいSubstanceグラフダイアログ – メインツールバーから作成](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainToolbar.png "新しいSubstanceグラフダイアログ – メインツールバーから作成"){zoomable="yes"}

  </td>
  </tr>
  </table>

* &#x200B;
  <table>
  <tr style="border: 0;">
  <td style="border: 0;" valign="top">

  メインメニューで、<b>ファイル/新規/Substanceグラフ…</b>に移動します

  </td>
  <td style="border: 0;" valign="top">

  ![](creating-a-substance-compositing-graph.resources/newGraphDialog-create-mainMenu.png)

  </td>
  </tr>
  </table>

* <b>Ctrl + N</b> (Windows) / <b>Cmd + N</b> (macOS)キーを押します。

<b>新しいSubstanceグラフ</b>ダイアログが表示されます。

<a name="graph-templates"></a>

## グラフテンプレート

新しいSubstanceグラフの作成方法に関係なく、常に<b>新しいSubstanceグラフ</b>ダイアログが表示され、新しいグラフを構成できます。

![新しいSubstanceグラフダイアログ – マテリアル](creating-a-substance-compositing-graph.resources/newGraphDialog-materials.png "新しいSubstanceグラフダイアログ – マテリアル"){zoomable="yes"}

### テンプレート

Designerにはノードが事前設定されたグラフテンプレートが含まれており、作業をすばやく開始できます。 [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノード、これらの出力に値を渡すための単純なノード（[均一な色](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)など）および[Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)ノードを含めることができます。

一覧のテンプレートをダブルクリックするか、テンプレートを選択して[<b>作成</b>]ボタンをクリックし、そのテンプレートを使って新しいSubstanceグラフを作成します。 デフォルトでは、新しいグラフは保存されていない新しいパッケージに配置されます。

>[!TIP]
>
> ゼロから作成
> 
> 完全に空のグラフから開始するには、&#39;空&#39;カテゴリで<b>空</b>テンプレートを選択します。

>[!NOTE]
>
> テンプレートの切り替え
> 
> 間違ったテンプレートを選択すると、グラフの作成後に&#x200B;*別のテンプレートに切り替えることはできません*。
> 
> 既存のグラフを別のテンプレートに移植するには、適切なテンプレートを使用して新しいグラフを作成し、グラフを新しいグラフにコピー&amp;ペーストします。 ノードを適切に再接続し、特にノードを出力します。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

各テンプレートは、ラベルとサブタイトルごとに表示されます。

字幕は、テンプレートの&#x200B;*ユースケース*&#x200B;に関する詳細なコンテキストを提供します。テンプレートの基になるマテリアルモデル、テンプレートと組み合わせることを目的とするソフトウェアなどです。

<b>サムネール</b>モードでは、サブタイトルは暗く小さいテキストのラベルの下に配置されます。

<b>リスト</b>、<b>パッケージ</b>および<b>ディレクトリ</b>表示モードでは、サブタイトルがラベルに完全に追加されます： *ラベル – サブタイトル*。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![新しいSubstanceグラフダイアログ – サムネイルカード](creating-a-substance-compositing-graph.resources/newGraphDialog-thumbnailCard.png "新しいSubstanceグラフダイアログ – サムネイルカード")

</td>
</tr>
</table>

<a name="material-samples"></a>

### マテリアルサンプル

<b>マテリアルサンプル</b>のカテゴリには、[厳選されたグラフの選択](../../compositing-graphs/creating-compositing-gra/material-samples/material-samples.md)が含まれており、そこから学習して試すことができます。

<b>[サンプルに移動]</b>ボタンを使用して、ホーム画面から直接サンプルにアクセスすることもできます。

すべてのサンプルは[マテリアルモデル](../../interface/3d-view/material-properties/material-properties.md#openpbr)に基づいています。

![マテリアルサンプル – ホームスクリーンバナー](creating-a-substance-compositing-graph.resources/materialSamples-banner.png "マテリアルサンプル – ホームスクリーンバナー"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 情報ツールチップ

各テンプレート項目の情報アイコンにカーソルを合わせると、テンプレートに関する追加情報を含むツールチップが表示されます。

<b>種類：</b>テンプレートが生成するアセットの種類です。 これは、[グラフプロパティ](../../compositing-graphs/graph-parameters/graph-parameters.md)で編集できます。

<b>説明：</b>統合するワークフロー、使用目的、使用に関する推奨事項など、テンプレートに関する詳細。

<b>出力：</b>テンプレートの[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードがある場合。

</td>
<td style="border: 0;" valign="top">

![新しいSubstanceグラフダイアログ – テンプレートのヒント](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipTemplate.png "新しいSubstanceグラフダイアログ – テンプレートのヒント"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### 表示モード

テンプレートの一覧は、<b>表示モード</b>ボタンを使用して、さまざまなモードで表示できます。

選択したカテゴリとプロジェクトファイルによって実行されたフィルタは、すべてのビューに適用されます。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![新しいSubstanceグラフダイアログ – 表示モード](creating-a-substance-compositing-graph.resources/newGraphDialog-viewModes.png "新しいSubstanceグラフダイアログ – 表示モード"){zoomable="yes"}

</td>
</tr>
</table>

+++表示モード
![新しいSubstanceグラフダイアログ – サムネイルビュー](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-thumbnails.png "新しいSubstanceグラフダイアログ – サムネイルビュー"){zoomable="yes"}



<b>サムネイル</b>

サムネール付きのカードは、テンプレートタイプのプレビューまたはアイコンを提供します。

![新しいSubstanceグラフダイアログ – 一覧ビュー](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-list.png "新しいSubstanceグラフダイアログ – 一覧ビュー"){zoomable="yes"}



<b>リスト</b>

テンプレートは、ラベル別にのみ表示されます。

![新しいSubstanceグラフダイアログ – パッケージビュー](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-packages.png "新しいSubstanceグラフダイアログ – パッケージビュー"){zoomable="yes"}



<b>パッケージ</b>

テンプレートは、属するパッケージファイルの子として、ラベル別に一覧表示されます。

パッケージファイル項目にカーソルを合わせると、フルパスのツールヒントが表示されます。

![新しいSubstanceグラフダイアログ – ディレクトリビュー](creating-a-substance-compositing-graph.resources/newGraphDialog-viewMode-directories.png "新しいSubstanceグラフダイアログ – ディレクトリビュー"){zoomable="yes"}



<b>ディレクトリ</b>

テンプレートは、属するパッケージファイルをホストしているディレクトリの子として、ラベル別に一覧表示されます。

ディレクトリ項目にカーソルを合わせると、フルパスのツールヒントが表示されます。

+++

### プロパティ

テンプレートを選択した後、新しいグラフに関する基本的な情報を設定できます。 グラフ作成後にいつでも変更できます。

<b>グラフ名</b>:グラフの識別子です。 これは、指定されたパッケージに対して一意である必要があり、スペースや一部の特殊文字を含めることはできません。

<b>サイズ</b>：ほとんどのノードの出力解像度を制御するグラフの親解像度。詳細については、[出力サイズ](../../compositing-graphs/output-size/output-size.md)ページを参照してください。 デフォルトでは、幅とHeightがリンクされています。幅とHeightのコンボボックスの間にある「リンク」ボタンをクリックすると、リンクを解除できます。

<b></b>でグラフを作成する：このコンボボックスを使って新しいグラフ用の&#x200B;*新しい*&#x200B;パッケージを作成するか、既に[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)パネルに読み込まれている&#x200B;*既存の*&#x200B;パッケージに新しいグラフを追加できます。

### ヘルプツールチップ

疑問符のアイコンにカーソルを合わせると、このページに直接リンクするボタンのツールチップが表示されます。このドキュメントは、必要に応じて参照できます。

![新しいSubstanceグラフダイアログ – ヘルプのヒント](creating-a-substance-compositing-graph.resources/newGraphDialog-tooltipHelp.png "新しいSubstanceグラフダイアログ – ヘルプのヒント"){zoomable="yes"}

<a name="managing-templates"></a>

## テンプレートの管理

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### カテゴリ別のフィルタリング

カテゴリは、ユースケースまたはアセットタイプによって相互に関連するテンプレートをグループ化するために使用されます。

<b>カテゴリ</b>コンボボックスを使用して、テンプレートをフィルター処理するカテゴリを選択します。

</td>
<td width="41.67%" style="border: 0;" valign="top">

![新しいSubstanceグラフダイアログ – カテゴリ別にフィルター処理](creating-a-substance-compositing-graph.resources/newGraphDialog-categories.png "新しいSubstanceグラフダイアログ – カテゴリ別にフィルター処理"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

テンプレートの<b>テンプレートデータ</b>には、テンプレートにカテゴリが設定されている場合があります [グラフ属性](../../compositing-graphs/graph-parameters/graph-parameters.md)。テンプレートのリストを絞り込むためのフィルターとして使用されます：

&lt;category>;&lt;subtitle>

カスタムカテゴリは、プロジェクトファイルが提供するテンプレートで設定できます（以下を参照）。 次に、これらのカテゴリがコンボボックスの一覧に追加されます。

</td>
<td width="50.00%" style="border: 0;" valign="top">

![新しいSubstanceグラフダイアログ – テンプレートカテゴリを設定しています](creating-a-substance-compositing-graph.resources/newGraphDialog-templateCategorySetup.png "新しいSubstanceグラフダイアログ – テンプレートカテゴリを設定しています"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

### プロジェクトファイルによるフィルタリング

アクティブな[プロジェクトファイル](../../interface/preferences-window/project-settings/project-settings.md)のいずれかに1つ以上のテンプレートパスが指定されている場合、これらのパスで見つかったパッケージファイル内のグラフがテンプレートの一覧に追加されます。

次に、<b>プロジェクトファイルでフィルター</b>ボタンを使用して、テンプレートのリストを特定のプロジェクトファイルで提供されているリストに絞り込みます。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![新しいSubstanceグラフダイアログ – プロジェクトファイルによるフィルター処理](creating-a-substance-compositing-graph.resources/newGraphDialog-projectFiles.png "新しいSubstanceグラフダイアログ – プロジェクトファイルによるフィルター処理"){zoomable="yes"}

</td>
</tr>
</table>
