---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/exporting-mdl-content.html"
breadcrumb-title: ''
description: Substance 3D DesignerからMDLコンテンツを書き出して、外部レンダラーやアプリケーションで使用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > Exporting MDL content
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDLコンテンツのエクスポート
user-guide-description: ''
user-guide-title: ''
source-git-commit: f320cf6842ff56ac24912ceda264f30c28317c05
workflow-type: tm+mt
source-wordcount: '1144'
ht-degree: 0%

---


# MDLコンテンツのエクスポート

このページでは、[MDLグラフ](../../mdl-graphs/mdl-graphs.md)に関連する書き出しプロセスとSubstance 3D Designerのマテリアルについて説明します。

## 概要

DesignerでMDLマテリアルを作成したら、そのマテリアルを&#x200B;*マテリアルの定義を保持*&#x200B;できるフォーマットにエクスポートし、MDLをサポートするレンダラーで読み取る必要があります。 MDLでは、独自の書式を使用してマテリアル定義を伝送します。これは、MDLモジュールと呼ばれ、さまざまな書式で書き込まれ、パッケージ化されます。これらはすべて、Designer内から書き出すことができます。

>[!NOTE]
>
> これらの形式はすべて、*テキストエディター*&#x200B;で直接開くことができ（場合によっては、アーカイブマネージャーで展開した後）、保有しているマテリアル定義を検査できます。

## MDLモジュール(\*.mdl)

これは、マテリアル定義の基本的な交換ファイル形式です。 MDLモジュールは、次の項目を定義します。

* 物質の特性と挙動
* 公開されたパラメーターとデフォルト値
* その注釈（すなわち、メタデータ）：作成者、タグ、カテゴリ、...

MDLモジュールのエクスポートは、*パッケージ*&#x200B;レベルで実行されます。 特定のパッケージのMDLモジュールをエクスポートするには、[エクスプローラー](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)の![](../../assets/mdl-export-module-icon.png) <b>MDLモジュールのエクスポート</b>ボタンをクリックするか、*パッケージのコンテキストメニュー*&#x200B;で同じオプションを選択します。 エクスポートされたMDLモジュールの対象の場所と名前を選択すると、エクスポート処理中にログに記録されたメッセージの一覧を含む<b>レポートのエクスポート</b>ダイアログが表示されます。

書き出されたモジュールには、パッケージ内の[MDLグラフ](../../mdl-graphs/mdl-graphs.md)で定義されたMDLマテリアル&#x200B;*all*&#x200B;の定義が含まれます。

>[!NOTE]
>
> MDLモジュールについて詳しくは、NVIDIAの[MDL仕様](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9)のセクション4および15を参照してください。

>[!NOTE]
>
> このテンプレートに続く警告： `x appears to be invalid whereas it was expected to be an mdl::call`は、MDLグラフでMDLのデータがどのように処理されるかによって発生し、*無視しても*&#x200B;安全です。

![MDL書き出し経路](../../assets/mdl-export-module.png "MDL書き出し経路")

*エクスプローラーの[MDLモジュールのエクスポート]パス、および結果の[レポートのエクスポート]ダイアログ*

### MDLプリセット(\*.mdl)

