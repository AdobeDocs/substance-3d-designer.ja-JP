---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/working-with-3d-scenes.html"
breadcrumb-title: ""
description: Substance 3D Designerで3D シーンを読み込み、編集、操作して、マテリアルをプレビューおよびテストする方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D シーンの操作
user-guide-description: ""
user-guide-title: ""
source-git-commit: c3acf6cdb931126827d2a35dec1135800788ed81
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 0%
---

# 3D シーンの操作

![3D シーンの操作](working-with-3d-scenes.resources/workingWith3DScenes.png "3D シーンの操作"){zoomable="yes"}

Designerでは、[3D シーン](../glossary/glossary.md)を読み込んで、コンテキスト内のマテリアルで作業できます。 各フォーマットでサポートされている機能のリストを含む、3Dシーンでサポートされているファイルフォーマットのリストは、こちらを参照してください。 <b>&lt;リンクが必要です></b>

コンテキストで作業するには、シーンの[マテリアル](../glossary/glossary.md)の1つを[上書き](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)して、Designerで作成されたマテリアルに置き換える必要があります。\
最初から、Designerで利用できる任意のSubstanceグラフテンプレートを使用するか、または3D シーンのマテリアルから[値とテクスチャを抽出](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)して、ゼロから作成することができます。

3D シーンの処理が完了したら、別のアプリケーションで取り込む新しいファイルに[エクスポート](../working-with-3d-scenes/exporting-scenes/exporting-scenes.md)できます。

USD形式に書き出す場合。このワークフローはすべて<b>非破壊的</b>にすることができます。つまり、編集内容と追加内容のみが書き出されます。

まず、作業する3D シーンを読み込み、セッション間でDesignerのステータスを維持できるようにする必要があります。

## 3D シーンのコンテンツ

3D シーンを読み込むときに、Designerはデータをホストする独自のシーンを作成しました。

シーンの次の内容を操作できます。

* <b>マテリアル:</b>シーンで使用されているすべてのマテリアルは、Designerによって作成されたコピーで[上書き](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)できます。 そのコピーの[マテリアルのプロパティ](../interface/3d-view/material-properties/material-properties.md)をRAW値またはSubstanceグラフからのテクスチャで編集できます。
* <b>メッシュ:</b>ジオメトリは、ビューポートで直接選択するか、[シーンブラウザー](../interface/3d-view/scene-browser/scene-browser.md)から選択して、そのマテリアル操作にアクセスすることができます（[上書き](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)、[リセット](../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)、[Substanceグラフに展開](../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)）
* <b>ライト:</b> シーン内のすべてのライトは、[シーンブラウザー](../interface/3d-view/scene-browser/scene-browser.md)で無効にできます。
* <b>カメラ:</b> シーンで検出されたすべてのカメラは、Designerによって追加されたカメラにプリセットとして追加されます。

![3D シーンの内容](working-with-3d-scenes.resources/loaded3DScene.png "3D シーンの内容"){zoomable="yes"}

