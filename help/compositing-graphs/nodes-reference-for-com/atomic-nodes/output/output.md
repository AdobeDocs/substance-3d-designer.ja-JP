---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/output.html"
breadcrumb-title: ''
description: ''
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Output
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 出力
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '805'
ht-degree: 0%

---


# 出力

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![原子ノード： Output](output.resources/comp_output_1.png "原子ノード： Output"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

Outputノードは、Substanceグラフの<b>result</b>を指定します。複数のOutputノードが含まれている場合は、結果の1つを指定します。

グラフの出力ノードに接続されたイメージまたは値は、このグラフを表す[インスタンス化](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)によって出力され、[グラフ出力としてエクスポート](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)できます。

</td>
</tr>
</table>

同様に、[公開されたSbsar ファイル](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)にこのグラフが含まれている場合、そのファイルは、そのファイルを使用する任意の統合またはプラグインでそのイメージを出力できます。

入力スロットはタイプに依存しません。つまり、データ型が接続された後に入力されます。

このマクロにはパラメーターはありませんが、出力に適切なラベルを付けて目的の用途に使用するために非常に重要な属性を持っています。

各Substance グラフには、*少なくとも1つの*&#x200B;出力ノードが必要です。 出力が存在しない場合、グラフは実際の結果を返すことができず、[警告](../../../../technical-issues/warnings-and-errors/warnings-and-errors.md)が発生します。

## 属性

|  |  |
| --- | --- |
| <b>識別子</b> *文字列* | 出力の一意の識別子。 このプロパティは、空白のままにすることはできません。また、特殊文字やスペースを含めることはできません。   識別子は、ノードのラベルとして使用されます。「ラベル」プロパティは空白のままです。 また、[書き出されたテクスチャ](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)に名前を付ける場合にも使用できます。 |
| <b>説明</b> *文字列* | 出力のツールチップとして使用されるオプションの説明は、Substanceグラフです。 |
| <b>ラベル</b> *文字列* | このグラフを表す[インスタンスノード](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)で、出力ノードと対応するコネクタのラベルとして使用されます。 ラベルには、スペースや特殊文字を含めることができます。 |
| <b>ユーザーデータ</b> *文字列* | 特定のフィルタリング操作に使用できるオプションのメタデータ。 [Substance 3D Painter](https://www.adobe.com/jp/products/substance3d/apps/painter.html)このデータを使用して[いくつかの機能を実行](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/content/creating-custom-effects/user-data).. |
| <b>グループ</b> *文字列* | Designerの[リンク作成モード](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)で出力をグループ化するために使用される属性です。   同一の「Group」属性を持つ出力は、「コンパクトマテリアル」リンク作成モードで1つの接続として表示されます。 |

## 統合の属性

これらは、[公開されたSbsar ファイル](../../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)のグラフを使用する統合/プラグインで使用されることを意図した属性です。

そのため、[ビットマップの書き出し](../../../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)の形式には影響しません。 さらに、Designerでは<b>Usage</b>属性のみが使用されます。詳しくは、以下を参照してください。

<b>使用方法</b>

|  |  |
| --- | --- |
| <b>コンポーネント</b> *文字列* | AxFワークフローで、一部のテクスチャチャンネルを適切なSVBRDF シェーダー入力にマッピングするために使用されます。 |
| <b>使用方法</b> *文字列* | 出力ノードのタイプと使用方法を定義します。 このプロパティは、次の点で重要です。<ul data-preserve-html="true"> <li data-preserve-html="true">一部の[リンク作成モード](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)を使用する場合のグラフ内のノードの接続 </li> <li data-preserve-html="true">3D ビュー内のシェーダへのテクスチャの接続（以下を参照： &#39;[3D ビュー内の使用のロールについて](#usages-role-3dview)&#39;）</li> <li data-preserve-html="true">統合/プラグイン内のマテリアルへのテクスチャの接続</li> </ul> |
| <b>カラースペース</b> *文字列* | 出力を解釈するカラースペースを設定します。 他のアプリケーションの一部の統合で使用され、Designerには影響しません。 |

### 3D ビュー内での使用のロールについて

グラフ出力は多くの場合、特定のテクスチャチャンネルの最終結果として使用されるため、3D ビューに使用されているシェーダーの適切なサンプラーに出力を自動送信することができます。

実際、3D ビュー内の<b>Usage</b>のプロパティ&#x200B;*がサンプラーの使用状況*&#x200B;に一致する出力は、そのサンプラーに接続されます。 例えば、`basecolor`を使用する出力は、シェーダーの`basecolor`サンプラーに接続されます。 詳細については、[データ](https://substance3d.adobe.com/documentation/display/draftdesigner/.3d%20view%20vdraftversion)ページの[3D ビューを3D ビューで表示](../../../../interface/3d-view/3d-view.md)セクションを参照してください。

[グラフビュー](../../../../interface/the-graph-view/the-graph-view.md)の空の領域でRMBをクリックし、コンテキストメニューで「<b>3Dビューで出力を表示</b>」オプションを選択して、すべての出力を&#x200B;*一致する使用状況*&#x200B;を持つ3D ビューサンプラーに接続します。

>[!IMPORTANT]
>
> たとえば、パックされたテクスチャのチャンネルに使用を割り当てるように複数の使用が設定されている場合、リスト内の&#x200B;*最初の使用*&#x200B;のみが3D ビューに接続されます。 これは既知の制限です。

## デフォルト出力

グラフに複数の出力がある場合は、そのうちの1つをグラフのデフォルト出力にすることができます。 どの出力を使用するかを指定します。

* そのグラフを表すインスタンス化のサムネール
* 2D ビュー内のインスタンス化の表示
* ライブラリにあるそのグラフのサムネイル（独自のリソースの追加については、[こちら](../../../../interface/preferences-window/project-settings/project-settings.md)を参照してください）

この機能を使用すると、グラフをグラフ出力として表示する方法とは別に、ノードを任意の順序で配置できます。

出力ノードをグラフのデフォルト出力として設定するには：

* 出力ノードを右クリックし、コンテキストメニューで「デフォルトの出力として設定」アクションを選択します。
* 出力ノードのプロパティで、「属性」セクションのヘッダーにある「デフォルトとして設定」ボタンを使用します。

次に、デフォルト出力の設定前と設定後のインスタンス化の例を示します。

<table>
  <tr style="border: 0">
    <td style="border: 0">
      <img src="output.resources/defaultouput2.png" alt="defaultupput2">
      <br><i>前</i>
    </td>
    <td style="border: 0">
      <img src="output.resources/defaultouput1.png" alt="defaultupput1">
      <br><i>後</i>
    </td>
  </tr>
</table>
