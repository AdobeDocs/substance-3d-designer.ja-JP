---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/atomic-nodes/input.html"
breadcrumb-title: ''
description: 入力ノードを使用して、ユーザーが公開および調整できるSubstanceグラフの入力パラメーターを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Atomic nodes > Input
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 入力
user-guide-description: ''
user-guide-title: ''
source-git-commit: ea96f5a148246d20263c4ecf0b67d0b4a51f28a8
workflow-type: tm+mt
source-wordcount: '816'
ht-degree: 0%

---


# 入力

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![原子ノード：入力色](../../../../assets/comp_inputcolor_1.png "原子ノード：入力色"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![アトミックノード：入力グレースケール](../../../../assets/comp_inputgrayscale_1.png "アトミックノード：入力グレースケール"){width="200px"}

</td>
<td style="border: 0;" valign="top">

![アトミックノード：入力値](../../../../assets/comp_inputnumeric_1.png "アトミックノード：入力値"){width="200px"}

</td>
</tr>
</table>

入力ノードは、グラフにダイナミックスロットを作成する特殊なタイプのノードで、グラフを別のコンテキストで使用すると、任意の入力を接続できます。

[出力ノード](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)とは異なり、カラー、グレースケール、または値の入力を明示的に配置する必要があります。 接続されている内容によってタイプが変わる独自の「不可知入力」を作成することはできません。

入力ノードは[出力ノード](../../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ほど重要ではありません。入力を必要としない、完全に機能する高度なグラフを作成できます。 入力は、Substance 3D Painterの[インスタンス](../../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)または[フィルター](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/effects/filter)を作成する場合など、グラフまたはノードインスタンスの結果を外部入力に基づいて作成する場合にのみ使用されます。

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

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## パラメーター

</td>
<td style="border: 0;" valign="top">

### 属性

</td>
<td style="border: 0;" valign="top">

### 遺伝

</td>
<td style="border: 0;" valign="top">

### 統合属性

</td>
</tr>
</table>

## パラメーター

デフォルトでは、何も接続されていない場合、入力カラーまたはグレースケールは黒を返します。 別の既定値を設定するか、既存の[ビットマップリソース](../../../../resources/importing-linking-and-new/importing-linking-and-new-resources.md)を[エクスプローラー](../../../../interface/the-explorer-window/the-explorer-window.md)からグラフの入力ノードにドラッグして、スロットでこのデータをプレビューできます。 この機能は、カラーとグレースケールの入力に対してのみ使用できます。 デフォルト値は、他のコンテキストで使用される場合は永続的で、プレビュービットマップは他の場所に破棄されます。

他のグラフの出力と一緒に表示したい場合は、上記の方法のためにグラフをビットマップに書き出すか、「コンテキスト内編集」を使用する必要があります。

|  |  |
| --- | --- |
| <b>PKGリソースパス</b> *文字列* | プレビュー用のカスタムビットマップリソースを示します。 |
| <b>既定値</b> *カラー/グレースケール/値* | このスロットに何も接続されていない場合、デフォルト入力として黒以外の別の値を使用できます。 |

## 属性

|  |  |
| --- | --- |
| <b>識別子</b> *文字列* | 唯一の必須で一意の属性です。 スペースは使用できません。   これは、ラベルが設定されていない場合に入力にラベルを付けたり、異なる出力を区別するために使用されます。 単に「input\_1」に残さないでください！ |
| <b>説明</b> *文字列* | DesignerのライブラリとPainterのシェルフで使用されるオプションの説明。 |
| <b>ラベル</b> *文字列* | DesignerおよびPainter UIのラベル付けに使用されるUIラベル。 スペースを含めることができます。   アンダースコアの代わりにスペースバーのみを使用して、識別子と同様の名前で設定することをお勧めします。 |
| <b>ユーザーデータ</b> *文字列* | 追加のオプションのユーザーデータ。特定のフィルター操作に使用できます。基本的には、ワイルドカードのカスタムデータフィールドです。 |
| <b>グループ</b> *文字列* | Designerの[リンク作成モード](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)の入力をグループ化するために使用されるグループ属性です。   同一の（大文字と小文字を区別する）グループ属性を持つ入力は、コンパクトマテリアルモードでは単一の接続として表示されます。 |

## 遺伝

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

複数の入力が存在する場合、グラフがこれらの入力から[基本パラメーターを継承](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)する方法に注意する必要があります。\
基本パラメーターには、特に<b>出力サイズ</b>、<b>出力形式</b>および<b>タイリングモード</b>が含まれます。

</td>
<td width="33.33%" style="border: 0;" valign="top">

[![Substanceグラフの主な入力](../../../../assets/node-primary-input.png)](https://helpx.adobe.com/Primary%20input%20in%20Substance%20graph)

</td>
</tr>
</table>

入力は、[プライマリ入力](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)として定義できます。 この入力は、継承メソッドが&#x200B;*親に対する相対*&#x200B;に設定されているすべての入力の属性を駆動します。 これは、入力ノードで既定で設定されている継承メソッド&#x200B;*です。*

入力ノードをグラフのプライマリ入力として設定するには、ノードの&#x200B;*RMB*&#x200B;をクリックし、コンテキストメニューの<b>プライマリ入力として設定</b>オプションを選択します。\
ノードのプライマリ入力は、コネクタの&#x200B;*小さな暗い点*&#x200B;でマークされます（このセクションの横の例では赤い丸で囲まれています）。

または、*入力に対して相対的*&#x200B;継承メソッドに設定された入力は、プライマリ入力の&#x200B;*に関係なく*&#x200B;接続先のノードから属性を継承します。

最後に、継承メソッドを&#x200B;*絶対*&#x200B;に設定することで、指定された属性の値を上書きできます。

>[!TIP]
>
> 継承の詳細については、このドキュメントの[Substanceグラフでの継承](../../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)ページに移動してください。

>[!IMPORTANT]
>
> [Substance 3Dアセット(SBSAR)](https://helpx.adobe.com/jp/substance-3d-assets.html)では、入力ノードの&#x200B;*入力に対する相対*&#x200B;継承方法が&#x200B;*サポートされていません*。 パッケージを公開する前に、すべての入力ノードの継承メソッドを&#x200B;*親に対する相対*&#x200B;に設定してください。

## 統合の属性

入力は3Dビューに直接送信されませんが、その使用量属性は、特定のマップをスロットに自動入力するために[Substance 3D Painter](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/home)によって使用されます（主に[フィルター](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/effects/filter)で使用されます）。

さらに、使用量属性は、正しい入力スロットと出力スロットに一致させるために、[リンク作成モード](../../../../interface/the-graph-view/link-creation-modes/link-creation-modes.md)でも使用されます。

<b>使用方法</b>

|  |  |
| --- | --- |
| <b>コンポーネント</b> *文字列* | これにより、結果の入力に実際にどのチャンネルが含まれるかが決まります。   これはレガシー設定で、統合やグラフでは使用されなくなりました。 |
| <b>使用方法</b> *文字列* | この入力のタイプまたは使用方法を定義します。 他のノードがこの入力に接続する方法を示します。 |
| <b>カラースペース</b> *文字列* | この入力を解釈するカラースペースを設定します。 |
