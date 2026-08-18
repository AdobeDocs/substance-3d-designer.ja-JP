---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/warnings-and-errors.html"
breadcrumb-title: ''
description: Substance 3D Designerでよくある警告やエラーの解決策を確認して、問題を迅速にトラブルシューティングできます。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Warnings and errors
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 警告とエラー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '851'
ht-degree: 6%

---


# 警告とエラー

このページでは、[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)に表示される可能性のある警告とエラーメッセージのレポート、およびソースに基づいた警告のトラブルシューティングへのリンクについて説明します。

## 概要

Designerでプロジェクトの作業中に、プロジェクトの問題を通知する警告やエラーメッセージが表示される場合があります。

* **警告**&#x200B;は、*黄色*&#x200B;のテキストで表示され、入力の不足や構成の誤りによって望ましくない結果を招く可能性のある問題に注意を向けさせます。 通常、*作品をブロック*&#x200B;しません。
* **エラー**&#x200B;は、*赤*&#x200B;のテキストで表示され、計算の失敗、予期しない結果、またはタスクを実行できないことを示します。 彼らは通常、あなたの作品を&#x200B;*ブロック*&#x200B;します。

通常、警告とエラーは、それらがトリガーされたアイテムに表示され、そのアイテムの各親&#x200B;*にわたって*&#x200B;表示されます。 警告とエラーが報告される一般的な場所のリストを次に示します。

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### エクスプローラー

[エクスプローラー](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)パネルの項目に警告がある場合、その警告は、リスト内の項目のエントリの右端に![](../../assets/warning-icon.png)アイコンと共に表示されます。 そのアイコンにカーソルを数秒間置くと、すべての警告の詳細を一覧表示する&#x200B;*ツールチップ*&#x200B;が表示されます。

次の規則に従います。

* アイテムが他のアイテム（フォルダーなど）の下にネストされている場合、折りたたまれている場合はそのアイテムに警告が表示されます。
* 警告リストは&#x200B;*累積的*&#x200B;で、項目の警告&#x200B;*と*&#x200B;の合計、その子の表面化された警告です。
* パッケージの内容によって報告されたすべての警告は、*パッケージ*&#x200B;項目に表示され、パッケージの&#x200B;*独自*&#x200B;の警告に追加されます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-explorer.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### グラフビュー

[グラフビュー](../../interface/the-graph-view/the-graph-view.md)パネル内の警告を含む項目については、その警告がビューポートの&#x200B;*左下隅*&#x200B;に色付きのテキストで表示されます。 特定のノードによって警告がトリガーされた場合、そのノードには![](../../assets/warning-badge.png)警告バッジが付きます。 バッジの上に数秒間カーソルを置いたままにすると、*ツールヒント*&#x200B;が表示され、すべての警告の詳細が一覧表示されます。

次の規則に従います。

* 他のホストグラフに対してソースグラフ&#x200B;*インスタンス化*&#x200B;で1つ以上の警告が発生した場合、そのソースグラフの[インスタンスノード](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)には&#x200B;*単一* `The referenced data has some warnings`の警告が発生します。
* 警告リストは、グラフの警告&#x200B;*と*&#x200B;の子ノードのすべての警告の合計である&#x200B;*累積*&#x200B;です。
* グラフのすべての警告は、エクスプローラーパネルでそのグラフを表すアイテムに関して報告されます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-graph.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### プロパティ

[プロパティ](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)パネルの項目に警告がある場合、その警告は、リスト内の項目のエントリの右端に![](../../assets/warning-icon.png)アイコンと共に表示されます。 そのアイコンにカーソルを数秒間置くと、すべての警告の詳細を一覧表示する&#x200B;*ツールチップ*&#x200B;が表示されます。

次の規則に従います。

* アイテムが他のアイテムの下にネストされている場合（例：セクションヘッダー）、折りたたまれている場合はそのアイテムに警告が表示されます。
* 警告リストは&#x200B;*累積的*&#x200B;で、項目の警告&#x200B;*と*&#x200B;の合計、その子の表面化された警告です。
* [入力パラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)に適用された[関数グラフ](../../function-graphs/function-graphs.md)に1つ以上の警告がある場合、パラメーター項目には&#x200B;*単一* `The [x] parameter's function has some warnings`の警告が含まれます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-properties.png){width="256px"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="58.30%" style="border: 0;" valign="top">

### コンソール

警告とエラーの両方が&#x200B;**コンソール**&#x200B;パネルに報告されます。このパネルには、[メインメニュー](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/the-main-menu-143720673.html)の&#x200B;**ウィンドウ**&#x200B;メニューからアクセスできます。 **チャネル**&#x200B;の設定を`ErrorMgr`に設定すると、警告やエラーを残りのコンソールエントリから分離できます。

>[!NOTE]
>
> コンソール内のすべてのテキストは&#x200B;*選択可能*&#x200B;であるため、このパネルを使用して&#x200B;*警告およびエラーメッセージを簡単にコピー*&#x200B;し、このドキュメントの&#x200B;**ローカル検索**&#x200B;ツールまたは任意のインターネット検索エンジンに貼り付けることができます。 これにより、問題のトラブルシューティングに関するガイダンスを迅速に入手できます。

</td>
<td width="41.60%" style="border: 0;" valign="top">

![](../../assets/warning-overview-console.png){width="256px"}

</td>
</tr>
</table>

### 「（#回）」のメッセージ

*まったく同じ*&#x200B;の警告またはエラーが、アイテム&#x200B;*とその子*&#x200B;について&#x200B;*複数回*&#x200B;発生すると、これらの警告は&#x200B;*1つにマージされ*&#x200B;サフィックスが表示され、この警告またはエラーが報告された回数を知らせることができます。`(# times)`

## カテゴリ

Designerで発生する可能性のある警告とエラーを、発生元に基づいて並べ替えたリストを次に示します。 カテゴリタイトルは、専用ページにリンクし、各問題を解決するための説明とトラブルシューティングガイドを提供します。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### Substance グラフの警告

* 出力ノードが定義されていません
* [x]パラメーターの関数に警告があります
* 参照したデータにいくつかの警告があります
* 参照リソースが見つかりません
* テキストノードで無効なフォントが使用されています

</td>
<td style="border: 0;" valign="top">

### 関数グラフの警告

* 出力ノードが定義されていません
* 現在の出力ノードは、x型の値を返します
* 一部のGetノードに変数名がありません
* 一部のSetノードには変数名がありません

</td>
</tr>
</table>

### 依存関係からの警告

* 無効な依存パッケージ
* プロジェクトでエイリアス「x」が定義されていることを確認します
* このリソースに一致するファイルが見つかりません
* リンクされたファイルが見つかりません
* カラースペースが見つかりませんでした
* 参照リソースが見つかりません
* UVタイルが複数回割り当てられる
* 無効なUVタイル
