---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/overview.html"
breadcrumb-title: ''
description: Substance 3D Designerの概要を説明し、プロシージャルなマテリアルやテクスチャを作成するための機能について説明します。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Overview
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 概要
user-guide-description: ''
user-guide-title: ''
source-git-commit: e42fdff3a7e8fca5a6d482bee42bb9f32d019c56
workflow-type: tm+mt
source-wordcount: '929'
ht-degree: 2%

---


# 概要

[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)は、ノードベースのインターフェイスで2Dテクスチャ、マテリアル、およびフィルターを作成することを目的としたアプリケーションで、プロシージャルな作成、パラメーター化、非破壊的なワークフローに重点を置いています。 これはSubstance 3Dエコシステムで最も長く使用されているアプリケーションであり、それを使用して作成されたリソースは最も汎用性が高く、動的です。

他のアプリケーションと比較した結果は次のとおりです。

|  | <div><img alt="Substance 3D Samplerアイコン" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c1_position_position-par_image_713298714" src="../../assets/sa-appicon-noshadow-256.png" title="Substance 3D Samplerアイコン" width="64px"/></div>  Substance 3D Sampler | <div><img alt="Substance 3D Painterアイコン" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c2_position_position-par_image" src="../../assets/pt-appicon-noshadow-256.png" width="64px"/></div>  Substance 3D Painter | <div><img alt="Substance 3D Designerアイコン" class="" data-preserve-html="true" id="root_content_flex_items_position_position-par_dynamic_grid_items_grid-cell_position-par_dx_table_row-r0-column-c3_position_position-par_image" src="../../assets/ds-appicon-noshadow-256.png" title="Substance 3D Designerアイコン" width="64px"/></div>  Substance 3D Designer |
| --- | --- | --- | --- |
| <b>学習曲線</b> | 低 | 中 | 高 |
| <b>資料の作成</b> | はい | はい | はい |
| <b>3Dモデルの作成</b> | いいえ | 制限付き\* | 制限付き\* |
| <b>フィルター、パターン、エフェクトの作成</b> | いいえ | 制限付き | はい |
| <b>パラメトリックコンテンツの書き出し</b> | いいえ | いいえ | はい |

\*: ディスプレイスメントのみ。[3Dビュー](../../interface/3d-view/3d-view.md)セクションの<b>シーンの書き出し</b>機能を参照してください。

つまり、Substance 3D Designerは最も技術的で高度なテクスチャリングアプリであるといえます。

これにより、ほぼすべてのユースケースまたはシナリオのコンテンツを作成できます。 つまり、UVマップされたメッシュに固有のマテリアルやテクスチャのセットなど、単一のタイプの出力に限定されず、より広範な用途に向けてコンテンツを作成できます。

例えば、PainterおよびSamplerの手続き型スマートコンテンツのほとんどは、Designerで作成して書き出されています。 ブラシAlpha、ジェネレーター、フィルター、ベースマテリアルなどは、すべてDesignerで作成できます。

## ワークフロー

Substance 3D Designerは、様々な複雑さで様々な方法でコンテンツを構築できるノードベースのエディターです。 [ワークフローについては専用ページ](../../getting-started/workflow-overview/workflow-overview.md)で詳しく説明しますが、ソフトウェアを使用すると次のような利点があります。

<b>[ノンリニア](../../compositing-graphs/substance-compositing-graphs.md) </b>：一度に多数のテクスチャ出力を作成できます。 1つのマスクまたはスライダーを編集すると、自動的に接続された出力が再計算されます。 ベースカラー、ラフネス、法線などのマップを個別に作成する必要がなくなりました。

<b>[非破壊的](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) </b> ：作業内容を失うことなく、*任意のアクションを元に戻すことができます。* 反復処理と実験が大幅に高速化され、さらに効率的なワークフローが見つかります。

<b>[統合されたベイク処理](../../bakers/bakers.md) </b>:ソフトウェア内から高度で高速なメッシュベイク処理ツールにアクセスできます。 ベークは別のソフトウェアで行う必要がなくなり、読み込みや書き出しのプロセスに時間がかかります。

<b>[パラメトリック](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md) </b>: 1つのスライダーまたはドロップダウンを使用して、テクスチャのほぼすべての側面を制御するように設定できます。 これにより、1つのアセットに無限のコントロールとバリエーションを追加できます。

## Filetypes

