---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs.html"
breadcrumb-title: ''
description: Substance 3D Designerで高度なマテリアルワークフロー用のマテリアル定義言語グラフを作成して使用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDLグラフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 0b8b2d2c05587d7fe84a71bb54244a492540d6dc
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 0%

---


# MDLグラフ

Substance 3D DesignerのMDLグラフを使用すると、MDL資料を作成して、その動作をリアルタイムでプレビューできます。

![マラカイトMDLマテリアル](../assets/mdl-malachite-example.jpg "マラカイトMDLマテリアル")

*クリソコラを使ったマラカイト、[Mark Foreman](https://www.artstation.com/oggyart)* *アドビの[従来のSubstance share](https://share-legacy.substance3d.com/libraries/4043)* *プラットフォーム*&#x200B;で利用可能なMDLマテリアル

>[!WARNING]
> 
> MDLグラフおよびすべての関連機能は、バージョン16.0.0でDesignerから削除されました。
> 
> 詳細については、こちらを参照してください： [MDLグラフとIrayの提供終了](../technical-issues/mdl-graph-iray-eol/mdl-graph-iray-eol.md)

+++目次

* [MDLグラフの主な概念](/help/mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)
* [MDLグラフの作成](/help/mdl-graphs/creating-an-mdl-graph/creating-an-mdl-graph.md)
* [MDLライブラリ](/help/mdl-graphs/mdl-library/mdl-library.md)
* [MDLグラフでのパラメータの表示](/help/mdl-graphs/exposing-parameters-mdl/exposing-parameters-in-mdl-graphs.md)
* [SubstanceグラフとMDL資料](/help/mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)
* [MDLコンテンツのエクスポート](/help/mdl-graphs/exporting-mdl-content/exporting-mdl-content.md)
* [MDLグラフの警告](/help/mdl-graphs/warnings-in-mdl-graphs/warnings-in-mdl-graphs.md)
* [MDL学習リソース](/help/mdl-graphs/mdl-learning-resources/mdl-learning-resources.md)

+++

## 概要

MDLは[Materials Definition Language](http://www.nvidia.com/object/material-definition-language.html)の略です： 「物理ベースのレンダリングソリューション用に物理ベースのマテリアルを定義するために[NVIDIA](https://www.nvidia.com/)によって開発されたテクノロジーです。」 （出典： [NVIDIA MDLドキュメント](https://raytracing-docs.nvidia.com/mdl/index.html)）

この言語を使用すると、完全なマテリアル定義が移植可能になるため、アプリケーションやレンダラーを問わず使用して、一貫した出力を得ることができます。 Substance 3D Designerは現在、*のみ*&#x200B;アプリケーションであり、MDL関数および値の型をMDLグラフのノードとして公開することで、MDL資料のグラフベースのノードオーサリングを提供しています。

マテリアルをオーサリング中に、Designerに埋め込まれ、[3Dビュー](../interface/3d-view/3d-view.md)パネルで使用可能なNVIDIA独自の[Iray](../interface/3d-view/iray/iray.md)レンダラーを使用して、マテリアル&#x200B;*インタラクティブに*&#x200B;の動作をプレビューできます。

MDLグラフは、[Substanceグラフ](../compositing-graphs/substance-compositing-graphs.md)と相補的です。後者の出力&#x200B;*テクスチャ*&#x200B;は、MDLマテリアルによって&#x200B;*サンプリング*&#x200B;され、その動作と外観に影響を与えることができます。

ガイド付き学習パスについては、このドキュメントのセクション&#x200B;*の順番*&#x200B;に従うことをお勧めします。このセクションは、すぐ下にあるMDLグラフリソースのプロパティから始まります。\
飛び込みたくないか？ [MDL学習リソース](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/first-steps-with-mdl-145654095.html)セクションでMDLグラフの使用を開始しましょう。

>[!NOTE]
>
> NVIDIAが作成および管理するすべてのMDL仕様および[MDLハンドブック](http://mdlhandbook.com/)へのリンクが含まれている[NVIDIA MDLドキュメント](https://raytracing-docs.nvidia.com/mdl/index.html)で、材料定義言語の技術的な実装について詳しく説明します。

![MDLグラフのプロパティ](../assets/mdl-main.png "MDLグラフのプロパティ")

*[プロパティ](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)パネルのMDLグラフのプロパティ*

## MDLグラフのプロパティ

### 属性

このセクションには、特定、分類、および作成者の確立を目的としたMDL資料に関する情報が含まれます。

* <b>識別子</b>：このリソースの名前。パッケージ内の親の下で一意である必要があります
* <b>表示名</b>:インターフェイスに表示されるMDLマテリアル名
* <b>アイコン</b>: Designerのライブラリで、このグラフのサムネールとして使用されている画像
* <b>非表示\*</b>:* True*に設定すると、MDLマテリアルはMDLライブラリで表示されませんが、内部に存在し、参照できます
* <b>ライブラリに表示</b>: *True*&#x200B;に設定すると、DesignerのライブラリにMDLグラフが表示されます
* <b>説明</b>: MDLマテリアルの説明。このグラフを参照しているインスタンスノードのツールチップに表示されます
* <b>カテゴリ\*</b>: MDLグラフが属するカテゴリ – これは現在、Designerの[ライブラリ](../interface/the-library/the-library.md)でのグラフの並べ替え方法に影響しません
* <b>グループ\*</b>: MDLマテリアルが属するライブラリグループ
* <b>作成者\*</b>: MDL資料の作成者
* <b>投稿者\*</b>：作成者以外のMDLマテリアルの投稿者
* <b>キーワード\*</b>:ライブラリ検索でMDL資料を検索するために使用されるキーワードです
* <b>著作権表示\*</b> : MDL資料の作成者および使用に関連する著作権表示

注意：アスタリスク(\*)が付いているプロパティは、MDLライブラリ統合で使用されるMDL注釈であり、Designerで*&#x200B;影響なし*です。

### グラフ入力

このセクションでは、MDLグラフの[公開パラメーター](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/exposing-a-parameter-145654033.html)に接続されている対話型パラメーターの一覧を表示し、*既定値*&#x200B;を定義します。 いつでも&#x200B;*調整*&#x200B;および&#x200B;*並べ替え*&#x200B;できます。

これらの入力のインターフェイスと動作は、これらの入力が接続されている公開パラメーターの&#x200B;*値型*&#x200B;と&#x200B;*範囲*&#x200B;で定義されます。 例：

* [0.0,4.0]のソフト範囲に設定された型<b>Float</b>の公開値は、0.0 ～ 4.0の&#x200B;*単一スライダー*&#x200B;として表示されます
* 公開される型<b>Color</b>の値は、選択グラデーションとカラーサムネールを含む&#x200B;*カラーウィジェット*&#x200B;として表示されます

グラフの入力を並べ替えるには、パラメーターの左側にある&#x200B;*暗いハンドル*&#x200B;にカーソルを置き、クリックして&#x200B;*ホールド* <b>LMB</b>し、カーソルを上下にドラッグします。 このカスタム注文は、次のコンテキストでMDL材料のプロパティを表示するために使用されます。

* このマテリアルのMDLグラフを参照するインスタンスノード
* [3Dビュー](../interface/3d-view/3d-view.md)のマテリアルプロパティ
* サードパーティのMDL統合