Designerは、3D シーンにUSDの説明を使用します。 そのレイアウトは、シーンブラウザーで移動できます。各[USD prim](https://openusd.org/release/glossary.html#usdglossary-prim)型には独自のアイコン（ジオメトリ、マテリアル、シェーダー、カメラ、変形など）があります。

[シーンブラウザー](../interface/3d-view/scene-browser/scene-browser.md)を使用して、シーンーのコンテンツを選択、有効、および無効にできます。 したがって、カスタム3D シーンを操作する場合は、常に表示しておくことをお勧めします。

## シーンの読み込み

3D ビューに3D シーンを読み込むには、いくつかの方法があります。

1. [パッケージ](../glossary/glossary.md)の[3D シーンリソース](../resources/3d-scene-resource/3d-scene-resource.md)をダブルクリックするか、3D ビューにドラッグします
1. [ライブラリ](../interface/the-library/the-library.md)の3D シーン項目を3D ビューにドラッグします（[独自のコンテンツをライブラリに追加](../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)した場合）
1. 3D シーンファイルをシステムのファイルブラウザから3D ビューにドラッグします
1. 3D シーン・ステート・ファイル(SBSSCN)とその参照メッシュをロードします。

シーンのステータスは3D シーン・リソースおよびシーン・ステート・ファイルに書き込まれ、パッケージに保存されるため、シーンを再びロードできるのは、メソッド1と4だけです。前回の作業とまったく同じです。 方法2および3は、他の方法と同様にシーンをロードします。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![3D シーンの読み込み – 3D シーンリソースから](working-with-3d-scenes.resources/load3DScene-3DSceneResource.gif "3D シーンの読み込み – 3D シーンリソースから"){zoomable="yes"}

3D シーンリソースを読み込んでいます

</td>
<td style="border: 0;" valign="top">

![3D シーンの読み込み – ライブラリから](working-with-3d-scenes.resources/load3DScene-Library.gif "3D シーンの読み込み – ライブラリから"){zoomable="yes"}

ライブラリからの3D シーンの読み込み

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![3D シーンファイルから3D シーンを読み込んでいます](working-with-3d-scenes.resources/load3DScene-3DSceneFile.gif "3D シーンファイルから3D シーンを読み込んでいます"){zoomable="yes"}

3D シーンファイルをロードしています

</td>
<td style="border: 0;" valign="top">

![3D シーンの読み込み – シーンの状態ファイルから](working-with-3d-scenes.resources/load3DScene-sceneStateFile.gif "3D シーンの読み込み – シーンの状態ファイルから"){zoomable="yes"}

シーン状態ファイルを読み込み中

</td>
</tr>
</table>

>[!NOTE]
>
> 3D ビュー内のシーンのナビゲーションと視覚化については、[3D ビュードキュメント](../interface/3d-view/3d-view.md)を参照してください。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

Designerでは、シーンに存在する環境に加えて、常に独自の環境（USDのDomeLight）とカメラが作成されます。

Designerで作成されたアイテムは、シーンブラウザーに<b>太字のラベル</b>で一覧表示されます。

>[!NOTE]
>
> 読み込まれたシーンに1つ以上のEnvironment (DomeLight)がある場合、Designerによって作成されたEnvironmentは、シーンのEnvironment Lightingと干渉しないように既定で&#x200B;*無効*&#x200B;になっています。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![シーンブラウザー – Designerによって作成された要素](working-with-3d-scenes.resources/sceneBrowser-createdByDesigner.png "シーンブラウザー – Designerによって作成された要素"){zoomable="yes"}

</td>
</tr>
</table>

## シーン状態ファイル

3D ビューにマテリアル、カメラ、ライトなどを設定した後、そのステータスをシーンのステータス・ファイル(.sbssscn)に保存できます。このファイルは、後でロードしてステータスをリストアできます。 例えば、様々な種類のマテリアルや特定の照明環境をプレビューするためのいくつかのシーンを設定することができます。

![シーン状態ファイルの読み込み](working-with-3d-scenes.resources/loadSceneStateFile.gif "シーン状態ファイルの読み込み"){zoomable="yes"}

保存されたシーンのステートは、3D ビューのデフォルトのステートとしても使用できるため、新しい3D ビューが作成されるたびに、そのステートが使用されます。 これは、タイリングの値が2で環境マップを指定したSphere 2-Tiles メッシュで、マテリアルのマテリアルをデフォルトでプレビューする場合に便利です。

シーン状態ファイルに関連する操作は、3D ビューのシーンメニューにあり、[こちら](../interface/3d-view/3d-view.md)で説明されています。

シーン状態ファイルはXML形式を使用し、[プロジェクト設定](../interface/preferences-window/project-settings/project-settings.md)で定義されている場合は[エイリアス](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)を使用します。

>[!NOTE]
>
> レンダラーがシーン状態ファイルに保存されません。
