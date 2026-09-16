---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/axf-appearance-exchange-format.html"
breadcrumb-title: ""
description: Substance 3D DesignerでAxFアピアランス交換フォーマットのリソースを読み込んで使用する方法と、マテリアルの読み込み方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Resources > AxF (Appearance eXchange Format)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: AxF（Appearance eXchange Format）
user-guide-description: ""
user-guide-title: ""
source-git-commit: c460f605a97021efd2143941c28a977e12452299
workflow-type: tm+mt
source-wordcount: '2140'
ht-degree: 0%
---

# AxF（Appearance eXchange Format）

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

[![AxF ファイルアイコン](axf-appearance-exchange-format.resources/axf-file-icon.png)](https://www.xrite.com/axf)

</td>
<td width="100.00%" style="border: 0;" valign="top">

Substance 3D Designerでは、[X-RiteのアピアランスeXchange形式がサポートされています。](https://www.xrite.com/axf) 書式の作成者は、この書式を次のように記述します。

AxF ファイルは、デジタルデザインワークフロー全体を通じて、複雑なマテリアル特性をキャプチャ、保存、編集、伝達するために使用されます。 AxFでは、PLM（製品ライフサイクル管理）、CAD（コンピュータ支援設計）、最先端のレンダリング・アプリケーションを通じて、関連するすべての外観データ(色、テクスチャ、光沢、屈折、translucency、特殊効果（輝き）、反射プロパティ)を保存し、共有するための標準的な手段を提供しています。」

</td>
</tr>
</table>

簡単に言えば、AxF ファイルはX-RiteのTAC7スキャナーハードウェアによって抽出された多くのテクスチャと、マテリアルの付加的なプロパティを記述するメタデータをホストします。 つまり、AxFは単なるテクスチャ・データではなく、シェーディング・プロパティも保持します。

AxF ファイルはパッケージ[resource](../../resources/resources.md)としてインポートされていません&#x200B;*1}。*&#x200B;代わりに、[インポートプロセス](#import)では、AxF ファイルからテクスチャとメタデータを抽出し、それらを使用して[専用のテンプレート](#graph-templates)から作成されたグラフを準備します。

使用可能なテンプレートは、次の2つのAxFワークフロー向けです。

* AxF ファイル内のSVBRDF マテリアルを<b>PBR マテリアルに</b>変換しています。
* SVBRDF マテリアルを所定の位置で<b>編集</b>し、新しいレイヤーとして既存のAxF ファイルに[書き出し](#export)します。

>[!NOTE]
>
> サポート対象マテリアルモデル
> 
> <b>SVBRDF</b> （空間的に変化するBRDF）モデルを使用しているマテリアルのみ、Designerで&#x200B;*完全に*&#x200B;読み込んで編集できます。
> 
> <b>EP-SVBRDF</b> (Energy Reserving SVBRDF)モデルを使用するマテリアルを読み込むことはできますが、編集および表示できるのはSVBRDFモデルに存在する機能のみです。 EP-SVBRDF専用の機能はサポートされていません。
> 
> その他のモデルはサポートされていません。

## AxF ファイルの読み込み

AxF ファイルの読み込みワークフローは、次の2つの方法のいずれかから開始できます。

+++ホーム画面

[ホーム画面](../../interface/home-screen/home-screen.md)の左側のセクションで、[<b>AxFのインポート…</b>]ボタンをクリックします。

![AxF:ホーム画面から読み込みを開始](axf-appearance-exchange-format.resources/axf_home-screen.png "AxF:ホーム画面から読み込みを開始"){width="600px"}

+++

+++エクスプローラー

[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)でパッケージの[RMB]をクリックし、パッケージのコンテキストメニューの<b>インポート/AxF</b>に移動します。

![AxF:エクスプローラーからのインポートを開始](axf-appearance-exchange-format.resources/axf_explorer.png "AxF:エクスプローラーからのインポートを開始"){width="600px"}

+++

### 読み込みダイアログ

<b>AxFインポート</b>ダイアログでは、選択したAxFファイルから読み込まれたデータを確認し、意図した編集または変換を実行するために必要なグラフテンプレートを設定できます。

4つのセクションで構成されています。

<b>ヘッダー</b>には、AxFファイルで検出されたマテリアルの名前とその表現（現在、常にSVBRDF）が表示されます。 ファイルに埋め込まれたプレビューサムネイルも表示されます。

「<b>テンプレート</b>」セクションでは、[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)テンプレートを設定して、素材の作業を開始できます。 これらのテンプレートの詳細と設定については、以下の[グラフテンプレート](#graph-templates)のセクションを参照してください。

<b>テクスチャ</b>は、検出されたマテリアルに含まれるAxFファイルから抽出されたすべてのテクスチャを一覧表示します。 各テクスチャの名前、ネイティブ解像度、データフォーマット、物理サイズが表示されます。

<b>メタデータ</b>と<b>プロパティ</b>には、AxFファイルのマテリアルから抽出されたデータが一覧表示されます。 これらは、一部のSubstanceグラフテンプレートのプロパティの構成方法に影響を与えます（以下の[グラフテンプレート](#graph-templates)セクションを参照）。

![AxF:ダイアログのインポート](axf-appearance-exchange-format.resources/axf_import.png "AxF:ダイアログのインポート")

### 結果

[<b>OK</b>]ボタンをクリックすると、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)にパッケージが作成されます。 このパッケージには、次のリソースが含まれています。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>Resources</b>フォルダーは、AxFファイルからインポートされたマテリアルごとに&#x200B;*サブフォルダー*&#x200B;をホストします。

各サブフォルダーには、そのマテリアルのAxFファイルから抽出された&#x200B;*テクスチャ*&#x200B;を含む別のサブフォルダーが含まれています。 この最後のサブフォルダーの名前は、テクスチャによって使用されるマテリアル&#x200B;*表現*&#x200B;にちなんで付けられています（現在は<b>SVBRDF</b>のみ）。

インポートダイアログの<b>テンプレート</b>セクションで設定された各テンプレートのグラフです。\
[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)の場合、AxFファイルから抽出されたテクスチャとデータ、および選択したテンプレート設定で事前に構成されます（以下のグラフテンプレートセクションを参照）。

</td>
<td style="border: 0;" valign="top">

![AxF:インポートプロセスのパッケージ結果](axf-appearance-exchange-format.resources/axf_package.png "AxF:インポートプロセスのパッケージ結果")

</td>
</tr>
</table>

## グラフテンプレート

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)には、AxFワークフロー専用のグラフテンプレートがあります。

「<b>テンプレートを追加</b>」ボタンをクリックし、ドロップダウンメニューで目的のグラフの種類を選択します。

</td>
<td style="border: 0;" valign="top">

![AxF:インポートダイアログにテンプレートを追加](axf-appearance-exchange-format.resources/axf_add-template.png "AxF:インポートダイアログにテンプレートを追加")

</td>
</tr>
</table>

### Substanceグラフテンプレート

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Substanceグラフテンプレートには、次の2種類があります。

<b>AxFからメタリックへの粗さ</b>および<b>AxFからSpecularへの光沢</b>は、*変換*&#x200B;テンプレートであり、AxFマテリアルを標準のPBRモデルにマップできます。\
これらのマテリアルは、デフォルトの3Dビューシェーダーで使用したり、Designerの[Sampler](https://www.adobe.com/products/substance3d-sampler.html)で作成された他のPBRマテリアルや、[3Dアセット](https://substance3d.adobe.com/assets/)ライブラリから取得した他のPBRマテリアルと組み合わせたりできます。

<b>AxFからAxF</b>は、*パススルー*&#x200B;のテンプレートです。このテンプレートを使用すると、AxFマテリアルを所定の位置で編集し、これらの変更を既存のAxFファイル内の新しいレイヤーとしてエクスポートできます。 詳しくは、以下のAxFファイルのエクスポートを参照してください。

</td>
<td style="border: 0;" valign="top">

![AxF: Substanceグラフテンプレート](axf-appearance-exchange-format.resources/axf-templates.png "AxF: Substanceグラフテンプレート")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>テンプレート</b>の一覧に追加されたすべてのSubstanceグラフテンプレートに対して、次の操作が実行されます。

AxF ファイルから抽出されたテクスチャの&#x200B;*識別子*&#x200B;に&#x200B;*usage*&#x200B;が一致する[Input](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input-color/input-color.md)ノードの場合、そのノードは、その入力ノードを参照している[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md) テクスチャに置き換えられます。

グラフの<b>Resolution</b>プロパティ（つまり出力サイズ）は、抽出された&#x200B;*最大*&#x200B;テクスチャの解像度以上の2の累乗に自動的に設定されます。

[Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノード&#39; <b>Resolution</b>プロパティ（つまり、出力サイズ）は、前の操作が適用された後、グラフと一致するように自動的に設定されます。

グラフの<b>物理サイズ</b>プロパティは、*最初*&#x200B;に抽出されたテクスチャの物理サイズに設定されています。

グラフのパラメーターの&#x200B;*既定値*&#x200B;は、AxFファイル内のデータと一致するように設定されています。

AxFファイルのマテリアルから抽出された&#x200B;*メタデータ*&#x200B;は、グラフの<b>説明</b>プロパティにコピーされます。

>[!IMPORTANT]
>
> グラフのパラメータのデフォルト値は、この初期設定後は変更しないでください。
> 
> テクスチャの値を正しく解釈するために必要なシェーディングプロパティを指定します。
> 
> そのため、これらの設定を変更すると、[3Dビュー](../../interface/3d-view/3d-view.md)でマテリアルを表示するときに正しくレンダリングされません。

</td>
<td style="border: 0;" valign="top">

![AxF: Substanceグラフパラメーター](axf-appearance-exchange-format.resources/axf_graph-props.png "AxF: Substanceグラフパラメーター")

</td>
</tr>
</table>

## AxFファイルのエクスポート

既存のAxFファイルは、Designerから適切な場所で編集できます。[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)の[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)を使用して、そのリソースが更新されます。

グラフ出力をAxFファイルに書き出す機能を使用すると、Designerの一般的なAxFワークフローは次のようになります。

1. AxFファイルのインポート
1. [AxFからAxF]Substanceグラフテンプレートを使用する
1. Substanceグラフで使用可能なフィーチャとノードを使用して、抽出されたテクスチャを編集します
1. グラフ出力を同じAxFファイルにエクスポートします

グラフの<b>物理サイズ</b>プロパティを使用して、編集したAxFファイルの更新されたテクスチャの<b>物理サイズ</b>属性を設定します。

>[!NOTE]
>
> ファイル内のリソースへの変更は、*新しいレイヤー*&#x200B;として追加されます。 つまり、Designerから同じAxFファイルに書き出すたびに、そのファイルのサイズが大きくなります。

![AxFのエクスポート](axf-appearance-exchange-format.resources/exportaxf.gif)

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

### 書き出しダイアログ

<b>AxF</b>書き出しダイアログは、<b>出力の書き出し</b>ダイアログで専用タブとして使用できます。

[グラフビュー](../../interface/the-graph-view/the-graph-view.md)ツールバーで、![](axf-appearance-exchange-format.resources/tools.jpg) <b>ツール</b>メニューを開き、[<b>出力のエクスポート…</b>]オプションを選択してダイアログを表示し、[<b>AxF</b>]タブを選択します。

</td>
<td width="100.00%" style="border: 0;" valign="top">

![AxF:グラフビューのツールバーの[エクスポート]オプション](axf-appearance-exchange-format.resources/axf_graph-export.png "AxF:グラフビューのツールバーの[エクスポート]オプション")

</td>
</tr>
</table>

このダイアログには、次の3つの主要なセクションがあります。

<b>ファイル</b>入力フィールドでは、編集する必要があるターゲットAxFファイルを選択できます。 このファイルが読み込まれ、チェックされます。有効な場合は、そのデータを使用して以下の「AxFリソース」列にデータが入力されます。

<b>マップされた出力</b>は、出力列のグラフ出力を一覧表示し、それらの&#x200B;*使用方法*&#x200B;を、同じ&#x200B;*識別子*&#x200B;を共有する対象ファイル内のAxFリソースと一致させます。 検出された問題は、警告（黄色）またはエラー（参照番号）として「Notes」列に表示されます。

<b>マップされていない出力</b>は、マップできなかったグラフ出力とターゲットファイル内のAxFリソースを一覧表示します。 これらの出力は無視され、これらのAxFリソースは変更されません。

>[!NOTE]
>
> グラフ出力をこのダイアログに一覧表示するには、グラフ出力の<b>Group</b>プロパティを&#39;AxF&#39;に設定する必要があります。

![AxF：書き出しダイアログ](axf-appearance-exchange-format.resources/axf_export.png "AxF：書き出しダイアログ")

<b>書き出しの開始</b>をクリックして、マップされた出力の変更を含む新しいレイヤーでターゲットAxFファイルを編集します。

結果は、ダイアログのステータスバーのプログレスバーの横にメッセージとして表示されます。

>[!TIP]
>
> 書き出しを実行するたびに、ターゲットファイルに新しいレイヤーが作成されます。 したがって、ファイルのサイズと複雑さを管理するために、意図的に意図的に書き出すことを忘れないでください。

### AxFリソースへの出力のマッピング

既存のAxF ファイルに書き出す場合、そのリソースはグラフ出力を使用して更新されます。 Designerは、<b>Usage</b>と同じ識別子を持つ[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードとリソース識別子を一致させます。

さらに、出力の<b>グループ</b>のプロパティ&#x200B;*は、AxF書き出しダイアログに一覧表示されるために、&#39;AxF&#39;に設定する必要があります（上記参照）。*

![AxF: Substance グラフの出力使用状況](axf-appearance-exchange-format.resources/axf_output_usage.png "AxF: Substance グラフの出力使用状況")

リソースは、テクスチャ（ビットマップ）またはユニフォーム（値）で、チャンネル数を指定できます。 グラフ出力は、そのチャンネル数と正確に一致することが必須です。 そうでない場合は、エクスポート中にそのリソースに対してエラーが発生し、リソースは変更されません。

チャンネル数は、出力ノードに提供されるデータのタイプによって異なります。

* <b>ビットマップ(テクスチャ):</b> [Components](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)プロパティは、チャンネル数を指定するために使用されます。ここで、Rは1チャンネル、RGは2チャンネルです。 このプロパティは、カラービットマップのRGBAチャンネルのうち、リソースにエンコードする必要のあるものをDesignerに通知するために使用されます。
* <b>値（均一）:</b>ベクトル値のコンポーネントの数は、チャンネルの数を指定するために使用されます。[浮動小数](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)は1チャンネル、[浮動小数2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)は2チャンネルです。

>[!IMPORTANT]
>
> <b>AxFからAxF</b>へのグラフテンプレートで、<b>Specularローブ</b>の貢献度の[Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードは既定で&#x200B;*シングルチャンネル*&#x200B;に構成されています（つまり、Componentsプロパティが&#39;R&#39;に設定されています）。\
> 読み込んだAxF ファイルがSpecularローブリソースで複数のチャンネルを使用している場合は、出力の<b>Components</b>プロパティを適宜設定してください。
> 
> たとえば、2つのチャンネルを使用するSpecularローブリソース（Specularラフネスは赤、Specular異方性は緑）の場合、コンポーネントプロパティを&#39;RG&#39;に設定します。

## 3D ビュー内のAxF ファイルの表示

[3D ビュー](../../interface/3d-view/3d-view.md)のAxF SVBRDFマテリアルをレンダリングする方式は、[インポート設定](#import)によって異なります。

+++PBRに変換

AxF ファイルのSVBRDFマテリアルを標準のPBRマテリアルに変換する場合、読み込み設定には[Substanceグラフ変換テンプレート](#graph-templates)が含まれる可能性があります。

その場合、3D ビューで&#x200B;**OpenGLレンダラー**&#x200B;を使用し、<code>AxF SVBRFを選択する必要があります</code> シェーダー。\
次に、読み込みダイアログで設定したグラフをドラッグ&amp;ドロップして、出力をシェーダーに接続できます。

![AxF:コンバージョン用に表示](axf-appearance-exchange-format.resources/axf-view-for-convert.gif "AxF:コンバージョン用に表示")

+++

+++同じ位置で編集

既存のAxF ファイルに対して&#x200B;*編集*&#x200B;を行うことを目標としている場合は、以下の手順に従って、選択したレンダラーに応じてSVBRDF マテリアルを視覚化します。

次のAxF ファイルのGLSLFX表現を使用してマテリアルを視覚化するために、専用のSVBRDF シェーダーが利用できます： <b>AxF SVBRDF</b>。

シェーダーは<b>マテリアル</b>メニューで使用できます。シーンのマテリアル （既定では&#39;Default&#39;）のサブメニューを開き、<b>AxF SVBRDF</b>エントリで任意の手法を選択します。

同じサブメニューの<b>編集</b>オプションを使用して、[プロパティ](../../interface/properties/properties.md)ドックのシェーダーのプロパティを表示します。\
特に、<b>タイリング</b>プロパティを使用すると、モデル上のテクスチャのタイリングを調整できるので、マテリアルを適切なスケールで視覚化できます。

シェーダーを選択した後、グラフの空き領域で[元のデータ]をクリックし、[<b>3D ビューに出力を表示</b>]オプションを選択して、出力を[3D ビュー](../../interface/3d-view/3d-view.md)で表示します。

![AxF: SVBRDF GLSLFX シェーダー](axf-appearance-exchange-format.resources/axf_glslfx-svbrdf.png "AxF: SVBRDF GLSLFX シェーダー"){width="600px"}

このシェーダーは現在&#x200B;*進行中*&#x200B;であり、一部の機能はまだサポートされていません。 したがって、マテリアルの特性の概要を示すことはできますが、微調整には使用しないでください。

同じサブメニューの<b>編集</b>オプションを使用して、[プロパティ](../../interface/properties/properties.md)ドックのシェーダーのプロパティを表示します。\
特に、<b>タイリング</b>プロパティを使用すると、モデル上のテクスチャのタイリングを調整できるので、マテリアルを適切なスケールで視覚化できます。

シェーダーを選択した後、グラフの空き領域で[元のデータ]をクリックし、[<b>3D ビューに出力を表示</b>]オプションを選択して、出力を[3D ビュー](../../interface/3d-view/3d-view.md)で表示します。

![AxF:エディション用に表示](axf-appearance-exchange-format.resources/axf-view-for-edit.gif "AxF:エディション用に表示")
<i>注意： </i> IrayレンダラーとMDLのサポートは、バージョン16.0.0でDesignerから<i>削除</i>されたため、最後までスイッチからIrayレンダラーへのビデオの一部を無視してください。

+++

### サポートされるモデルバリアント

3D ビューで使用されるシェーダは、Specular、フレネル、クリアコートのトランスミッションモデルに対して次のバリエーションをサポートしています。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">
<b>Specularバリアント</b>

* Ward / Geisler-Moroder 2010
* GGX/Walter2007
* GGX / Ross 2005

</td>
<td style="border: 0;" valign="top">
<b>フレネルのバリエーション</b>

* シュリック1994
* シュリック1994色付き
* シンプルフレネル

</td>
<td style="border: 0;" valign="top">
<b>クリアコートの透過バリエーション</b>

* 屈折ディラック&#x200B;*（OpenGLのみ）*
* 屈折ディラック/立体角圧縮なし&#x200B;*（OpenGLのみ）*
* 非屈折ディラック
* 非屈折型ディラック/DSPBR 2020x
* GGX

</td>
</tr>
</table>