MDLモジュールプリセットは、基になるモジュールとほとんど同じですが、異なる既定値のセットを含むという点だけが異なります。詳細については、[こちら](https://www.migenius.com/doc/realityserver/latest/resources/general/iray/api_reference/iray/html/classmi_1_1neuraylib_1_1IMdl__factory.html#details)を参照してください。

シーンマテリアル`my_material`に割り当てられたMDLマテリアルのプリセットは、次の場所からエクスポートできます。

* [エクスプローラー](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)パネル。MDLグラフリソースで<b>RMB</b>をクリックし、コンテキストメニューで「<b>プリセットを書き出し…</b>」オプションを選択します
* [3Dビュー](../../interface/3d-view/3d-view.md)パネルで、<b>マテリアル/my\_material/プリセットを書き出し…</b>メニューオプションを使用します

このメニューオプションを選択すると、<b>MDLマテリアルプリセットを書き出し</b>ダイアログが開き、次のオプションが表示されます。

* <b>ディレクトリ</b>: MDLモジュールのエクスポート先の場所
* <b>MDLファイル名</b>: MDLモジュールの名前
* <b>インポートされたMDLモジュールの埋め込み</b>: MDLモジュールがインポートされたモジュールに依存している場合（モジュール依存関係がある場合など）、このオプションをオンにすると、モジュール依存関係がエクスポートされたMDLモジュールに&#x200B;*埋め込み*&#x200B;され、ファイルサイズや動的継承を犠牲にして、事実上&#x200B;*自給自足*&#x200B;になります

書き出されたプリセットでは、3Dビューのマテリアルのパラメーター&#x200B;*現在の値*&#x200B;が&#x200B;*新しい既定値*&#x200B;値として使用されます。 これらの値は、<b>マテリアル/my\_material/編集</b>オプションを使用して変更できます。このオプションでは、マテリアルの公開パラメーターが[プロパティ](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/parameters-ui-129368153.html)パネルに表示されます。

>[!WARNING]
>
> [エクスプローラー](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)パネルからMDLモジュールをエクスポートすると、パッケージ内のMDLグラフによって定義された&#x200B;*すべての* MDLマテリアルを保持するMDLモジュールが作成されます。[3Dビュー](../../interface/3d-view/3d-view.md)からMDLプリセットをエクスポートすると、MDLモジュールに作成され、メニューの&#x200B;*選択したマテリアル* （この例では`my_material`）に適用されたMDLマテリアルの定義が&#x200B;*のみ*&#x200B;保持されます。

![MDLプリセットの書き出し経路](../../assets/mdl-export-preset.png "MDLプリセットの書き出し経路")

*3Dビューの「プリセットの書き出し」経路と、その結果のMDLマテリアルプリセットの書き出しダイアログ*

## MDLモジュールアーカイブ(\*.mdr)

MDLモジュールアーカイブは、上記のMDLモジュールと、*テクスチャ*&#x200B;やReadmeファイルなどのリソースを、*単一の移動可能なファイル*&#x200B;に結合します。

MDLモジュールアーカイブのエクスポートは、*パッケージ*&#x200B;レベルで実行されます。 特定のパッケージのMDLモジュールアーカイブをエクスポートするには、[エクスプローラー](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)の![](../../assets/mdl-export-module-icon.png) <b>MDLモジュールアーカイブのエクスポート</b>ボタンをクリックするか、*パッケージのコンテキストメニュー*&#x200B;で同じオプションを選択します。 エクスポートされたMDLモジュールアーカイブの対象の場所と名前を選択すると、エクスポート処理中にログに記録されたメッセージの一覧を含む<b>レポートのエクスポート</b>ダイアログが表示されます。

エクスポートされたモジュールアーカイブには、パッケージ内の[MDLグラフ](../../mdl-graphs/mdl-graphs.md)で定義されたMDLマテリアル&#x200B;*all*&#x200B;の定義を保持するMDLモジュールが含まれます。 [Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)が[MDLグラフ](../../mdl-graphs/compositing-graphs-and/substance-compositing-graphs-and-mdl-materials.md)にインスタンス化され、[ルート](../../mdl-graphs/main-mdl-graph-concepts/main-mdl-graph-concepts.md)ノードに移動するストリームに接続されている場合、出力されるテクスチャは&#x200B;*アーカイブに保存*&#x200B;されます。

これらの項目に加えて、アーカイブにはMDLモジュールアーカイブの次のメタデータを説明する<b>MANIFEST</b>ファイルが含まれています。

* `mdl`:モジュールアーカイブのエクスポートに使用されるMDLのバージョンです（例： 「1.5」）
* `version`:モジュールアーカイブのバージョン – 例： 「1.0.0」
* `module`:モジュールアーカイブの名前 – 例： &quot;::pbr\_metallic\_roughness\_basic&quot;
* `exports.material`:モジュールアーカイブで定義されたマテリアルの名前（例： &quot;::pbr\_metallic\_roughness\_basic::MDL\_graph&quot;）

>[!NOTE]
>
> MDLアーカイブファイル形式の詳細については、NVIDIAの[MDL仕様](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9)の付録Cを参照してください。

![MDR輸出経路](../../assets/mdl-export-archive.png "MDR輸出経路")

*エクスプローラーの[MDLモジュールアーカイブのエクスポート]パス、および結果の[レポートのエクスポート]ダイアログ*

## MDLカプセル化モジュール(\*.mdle)

エクスポーズドパラメーターを含むMDLグラフは、カプセル化されたMDL素材として書き出すことができます。 カプセル化&#x200B;*によってデータ*&#x200B;が専用クラスにラップされるため、データ&#x200B;*は直接アクセスできません*。

たとえば、公開されたパラメーターの値を変更してマテリアルの動作を制御することはできますが、カプセル化されたMDLモジュールでは、これらのパラメーターの&#x200B;*定義*&#x200B;は&#x200B;*利用できません*&#x200B;です。

カプセル化されたMDLモジュールの書き出しは、MDLグラフのコンテキストメニューで<b>[書き出し形式] .mdle</b>オプションを選択することにより、MDLグラフレベルの[エクスプローラー](https://helpx.adobe.com/jp/substance-3d/unlisted/documentation/sddoc/the-explorer-129368147.html)で実行されます。 書き出すMDLカプセル化モジュールのターゲットの場所と名前を選択すると、書き出し処理中に記録されたメッセージの一覧を含む<b>レポートの書き出し</b>ダイアログが表示されます。

*のみ* *選択したMDLグラフ*&#x200B;の材料定義は、エクスポートされたカプセル化されたMDLモジュールに含まれます。

>[!NOTE]
>
> カプセル化されたマテリアルの定義について詳しくは、NVIDIAの[MDL仕様](https://developer.download.nvidia.com/designworks/mdl-sdk/secure/MDL_spec_1.6.1_16Dec2019.pdf?__token__=exp=1776166178~hmac=38656bc9d8199764568d1fa0d4d945b90c57638ebd37b100a402bdc983e518ee&t=eyJscyI6ImdzZW8iLCJsc2QiOiJodHRwczovL3d3dy5nb29nbGUuY29tLyJ9)のセクション13.5および[MDL SDK API](https://raytracing-docs.nvidia.com/mdl/api/mi_neuray_example_mdle.html)を参照してください。

![MDLE書き出し方法](../../assets/mdl-export-encapsulated.png "MDLE書き出し方法")

*エクスプローラーの「mdleとして書き出し」パス、および結果の書き出しレポートダイアログ*
