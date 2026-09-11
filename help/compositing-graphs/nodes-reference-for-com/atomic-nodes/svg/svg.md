---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/svg.html"
breadcrumb-title: ''
description: SVGノードを使用して、スケーラブルなグラフィックエレメントを作成するためのテクスチャとしてSVGベクターグラフィックを読み込んでレンダリングします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > SVG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: SVG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 8b6f65bd88f3c83bf6682c7bca91615166389a91
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 1%

---


# SVG

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![アトミックノード: SVG](svg.resources/comp_svg_1.png "アトミックノード: SVG"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

[SVG画像](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)をビットマップとしてレンダリングします。 つまり、ベクトルシェイプをピクセルにマッピングします。

このノードを作成するには、いくつかの方法があります。これらすべての方法では、[リソースのリンクとインポートの違い](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)を理解する必要があります。

</td>
</tr>
</table>

ノードを最初から作成するか、SVGファイルをグラフビューにドロップします。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">



</td>
<td width="83.33%" style="border: 0;" valign="top">



</td>
<td width="100.00%" style="border: 0;" valign="top">



</td>
</tr>
</table>

>[!TIP]
>
> 生成またはインポートされたSVG画像は、[2D ビュー](../../../../interface/2d-view/2d-view.md) Dockの[ベクター編集ツール](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)を使用して編集できます。

>[!IMPORTANT]
>
> このノードは外部リソースに依存しているため、これらのノードを使用する際には、いくつかの点に留意する必要があります。
> 
> * SVGノードはカラーまたはグレースケールを返すことができますが、リソースがグレースケールベクトルの場合でもデフォルトでカラーが使用されます。 この設定は、グラフの性能や複雑さに影響する可能性があるため、必要に応じて常に「グレースケール」の[カラーモード](#parameters)に切り替えてください。
> * SVGノードを削除しても、[パッケージ](../../../../glossary/glossary.md)の[SVGリソース](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)は削除されません。[エクスプローラー](../../../../interface/the-explorer-window/the-explorer-window.md)で手動で削除する必要があります。
> * SVGシェイプは、Substanceグラフでビットマップとして使用するために、[テッセレーション](../../../../glossary/glossary.md)されてジオメトリ/ポリゴンに変換され、次に&#x200B;*ラスタライズ*&#x200B;されます。 これらの操作に使用されるテクノロジーは、アウトラインなどの複数のベクトルプロパティをサポートしていません。 これらの制限の詳細については、[こちら](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)をご覧ください。

>[!WARNING]
>
> SVGシェイプは、Substanceグラフでビットマップとして使用するために、[テッセレーション](../../../../glossary/glossary.md)されてジオメトリ/ポリゴンに変換され、次に&#x200B;*ラスタライズ*&#x200B;されます。
> 
> これらの操作に使用されるテクノロジーは、アウトラインなどの複数のベクトルプロパティをサポートしていません。
> 
> これらの制限の詳細については、[こちら](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)をご覧ください。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 例

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブーリアン* | カラーまたはグレースケールで返すノードの出力タイプを指定します。 |
| <b>背景色</b> *カラー/グレースケール* | ベクターシェイプで覆われていない領域で使用する出力画像の背景色を設定します。   *入力が接続されている場合は、&#39;[Background](#inputs)&#39;入力によって上書きされます。* |
| <b>PKGリソースパス</b> *文字列* | ノードによって参照されている[SVGリソース](../../../../resources/vector-graphics-svg-res/vector-graphics-svg-resource.md)へのパスです。   手動で入力するのではなく、エクスプローラーからリソースをコピーしてパラメーターのテキストフィールドに貼り付けるか、[エクスプローラー](../../../../interface/the-explorer-window/the-explorer-window.md)からビットマップリソースを直接グラフのSVGノードにドラッグアンドドロップすることをお勧めします。 |

## ベクター編集ツール

ベクターシェイプはDesignerで編集できます。 編集ツールの詳細については、[このセクション](../../../../resources/vector-graphics-svg-res/vector-editing-tools/vector-editing-tools.md)を参照してください。

## 入力コネクタ

|  |  |
| --- | --- |
| <b>背景</b> *グレースケール/カラー*&#x200B;プライマリ | ベクターシェイプで覆われていない領域で使用する出力画像の背景色を設定します。   *接続時に&#39;[背景色](#parameters)&#39;パラメーターを上書きします。* |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
