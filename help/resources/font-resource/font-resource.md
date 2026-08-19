---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/resources/font-resource.html"
breadcrumb-title: ''
description: Substance 3D Designerでフォントリソースを読み込んで使用し、テキストやタイポグラフィを素材に追加できます。
helpx_creative_field: ""
helpx_description: Designer > Resources > Font resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: フォントリソース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---


# フォントリソース

フォントリソースは、[atomic Textノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)と共に使用されます。 ディスク上の任意の場所にあるフォントファイルを参照することで、システムにインストールされていないフォントを使用できるようになります。

>[!NOTE]
>
> **SBSARのフォント**
> 
> フォントは、リンクされたリソースから、またはシステムにインストールされたフォントを使用しているかどうかに関係なく、常にSBSARに埋め込まれます。 この方法の利点は、インストールする必要がないことと、依存関係のあるSBSファイルを書き出すときにフォントファイルが一緒に来ることを確認できることです。

## カスタムフォントリソースの使用

* パッケージを右クリックし、<b>リンク/フォント</b>を選択します
* .otfまたは.ttfファイルを選択します。
* [テキストノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)を[グラフ](../../compositing-graphs/substance-compositing-graphs.md)に配置します。
* <b>フォント</b>プロパティでは、フォントリソースは一覧の先頭に表示されます。

フォントの一覧は、プロパティを開いても自動的に更新されるわけではありません。 新しくリンクされたフォントを表示するには、別のプロパティウィンドウに切り替えて、テキストノードに戻る必要があります。
