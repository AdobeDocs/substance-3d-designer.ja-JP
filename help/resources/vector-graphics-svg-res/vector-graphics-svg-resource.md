---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/vector-graphics-svg-resource.html"
breadcrumb-title: ''
description: ベクターグラフィックをSubstance 3D Designerに読み込んでリソースとして使用し、プロシージャルのマテリアルを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Resources > Vector graphics (SVG) resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベクターグラフィック（SVG）リソース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '728'
ht-degree: 2%

---


# ベクターグラフィック（SVG）リソース

Substance 3D Designerは、スケーラブルベクターグラフィックフォーマットを通じて、限られた形式のベクターグラフィックをサポートしています。 SVGファイルは、様々な方法でリソースとして取り込み、グラフのリソースとして使用できます。

SVGファイル[は、アトミックSVGノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)を使用して作成または編集できます。また、[UVからSVGへのベイカー](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/convert-uv-to-svg)を使用して作成することもできます。

>[!NOTE]
>
> Adobe Illustrator (**.ai**)ファイルは現在&#x200B;*サポートされていません*。

## SVGストレージ

SVGストレージは、リンクされているか、インポートされているかによって異なります。 読み込んだSVGファイルはSBSファイルに埋め込まれ、[ビットマップなどの外部ファイルは不要](../../resources/bitmap-resource/bitmap-resource.md)です。また、[ベクター編集ツール](../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)を使用して編集できます。

## SVG属性

パッケージ内のSVGリソースには、カスタマイズ可能な属性が多数用意されています。 ほとんどのアトリビュートには大きな目的がなく、ライブラリフィルタ用ですが、レンダリング品質に影響を与えるものはほとんどありません。

| 属性名 | 目的 |
| --- | --- |
| 識別子 | パッケージ内のSVGリソースを参照するために使用されるリソースは、一意である必要があります。 |
| ファイルパス | リソースによって参照されるSVGファイルのディスク上のパスです。 |
| 説明 | このリソースの[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)および[ライブラリ](../../interface/the-library/the-library.md)のツールヒントに表示された説明です。 |
| カテゴリ | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| ラベル | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| 作成者 | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| 作成者の URL | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| タグ | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| ユーザーデータ | オプションの追加データ。ベクターグラフィックでは使用されません。 |
| ライブラリで表示 | [ライブラリビュー](../../interface/the-library/the-library.md)でSVGリソースを非表示にするかどうかを指定します。 |
| ベクターグラフィック品質 | レンダリング品質に影響します。 範囲はリニアではなく、0.5で最高品質が達成されます。 |

## SVG作成

サポートされる機能が限られているため、オーサリングSVGには制限があります。

一般に、次の条件が当てはまります。

* 正しく描くことが保証されているのは、単純なプリミティブのシェイプとパスだけです。
* ストロークはサポートされていますが、結果として1ピクセル幅のストロークになるだけで、ストロークのスタイル設定は無視されます。
* 破線スタイルは必ず破れます。
* レンダリングするには、テキストをパス/アウトラインに変換する必要があります。
* [複合パス](https://helpx.adobe.com/ie/illustrator/using/combining-objects.html#compound_paths)はサポートされていません。
* グラデーションなどの高度な機能はサポートされていません。
* CSSプロパティのスタイル要素はサポートされていません。

## 推奨される書き出しオプション

書き出しオプションは、アプリケーションごとに少し異なります。

### Adobe Illustrator

[Illustrator](https://www.adobe.com/products/illustrator.html)では、以下のオプションに注意を払う場合、SVGの書き出しを最大限に制御できます。

* <b>名前を付けて保存</b>のみを使用してください。名前を付けて書き出しは&#x200B;*使用できません。*
* <b>SVGプロファイル</b>は特に重要ではありませんが、小さなプロファイルは間違いなく正しい設定にデフォルトで（ほとんどの場合）設定されます。
* 有効にするには、<b>フォント</b>を<b>アウトラインに変換</b>に設定する必要があります。
* <b>CSSプロパティ</b>は、スタイル要素に&#x200B;*ではなく*&#x200B;設定する必要があります。他のすべてのオプションは機能します。
* 「<b>Illustratorの編集機能を保持</b>」をオフにします。
* 「<b>レスポンシブ</b>」をオフにします。
* ストロークは正常に機能しません。<b>オブジェクト/パス/パスのアウトライン</b>を使用して、ストロークを表示します。

右側の図は、推奨される書き出しオプションを示しています。これをクリックすると、フルサイズで表示されます。

>[!IMPORTANT]
>
> アートボードは、生成されたSVGファイルの結果に影響を与える場合があります。 一部のIllustratorファイルテンプレートには、複数のアートボードが含まれています。\
> SVGとして保存する場合は、適切にトリミングされた1つのアートボードのみを用意し、アートボードウィンドウでそのアートボードを選択するようにしてください。

![Illustrator SVGの書き出しオプション](../../assets/svg-export-options-ai.jpg "Illustrator SVGの書き出しオプション"){width="512px"}

### Inkscape

InkscapeはSVGとしてネイティブに保存されますが、ファイルフォーマットの制御は少なくなります。 Inkscapeファイルは主にアプリケーションでネイティブに動作しますが、いくつかの制限があります。

* Substance 3D Designerでは、線の幅は1 pxまでしか表示されません。<b>パス/パスの線</b>を使用して、動作させることができます。
* テキストは機能しません。テキストを機能させるには、<b>パス/パスのオブジェクト</b>を使用してください。

### Adobe Photoshop

Photoshopには、非常に限られたSVGエクスポーターがあります（<b>ファイル/書き出し/書き出し形式…</b>） 現在、Substance 3D Designerで正しい結果を生成できません。 シェイプとパスの情報を取得できますが、スタイルは常に要素として保存されます。これは互換性がありません。

単純な白黒のシェイプマスクに使用できます。解決策は、[Alphaの分割](../../compositing-graphs/nodes-reference-for-com/node-library/filters/channels/alpha-split/alpha-split.md)を使用して、SVGからAlphaを取り出すことです。

または、Photoshopで書き出したSVGを[読み込み済み](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)にすることもできます。この場合、[アプリケーション内でスタイル情報をネイティブに編集](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)できます。
