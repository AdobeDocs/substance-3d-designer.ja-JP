---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/publishing-substance-3d-asset-files-sbsar.html"
breadcrumb-title: ''
description: DesignerからSubstance 3Dアセットファイル(SBSAR)を公開して、他のアプリケーションやエンジンで使用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Publishing Substance 3D asset files (SBSAR)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Substance 3D アセットファイル（SBSAR）の公開
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1234'
ht-degree: 2%

---


# Substance 3D アセットファイル（SBSAR）の公開

このページでは、Substance 3D Designerでパッケージを<b>Substance 3Dアセット</b>ファイル（拡張子<b>SBSAR</b>）として公開する方法について説明します。このファイルは、Substanceエコシステム内およびそれをサポートする他のアプリケーションで使用されます。

通常は、ビットマップではなくSubstance 3Dアセットを使用することをお勧めします。その方が、非常に柔軟で軽量であるためです。 Substance 3D [Painter](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/home)、[Sampler](https://helpx.adobe.com/jp/substance-3d-sampler.html)または[Player](https://helpx.adobe.com/substance-3d-player/home.html)で使用している場合は、[&#39;送信先…&#39;機能](../../interface/the-explorer-window/send-to-interoperability/send-to-interoperability.md)を使用すると高速になります。

![単純化されたSBSARファイルの公開](../../assets/exportflow.png "単純化されたSBSARファイルの公開")

## パブリッシュの概念

Substanceグラフを公開する場合は、次の点に注意してください。

* 個々の[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)ではなく、すべての内容を含むパッケージ</b>を公開<b>します。 これにより、Substance 3Dアセットを使用して、このパッケージ内のすべてのSubstanceグラフからコンテンツを作成できるようになります。
* 公開されたパッケージは<b>完全にスタンドアロン</b>です。必要なすべてのリソースがファイルに埋め込まれています。 つまり、SBSファイルよりも簡単に共有できます。
* Substance 3Dアセットからの出力は<b>完全に動的</b>にすることができます。 [解像度が設定されていません。公開されたパラメーターは変更できます。](../../compositing-graphs/compositing-graph-key-con/substance-compositing-graph-key-concepts.md) ただし、グラフの編集はできなくなりました。
* Substance 3Dのアセットは、Designer以外で、すべてのAdobeのSubstance 3D製品、Adobe Dimension、および[Substance連携](https://experienceleague.adobe.com/ja/docs/substance-3d/ecosystem/home)を備えたその他のアプリケーションで使用できます。
* 公開は[書き出し](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)とは異なります。違いをよく理解してください。

## 公開の準備をしています

パブリッシュには、ビットマップの書き出しよりも多くの準備が必要です。 これは、パブリッシュされたSubstance 3Dアセットが、テクスチャの現在の状態の静的なスナップショットだけでなく、動的なツールであるためです。 特に、次の点に留意する必要があります。

* グラフの解像度（[出力サイズ](../../compositing-graphs/output-size/output-size.md)）が&#x200B;*親に相対的* [継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されていることを確認してください。これは、動的であり、その場で変更できることを意味します。
* [グラフ出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)が、名前、ラベル、および使用法タグを使用して正しく設定されていることを確認してください。
* 必要に応じて、[パラメーターが適切に整理され、名前が指定されていることを確認してください](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)。
* グラフにマテリアルが記述されている場合は、その[マテリアルモデル](../graph-parameters/graph-parameters.md)属性をそのマテリアルのモデルに設定します。
* すべての[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードの[出力サイズ](../../compositing-graphs/output-size/output-size.md)プロパティが&#x200B;*絶対* [継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されていることを確認してください。 そうでない場合は、参照されている[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)が、公開されているSubstance 3Dアセットファイルのデフォルトの<b>256\*256</b>解像度で保存されます。これにより、1つ以上の出力の*&#x200B;品質*に影響します。
* Designer以外では使用できないはずのパッケージ内にグラフが存在する場合（例えば、特定のコンテキストでのみ機能するヘルパーや「ツール」サブグラフ）、そのグラフをプロパティ内で非表示に設定します。 詳しくは、以下を参照してください。

## 公開方法

公開の準備ができたら、[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)から公開ダイアログにアクセスします。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

エクスプローラーで、パッケージを右クリックして、![](../../assets/image2020-9-23-9-39-58.png) **Publish .sbsarファイル…**、別のホットキーCtrl + Pを選択します。

ダイアログを1回使って公開した後、![](../../assets/image2020-9-23-11-15-35.png) **Publish .sbsarファイルを以前のファイル**&#x200B;と同様に使用して、ダイアログを表示せずに公開プロセスを繰り返し、同じ設定を使用してすぐに公開できます。

</td>
<td style="border: 0;" valign="top">

![](../../assets/publish-rightclick.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

エクスプローラーで、上部のツールバーにある[Publish]ボタン![](../../assets/image2020-9-23-9-39-58.png)をクリックします。

ダイアログを使って発行した後は、[前の設定でPublish]ボタン![](../../assets/image2020-9-23-11-15-35.png)を使用して、ダイアログが表示されることなく発行プロセスを繰り返し、同じ設定で発行することができます。

</td>
<td style="border: 0;" valign="top">

![](../../assets/publish-toolbutton.gif)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## アセットの公開オプション

Substance 3Dファイル(SBS)を保存していない場合は、「アセットのPublish」オプションが表示される前に、保存するかどうかを確認するメッセージが表示され、Substance 3Dアセットの保存先を確認するメッセージが表示されます。 ファイルに関するメッセージやダイアログが表示され、ファイルの送信が速くなるのを防ぐには、前述の<b>Publishを以前の</b>と同じ方法で使用します。

</td>
<td style="border: 0;" valign="top">

![アセット公開オプション](../../assets/publish-dialog.png "アセット公開オプション")

</td>
</tr>
</table>

次のオプションを使用できます。

<b>ファイルパス</b>では、Substance 3Dアセットファイルの保存先を選択するためのファイルダイアログが開きます。 デフォルトパスは、システムのユーザードキュメントです。 パッケージが保存された場合、パスはパッケージの場所になります。 セッション中にパッケージが公開された場合、パスは最後の公開場所になります。

<b>アーカイブの圧縮</b>アーカイブの圧縮オプションを設定します。ファイルサイズに影響します。

<b>見つからないアイコンを生成</b>では、組み込みの[PBR レンダリング](../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/pbr-utilities/pbr-render/pbr-render.md)手法を使用して、各グラフの属性のサムネイルを作成します。

<b>公開されたグラフ</b>このパッケージで公開されるすべてのグラフを一覧表示します。グラフの除外については、以下を参照してください。

>[!NOTE]
>
> **ランダムシードの露出**
> 
> ランダムシードの露光量設定は、Publishダイアログで使用できなくなりました。 代わりに、[グラフのランダムシード属性が使用可能にならないように、相対ではなく絶対シードに設定してください。](../../compositing-graphs/graph-parameters/graph-parameters.md)

## 公開されたアセットからのグラフの除外

パッケージ内の一部のグラフは、外部での使用を目的としていない場合があります。 これらのサブグラフは、通常、より大きな全体の一部、つまりマスターマテリアルのサブルーチンとして使用されます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

Substance 3Dアセットファイル内でグラフが表示されたり、使用可能になったりしないようにするには、そのグラフのプロパティにアクセスして（グラフビューの空の領域をダブルクリックするか、エクスプローラーでグラフをシングルクリックして）、<b>属性</b>ロールアウトを開きます。 公開時に非表示にするには、<b>SBSARで公開</b>を<b>いいえ</b>に設定します。

</td>
<td style="border: 0;" valign="top">

![](../../assets/image2020-9-23-10-40-21.png)

</td>
</tr>
</table>

### Publishダイアログの警告

Publishダイアログに黄色の警告が表示される場合があります。 一般的なものについては、以下に説明と解決策を示します。

* 1つ以上のグラフに出力がありません\
  この警告は、出力ノードを持たない1つ以上のグラフを含むパッケージを公開しようとしていることを意味します。 解決策としては、黄色の警告三角形を付けたグラフに[出力ノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)を追加します。
* 1 つ以上のグラフに親に相対的でない出力サイズのパラメーターがあります\
  この警告は、1つ以上のグラフが誤った出力サイズに設定されていることを意味します。 通常は、グラフ自体のプロパティです。 この警告は、パブリッシュ時にこのグラフの解像度を動的に制御できないことを意味します。 解決策は、黄色い三角形が付いたグラフのプロパティに移動し、出力サイズの[継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)を&#x200B;*親に対して相対的*&#x200B;に設定します。

## Substance 3Dアセットの制限

Substance 3DアセットはSubstanceエコシステムで最も強力で最もダイナミックなフォーマットですが、注意すべき小さな技術的な制限があります。

* 公開されたSubstance 3Dアセットパッケージは、一方向のファイル形式です。 Substance 3DアセットをSubstance 3Dファイル(SBS)に「逆コンパイル」することはできません。 Substance 3Dアセットを「編集」するには、元のSubstance 3Dファイルを編集する必要があります。 Substance 3Dアセットパッケージのコンテンツは、新しいSubstanceグラフ（開いてドラッグ&amp;ドロップ）内のノードとして引き続き使用できるため、これは大きな制限ではありません。
* Substance 3Dアセットファイルには、互換性を推測するバージョンが含まれています。 コアSubstance engineは、新機能を使用して随時更新されます。 これらの機能を使用するパッケージは、これらの新機能をサポートするアプリケーションで読み取る必要があります。 すべてのSubstanceアプリケーションが同時に更新されるため、これは問題ではありませんが、プラグインと統合の互換性の遅延が長くなる可能性があります。\
  [プロジェクトの環境設定](../../interface/preferences-window/project-settings/project-settings.md)のSubstance engine互換表示オプションを使用して、潜在的な問題を特定します。
* Substance 3Dアセットの一部としてグラフが公開されると、*static*&#x200B;パラメーターなど一部の公開パラメーターが&#x200B;*非表示*&#x200B;になります。 これらのパラメーターの一覧および一般的な静的パラメーターの詳細については、[パラメーターの公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)ページの[制限](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)セクションを参照してください。
