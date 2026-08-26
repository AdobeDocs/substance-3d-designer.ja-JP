---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/importing-linking-and-new-resources.html"
breadcrumb-title: ''
description: Substance 3D Designerでマテリアルプロジェクト用にリソースを読み込み、リンクし、新しいリソースを作成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Resources > Importing, linking and new resources
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 新しいリソースの読み込み、リンクおよび追加
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 2%

---


# 新しいリソースの読み込み、リンクおよび追加

[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)では、グラフで使用するリソースを3つのモードで取り込んだり、新しいリソースを作成したりできます。 これらのリソースには、[ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)、[ベクターグラフィックス](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)、[3Dシーン](../3d-scene-resource/3d-scene-resource.md)および[フォント](../../resources/font-resource/font-resource.md)など、様々な種類があります。 このページでは、様々な方法と、それらが最適に使用されるタイミングについて説明します。

すべてのメソッドにアクセスするには、ExplorerでパッケージのRMBをクリックします。

次の表では、各メソッドの機能の違いについて簡単に説明します。

|                                                                                                                                                                         | 新規 | 読み込み | リンク |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| グラフ([Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)、[Substance関数グラフ](../../function-graphs/function-graphs.md) | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| [ビットマップ](../../resources/bitmap-resource/bitmap-resource.md),[ベクターグラフィックス(SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md) | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 3Dシーン、[フォント](../../resources/font-resource/font-resource.md) | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| SBSファイルの横に作成されます | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| Designerで編集可能 | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> |
| 外部編集は自動的に同期されます | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（エラー）" data-preserve-html="true" src="../../assets/error.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> |
| 公開されたSBSARに埋め込まれています | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> | <div><img alt="（ティック）" data-preserve-html="true" src="../../assets/check.svg"/></div> |

## 新しいリソース

新しいリソースを作成すると、パッケージ内のリソースが最初から作成されます。 Designerのみのリソースは、SubstanceグラフやSubstance関数グラフなど、この方法でのみ作成できます。

特殊なケースとして、新しい[ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)または[リソース](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)を作成した場合があります。これらのファイルは、エクスプローラーに表示され、インポートされたSVGのように動作しますが、外部ファイルは必要ありません。 これらはDesignerで変更できます。 この方法で作成した新しいビットマップとSVGは、外部の編集機能に頼る必要がない場合に適しています。例えば、すばやくシンプルなベクターシェイプや、ペイントされた2Dビットマップマスクが必要な場合です。

## 読み込んだリソース

リソースをインポートすると、リソースファイルの複製がSBSファイル（*Graphname*.resourcesフォルダー内）、[SVGファイルを除く](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)の横に作成されます。 また、リソースの「埋め込み」とも呼ばれます。

読み込んだリソースは、グラフに配置した後、[2Dビュー](../../interface/2d-view/2d-view.md)の[ビットマップペイントツール](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)または[ベクター編集ツール](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)を使用してDesignerで編集できます。 読み込んだリソースは、元のソースファイルにリンクされなくなります。つまり、読み込んだ元のファイルを変更、削除、または更新しても、Designerのリソースには影響しません。

[AxFファイル](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)の場合、プロセスは少し複雑です。SubstanceグラフとビットマップリソースはAxFパッケージから作成されます。 ただし、これらはすべて、それぞれのエディター（グラフビューまたは2Dビュー）で引き続き編集できます。

>[!WARNING]
>
> 新しいパッケージの場合、インポートされたリソースと新しいリソースは、パッケージを保存するまでディスクに保存されません。

## リンクされたリソース

リソースをリンクすると、Designerはディスク上の元の場所にあるソースファイルを参照しますが、パッケージの一部であるかのようにエクスプローラーに表示されます。 実際のリソースをDesigner内で直接編集することはできません。グラフのコンポーネントまたはベイク処理マップのソースとしてのみ使用してください。

Designerで同時に作業しながら、外部エディターを使用してリソースを更新する必要がある場合は、リンクが最適です。 ベイク処理マップが代表的な例です。Designerのリファレンスビットマップを外部ベイク処理アプリケーションとして使用すると、これらのファイルが変更されるとすぐに、グラフが自動的にリロードされ、更新されます。 同様に、3Dシーンはリンクすることしかできないため、3Dアプリケーションから新しいFBXファイルを書き出すたびに、Designerでは3Dビューで使用されているメッシュが自動的に更新されます。 このメッシュからマップをベイク処理する場合は、ベイク処理を手動で開始する必要があります。理想的には、RMBをクリックして「すべてのベイク済みマップをリフレッシュ」を選択します。

## リソースの削除

パッケージからリソースを削除するときに、<b>項目の削除の確認</b>ダイアログが表示されます。 [Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)で使用されている[グラフインスタンス](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)および[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)など、削除中のアイテムが他のリソース&#x200B;*で*&#x200B;参照されている場合、ダイアログにこれらのアイテムの&#x200B;*警告と一覧*&#x200B;が表示されます。

>[!NOTE]
>
> パッケージからアイテムを削除した結果、*依存関係が壊れていることを予測*&#x200B;するために、これらのアイテムに注意して必要なアクションを実行することをお勧めします。\
> これらのアクションには、削除前にこれらのリソースの&#x200B;*すべての使用を削除*&#x200B;することが含まれる場合があります。

![&#39;使用中のリソースが削除されました&#39;警告](../../assets/confirm-item-removal.png "&#39;使用中のリソースが削除されました&#39;警告"){width="512px"}
