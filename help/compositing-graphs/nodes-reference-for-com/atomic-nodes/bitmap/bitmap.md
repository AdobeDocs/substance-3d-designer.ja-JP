---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/bitmap.html"
breadcrumb-title: ''
description: ビットマップノードを使用すると、ビットマップイメージを読み込んで、Substance合成グラフのテクスチャとして使用することができます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Bitmap
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ビットマップ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 1%

---


# ビットマップ

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![Atomicノード：ビットマップ](../../../../assets/comp_bitmap.png "Atomicノード：ビットマップ"){width="200px"}

</td>
<td width="100.00%" style="border: 0;" valign="top">

[ビットマップリソース](../../../../resources/bitmap-resource/bitmap-resource.md)をグラフに読み込みます。

このノードは、[ビットマップ](../../../../glossary/glossary.md)をグラフに読み込むためか、[ビットマップペイントツール](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)で使用する新しいビットマップを作成するために使用されます。

このノードを作成するには、いくつかの方法があります。これらすべての方法を実行するには、[リソースのリンクとインポートの違いを理解する必要があります。](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)

</td>
</tr>
</table>

ノードを最初から作成するか、サポートされている形式の[ビットマップ](../../../../glossary/glossary.md)を[グラフ]ビューにドロップします。

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
> 生成または読み込まれた8ビットビットマップは、[2Dビュー](../../../../interface/2d-view/2d-view.md) Dockの[ビットマップペイントツール](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)を使用してペイントできます。

>[!IMPORTANT]
>
> このノードは外部リソースに依存しているため、これらのノードを使用する場合は、いくつかの点に留意する必要があります。
> 
> * ビットマップノードはカラーまたはグレースケールを返すことができますが、リソースがグレースケールビットマップの場合でもデフォルトはカラーです。 この設定は、グラフのパフォーマンスや複雑さに影響を与える可能性があるため、必要に応じて常に「グレースケール」の[カラーモード](#parameters)に切り替えてください。
> * ビットマップノードを削除しても、[パッケージ](../../../../glossary/glossary.md)の[ビットマップリソース](../../../../resources/bitmap-resource/bitmap-resource.md)は削除されません。[エクスプローラー](../../../../interface/the-explorer-window/the-explorer-window.md)で手動で削除する必要があります。
> * 一方、エクスプローラーで[ビットマップリソース](../../../../resources/bitmap-resource/bitmap-resource.md)を削除する場合は注意してください。キャッシュに保持されるため、そのセッションのグラフでは引き続き機能しますが、次に[パッケージ](../../../../glossary/glossary.md)を読み込んだときに、欠落しているリソースとしてマークされます。
> * Substanceグラフが[cooked](../../../../glossary/glossary.md)の場合、ビットマップの解像度は、元のサイズではなく、グラフ内の解像度で固定されます。 ビットマップノードの&#39;出力サイズ&#39; [基本パラメーター](../../../../glossary/glossary.md)で&#39;絶対&#39; [継承メソッド](../../../../glossary/glossary.md)が使用され、そのノードの後に、&#39;親を基準にする&#39;に設定された[変換2D](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)ノード（ホストグラフの解像度）が続いていることを確認することをお勧めします。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## パラメーター

</td>
<td style="border: 0;" valign="top">

### ビットマップペイントツール

</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### 例

</td>
</tr>
</table>

## パラメーター

|  |  |
| --- | --- |
| <b>カラーモード</b> *ブール値* | カラーまたはグレースケールで返すノードの出力タイプを指定します。 |
| <b>PKGリソースパス</b> *文字列* | ノードによって参照されている[ビットマップリソース](../../../../resources/bitmap-resource/bitmap-resource.md)へのパスです。   手動で入力するのではなく、エクスプローラーからリソースをコピーしてパラメーターのテキストフィールドに貼り付けるか、[エクスプローラー](../../../../interface/the-explorer-window/the-explorer-window.md)からビットマップリソースを直接グラフのビットマップノードにドラッグアンドドロップすることをお勧めします。 |
| <b>メソッドのサイズ変更</b> *整数* | ビットマップを拡大または縮小するときに使用する再サンプル方法です。<ul data-preserve-html="true"> <li data-preserve-html="true"><i>滑らかな引き伸ばし：</i>引き伸ばされた画像の元のピクセルを補間するには、[バイリニアフィルター](../../../../glossary/glossary.md)を適用します。</li> <li data-preserve-html="true"><i>最も近い伸縮：</i>画像を伸縮し、最も近いソースピクセルの色をそのまま使用します。</li> </ul> |

## ビットマップペイントツール

ビットマップはDesignerで編集できます。 編集ツールの詳細については、[このセクション](../../../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)を参照してください。

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *グレースケール/カラー* |  |

## 例

*近日公開。*