アプリケーションとそのエコシステムは、4つの異なるファイルタイプを使用します。 消去する必要があるファイルの種類は<b>Substance 3D Designerからエクスポート</b>され、一部のアプリケーションまたは他のすべてのSubstance 3Dアプリケーションにインポートできます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../assets/ds-sbs-48.png)

### Substance 3Dファイル

*(\*.SBS)*

Substanceファイルは、Designerの&#x200B;**メインソースファイル**&#x200B;です。 Substanceファイルを開くと、**グラフ内のすべてのノードを表示および編集**&#x200B;できます。 これらはパッケージとして表され、グラフ、関数、ビットマップ、メッシュなどの任意の数のリソースを含むことができます。共有するのが難しく、計算するのが遅くなります。 Substance 3D DesignerおよびSubstance Playerでのみ開くことができます。

</td>
<td style="border: 0;" valign="top">

![](../../assets/sbsar-48.png)

### Substance 3D アセット

*(\*.SBSAR)*

Substanceアーカイブは<b>個のコンパイル済み最適化された</b>個のSubstanceファイルです。 計算が非常に高速で、参照問題なく簡単に共有できます。 パラメーターはまだ微調整できますが、グラフの編集は<b>ロックされています</b>。 Substanceアーカイブは、すべてのSubstance 3Dアプリケーション、およびAutodesk 3DS Max &amp; Maya、Unreal Engine、Unity Engineなど、[Substance 3Dと連携](https://experienceleague.adobe.com/en/docs/substance-3d/ecosystem/home)するアプリケーション（外部プラグインを含むものもあります）で使用できます。

</td>
<td style="border: 0;" valign="top">

![](../../assets/bmp-96.png){width="48px"}

### 静的ファイル

*（\*.TGA, \*.BMP, \*.PNG, \*.FBX, \*.OBJなど）*

Substance 3D Designerでは、静的ファイル形式への書き出しが常にサポートされています。 2Dイメージはビットマップファイルに書き出すことができ、3Dモデルは一般的な3Dファイルタイプに書き出すことができます。 静的ファイルにエクスポートすると、**すべての動的機能が失われます**。 画像は解像度でロックされ、3Dモデルはpolycountでロックされています。

</td>
</tr>
</table>

これは通常、Designer内で作業する場合は作品をSBS形式に保ち、ターゲットがサポートしている場合（Painterなど）はSBSARに書き出し、SBSARのサポートがない、または必要がない場合は静的ビットマップファイルを使用することを意味します。

## リソースの種類

Substance 3Dファイルには、様々な目的を持つ様々なリソースを含めることができます。 一部のリソースはDesigner内でのみ作成でき、一部のリソースは外部アプリケーションから取得されます。

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/graph-5.png){width="150px"}](../../compositing-graphs/substance-compositing-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Substance グラフ

Substanceグラフを使用すると、*2D画像データ*&#x200B;を生成して処理し、1つまたは複数のテクスチャ出力に出力できます。 多くの場合、プロジェクトは1つまたは複数のSubstanceグラフを中心に展開されます。

[Substanceグラフ専用のセクションに移動します。](../../compositing-graphs/substance-compositing-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/function-1.png){width="150px"}](../../function-graphs/function-graphs.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### Substance関数グラフ

<b>関数</b>は、抽象化および複雑さのレベルが高くなっています。画像データ（ピクセル値のセット）を処理するのではなく、*単一の値* （整数、浮動小数点、ベクトル）を処理します。 関数は、より複雑な操作を行う場合や、特定の動作を微調整する場合に使用します。 通常、関数はスタンドアロンでは動作せず、Substanceグラフのコンテキスト外では使用されません。

[Substance関数グラフ専用のセクションに移動します。](../../function-graphs/function-graphs.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="16.67%" style="border: 0;" valign="top">

[![](../../assets/folder-4.png){width="150px"}](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
<td width="100.00%" style="border: 0;" valign="top">

### グラフ以外のリソース

グラフ以外のリソースは、外部アプリケーション（PhotoshopやAutodesk Mayaなど）から提供される場合もありますが、*Designer内で作成*&#x200B;される場合もあります。 主な違いは、これらはノードベースのグラフではなく、前述のグラフタイプの内部または横で使用する要素であることです。

次のリソースタイプが存在します。

* [ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)
* [ベクターグラフィック(SVG)](../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)
* [3Dシーン](../../resources/3d-scene-resource/3d-scene-resource.md)
* [フォント](../../resources/font-resource/font-resource.md)
* [AxFファイル](../../resources/axf-appearance-exchange/axf-appearance-exchange-format.md)

</td>
</tr>
</table>
