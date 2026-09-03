---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Substance 3D Designer グラフにコメントを付けて、ワークフローを文書化し、ノードの接続について説明します。
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 注釈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# 注釈

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![コメントアイコン](comment.resources/comment-01.png "コメントアイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

コメントは、グラフ内の任意の場所に配置できる、自由に動くテキストです。

グラフの一部に注釈を付けたり、説明したりすることを目的としています。 その<b>Description</b>プロパティには、表示されているテキストが保持されています。

</td>
</tr>
</table>

>[!NOTE]
>
> コメントには、グラフ内のフットプリントを最小限に抑えることを目的とした自動改行が含まれています。

## コメントの作成

デフォルトのコメントの種類は、グラフの節点とは別に配置されます。

以下の方法で作成できます。

+++ノードメニュー
グラフ表示で<b>スペースバー</b>を押して<b>ノードメニュー</b>を開き、リストの「コメント」項目を選択します。

検索フィールドに「comment」と入力して、項目を表面化し、より迅速に検索します。

+++

+++ショートカット
[環境設定](../../../../interface/preferences-window/preferences-window.md)の「コメント」項目にキーボードショートカットがマッピングされている場合は、グラフビューにフォーカスがあるときにそのショートカットを押します。

+++

+++コンテキストメニュー
グラフビューで、任意のオブジェクトまたは空のスペースで<b>人民元</b>を押し、「<b>コメントを追加</b>」オプションを選択します。

+++

+++グラフツールバー
グラフビューツールバーで、<b>ノードパレット</b>の[コメント]ボタンをクリックします。

+++

+++ライブラリ
ライブラリで、<b>グラフ項目</b>を選択し、「コメント」項目をグラフビューにドラッグ&amp;ドロップします。

+++

>[!TIP]
>
> コメントを作成すると、その「説明」プロパティに自動的にフォーカスが移動し、コメントのテキストをすぐに編集できます。

## 親になったコメント

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

親の付いたコメントとは、ノードが移動したときにコメントが続き、グラフが削除されたときにコメントも一緒に削除されるように、ノードの特定のノード&#x200B;*に*&#x200B;添付されたコメントです。

*single*&#x200B;ノードが現在選択されているとき、または単一ノードのコンテキストメニューを通じて作成されたコメントは、そのノードの親になります。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![コメント：親になったコメント](comment.resources/comment-02.gif "コメント：親になったコメント")

</td>
</tr>
</table>

## HTMLの書式設定

HTMLタグを使用してテキストを書式設定できます。 この書式設定は、コメントの<b>Description</b>プロパティの![](comment.resources/comment-03.png) <b>HTMLマークアップ</b>ボタンを使用して切り替えられます。

>[!TIP]
>
> この機能について詳しくは、[フレーム](../../../../interface/the-graph-view/graph-items/frame/frame.md)のドキュメントの<b>説明</b>セクションを参照してください。

![注釈：HTML注釈](comment.resources/comment-04.gif "注釈：HTML注釈")
