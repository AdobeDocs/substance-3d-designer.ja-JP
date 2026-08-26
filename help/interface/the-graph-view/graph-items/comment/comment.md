---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/the-graph-view/graph-items/comment.html"
breadcrumb-title: ''
description: Substance 3D Designerグラフにコメントを付けて、ワークフローを文書化し、ノードのコネクションについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Comment
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 注釈
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '338'
ht-degree: 1%

---


# 注釈

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![コメントアイコン](../../../../assets/graphatomic-comment_1.png "コメントアイコン")

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

デフォルトのコメントの種類は、グラフ内のノードとは別に配置されます。

以下の方法で作成できます。

+++ノードメニュー
グラフ表示で<b>スペースバー</b>を押して<b>ノードメニュー</b>を開き、リストの「コメント」項目を選択します。

検索フィールドに「comment」と入力して、項目を表面化し、より迅速に検索します。

+++

+++ショートカット
[環境設定](../../../../interface/preferences-window/preferences-window.md)の「コメント」項目にキーボードショートカットがマッピングされている場合は、グラフビューにフォーカスがあるときにそのショートカットを押します。

+++

+++コンテキストメニュー
グラフビューで、任意のオブジェクトまたは空の領域で<b>人民元</b>を押し、[<b>コメントの追加</b>]オプションを選択します。

+++

+++グラフツールバー
グラフビューツールバーで、<b>ノードパレット</b>の[コメント]ボタンをクリックします。

+++

+++ライブラリ
ライブラリで、<b>グラフ項目</b>カテゴリを選択し、「コメント」項目をグラフビューにドラッグアンドドロップします。

+++

>[!TIP]
>
> コメントを作成すると、その「説明」プロパティに自動的にフォーカスが移動し、コメントのテキストをすぐに編集できます。

## 親になったコメント

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

親の付いたコメントとは、グラフ内の特定のノードに付けられた&#x200B;*コメントです。ノードが移動するとコメントが続いて表示され、ノードが削除されるとコメントも一緒に削除されます。*

*single*&#x200B;ノードが現在選択されているとき、または単一ノードのコンテキストメニューを通じて作成されたコメントは、そのノードの親になります。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![コメント：親になったコメント](../../../../assets/graph-comment_parented.gif "コメント：親になったコメント")

</td>
</tr>
</table>

## HTMLの書式設定

HTMLタグを使用してテキストを書式設定できます。 この書式設定は、コメントの<b>Description</b>プロパティの![](../../../../assets/graph-frames_html-markup-button.png) <b>HTMLマークアップ</b>ボタンを使用して切り替えられます。

>[!TIP]
>
> この機能について詳しくは、[フレーム](../../../../interface/the-graph-view/graph-items/frame/frame.md)のドキュメントの<b>説明</b>セクションを参照してください。

![注釈：HTML注釈](../../../../assets/graph-comment_html-markup.gif "注釈：HTML注釈")
