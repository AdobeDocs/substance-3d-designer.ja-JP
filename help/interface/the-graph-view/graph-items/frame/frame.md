---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/the-graph-view/graph-items/frame.html"
breadcrumb-title: ''
description: Substance 3D Designer グラフビューのフレームを使用してノードを整理し、グループ化することで、見やすくすることができます。
helpx_creative_field: ""
helpx_description: Designer > Interface > Graph view > Graph items > Frame
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: フレーム
user-guide-description: ''
user-guide-title: ''
source-git-commit: 01adf91721f742481a84e22a1fa0c22e5e0de887
workflow-type: tm+mt
source-wordcount: '1645'
ht-degree: 1%

---


# フレーム

<table>
<tr style="border: 0;">
<td width="25.00%" style="border: 0;" valign="top">

![フレームアイコン](frame.resources/graphatomic-frame_1.png "フレームアイコン")

</td>
<td width="100.00%" style="border: 0;" valign="top">

フレームでは、グラフ内のオブジェクトを視覚的にグループ化し、これらすべてのオブジェクトを簡単に一緒に動かすことで、グラフの読みやすさとレイアウトが向上します。

例えば、フレームに名前や色を付けて、概観したときにグラフの構造がはっきりと見えるようにすることができます。これは、グラフが複雑になるにつれて大きな助けとなります。

また、ノードに注釈を付けて、特定の方法でノードが設定された理由を説明するドキュメンテーションツールとして機能することもできます。

</td>
</tr>
</table>

## 外観

マウスカーソルの位置または選択範囲の一部であるかどうかに応じて、フレームが様々な表示スタイルで表示され、それとどのように相互作用できるかが示されます。

+++デフォルト
既定では、フレームは<b>フレームの色</b>プロパティで選択された色で塗りつぶされた、角が丸い四角形です。 そのカラーの暗いシェードがフレームのアウトラインに適用されます。

<b>Title</b>プロパティのタイトルセットは、フレームの左上隅にグレーで表示されます。

![フレーム （既定の状態）](frame.resources/graph-frames-default.png "フレーム （既定の状態）")



+++

+++ポイント時のヘッダー
フレームの上部にマウスポインターを置くと、ヘッダーバーが表示されます。

フレームは、ヘッダーバーまたはそのタイトルをドラッグして移動できます。

![フレーム （ホバーステート）](frame.resources/graph-frames-hover.png "フレーム （ホバーステート）")



+++

+++選択済み
選択すると、フレームのタイトルとアウトラインが白でハイライトされます。 輪郭が太くなります。

![フレーム （選択されたステート）](frame.resources/graph-frames-selected.png "フレーム （選択されたステート）")



+++

## フレームの作成

フレームは、次のいずれかの方法で、任意のグラフの種類に追加できます。

+++ノードメニュー
グラフビューの<b>スペースバー</b>を押して<b>ノードメニュー</b>を開き、一覧の[フレーム]をクリックします。

検索フィールドに「フレーム」と入力して、アイテムのサーフェスを表示し、すばやく検索することができます。

+++

+++ショートカット
[環境設定](../../../../interface/preferences-window/preferences-window.md)の「フレーム」項目にキーボードショートカットがマッピングされている場合は、グラフビューにフォーカスがあるときにそのショートカットを押します。

+++

+++コンテキストメニュー
グラフビューで、任意のオブジェクトまたは空の領域で<b>RMB</b>を押し、「<b>フレームを追加</b>」オプションを選択します。

+++

+++グラフツールバー
グラフビューツールバーで、<b>ノードパレット</b>の[フレーム]ボタンをクリックします。

+++

+++ライブラリ
ライブラリで、<b>グラフアイテム</b>カテゴリを選択し、「フレーム」アイテムをグラフビューにドラッグアンドドロップします。

+++

### フレームの選択範囲

フレームの作成時にグラフで選択範囲がアクティブになっていると、そのフレームは自動的に調整され、選択したオブジェクトが完全に含まれます。

そのため、キーボードショートカットを使用してフレームを作成すると、グラフのコンテンツのフレーム化がさらに高速になります。

![フレーム：作成メソッド](frame.resources/graph-frames_creation.gif "フレーム：作成メソッド"){width="480px"}

>[!TIP]
>
> フレームを作成すると、その「タイトル」プロパティに自動的にフォーカスが移動するので、すぐにフレームのタイトルを編集できます。

## フレームの操作

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

フレームは、タイトルまたはヘッダーバーをドラッグすると<b>パン</b>され、境界線またはコーナーをドラッグすると<b>サイズ変更</b>されます。

この図では、パン（青）とサイズ変更（黄）の相互作用ゾーンが強調表示されています。

</td>
<td style="border: 0;" valign="top">

![フレーム：対話ゾーン](frame.resources/graph-frames_interaction-zones.png "フレーム：対話ゾーン")

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### グリッドのスナップ

初期設定では、フレームを移動またはサイズ変更すると、中くらいのグリッドにスナップします。

<b>Ctrl</b> (Windows) / <b>Cmd</b> (macOS)キーを押したままにすると、このスナップが小さなグリッドに移動し、微調整が行われます。

</td>
<td style="border: 0;" valign="top">

![フレーム：グリッドのスナップ](frame.resources/graph-frames_grid-snapping.gif "フレーム：グリッドのスナップ")

</td>
</tr>
</table>

## プロパティ

フレームを選択すると、[プロパティ](../../../../interface/properties/properties.md)ドックで次のプロパティを使用できます。

+++タイトル
フレーム左上に配置されている<b>タイトル</b>。 <b>タイトルの表示</b>プロパティを使用して、タイトルの表示のオンとオフを切り替えることができます。

タイトルのサイズを最小限の画面サイズでロックして、グラフをズームアウトしてもタイトルが読みやすいようにすることができます。 これを行うには、[グラフビュー](../../../../interface/the-graph-view/the-graph-view.md)ツールバーの<b>情報</b>ドロップダウンで「フレームタイトル」オプションをオンにします。

![フレーム：タイトル](frame.resources/graph_frames_title.gif "フレーム：タイトル"){width="640px"}



+++

+++説明
<b>説明</b>は、フレームの内容に注釈を付けるために使用できるオプションの追加テキストです。

HTMLタグを使用してテキストをフォーマットできます。 ![](frame.resources/graph-frames_html-markup-button.png) <b>HTMLマークアップ</b>ボタンをクリックすると、この書式が切り替わります。

詳しくは、以下の説明セクションを参照してください。

![フレーム：説明](frame.resources/graph-frames_description.gif "フレーム：説明"){width="640px"}



+++

+++カラー
<b>フレームの色</b>は、グラフビューのフレームを塗りつぶすために使用されます。 カラーピッカーを使用して、任意のカラーを選択します。

色のアルファチャンネルはフレームの&#x200B;*不透明度*&#x200B;を制御します。値0はフレームが完全に透明であることを示します。

![フレーム:カラー](frame.resources/graph-frames_colour.gif "フレーム:カラー"){width="640px"}



+++

## 説明

フレームには、フレーム内に配置されるテキストで注釈を付けることができます。 テキストが左揃えで配置され、フレームの左上隅から開始します。 フレームの[Description](#properties)プロパティを使用してテキストを編集します。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 標準

<b>タイトル</b>は、フレームの左上に太字で表示されます。 タイトルの表示/非表示を切り替えることができます。

画面サイズを最小限に抑えることで、グラフをズームアウトしても読みやすいサイズに保つことができます。 これを行うには、[グラフビュー](../../../../interface/the-graph-view/the-graph-view.md)ツールバーの<b>情報</b>ドロップダウンで「フレームタイトル」オプションをオンにします。

</td>
<td style="border: 0;" valign="top">

![フレーム （既定の説明）](frame.resources/graph-frames-descr.png "フレーム （既定の説明）"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### HTMLの書式設定

フレームの<b>Description</b>プロパティのHTMLタグを使用して、テキストを書式設定できます。 同じプロパティの![](frame.resources/graph-frames_html-markup-button.png) <b>HTMLマークアップ</b>ボタンを使用して、書式設定を有効にする必要があります。

</td>
<td style="border: 0;" valign="top">

![フレーム （HTML形式の説明）](frame.resources/graph-frames-descr-html.png "フレーム （HTML形式の説明）"){zoomable="yes"}

</td>
</tr>
</table>

このサンプルをフレームの「説明」プロパティにコピー&amp;ペーストして、この機能を自分でテストできます。

```
<h2>HTML formatting</h2>

<p>This is a description formatted using <b>HTML markup</b>.</p>

<p>Formattig text makes it more <i>pleasant</i>, <font color="#CC8822">impactful</font> and <code>clearly structured</code> for users.</p>

<p><img src="image_filepath">  Images are also supported! <sup>How nice!</sup></p>
```


テキストの書式設定に役立つタグのリストを次に示します。

+++HTML書式タグ

|  |  |
| --- | --- |
| 太字 | &lt;b>...&lt;/b> |
| 斜体 | &lt;i>...&lt;/i> |
| カラー | &lt;font color=&quot;#4A567C&quot;>...&lt;/font> |
| 段落 | &lt;p>...&lt;/p> |
| 改行 | &lt;br> |
| 見出し | &lt;h1>...&lt;/h1>、&lt;h2>...&lt;/h2>など |
| 画像 | &lt;img src=&quot;{path\_to\_image}&quot;> |
| 上付文字 | &lt;sub>...&lt;/sub> |
| 番号なしリスト（箇条書き） | &lt;ul> &lt;li>...&lt;/li> &lt;li>...&lt;/li> &lt;/ul> |
| 番号付きリスト（番号） | &lt;ol> &lt;li>...&lt;/li> &lt;li>...&lt;/li> &lt;/ol> |
| コード | &lt;code>...&lt;/code> |


+++

## 包含ルール

オブジェクトが包含ルールを満たす場合、そのオブジェクトはフレームに含まれると見なされます。 これらの規則は、オブジェクトや特殊ケースによって異なります。 次に一覧を示します。

各イラストレーションの黄色の記号は、オブジェクトをフレームに含めるために、フレームの境界内に完全に収まる必要があるポイントまたは領域を表します。

+++ノード
<b>中心点</b>が使用されています。

ノードの下に表示されるバッジ、コネクタ、情報はすべて無視されます。

ノードのHeightは、入力コネクタまたは出力コネクタの数によって異なる場合があります。

コネクタの表示と非表示、追加、または削除を切り替えると、ノードのHeightが&#x200B;*中心*&#x200B;から調整されます。

したがって、ノードの中心点の位置は、*意図的に移動*&#x200B;するまで変更しないでください。

![フレームの包含：背の高いノード](frame.resources/frame_inclusion_node_tall.png "フレームの包含：背の高いノード")



*host*&#x200B;ノードの<b>c</b><b>enter point</b>が使用されています。

ホストノードは、ノードがドッキングされているノードです。

複数のノードが1つのチェーンにドッキングされている場合、最後にドッキングされたノードのホストノードがチェーン全体に使用されます。

ノードの下に表示されるバッジ、コネクター、情報はすべて無視されます。

![フレームの含み：ドッキングされているノード](frame.resources/frame_inclusion_node_docked.png "フレームの含み：ドッキングされているノード")



![フレームの含み： nodes](frame.resources/frame_inclusion_node.png "フレームの含み： nodes")



+++

+++ドットノード
ドットの<b>中心点</b>が使用されます。

コネクター、ポータルアイコン、名前はすべて無視されます。

![フレームの含み：ドットノード](frame.resources/frame_inclusion_dot.png "フレームの含み：ドットノード")



+++

+++コメント
コメントの&#x200B;*バウンディングボックス* （黄色のアウトライン）の<b>中心点</b>が使用されます。

親になったコメントは、コメントの含めるルールに従いません。

代わりに、*親*&#x200B;ノードの<b>中心点</b>が使用されます。

ノードの下に表示されるバッジ、コネクター、情報はすべて無視されます。



![フレームの取り込み：親になったコメント](frame.resources/frame_inclusion_comment_parented.png "フレームの取り込み：親になったコメント")



![フレームの追加：コメント](frame.resources/frame_inclusion_comment.png "フレームの追加：コメント")



+++

+++ピン
ピンアイコンの<b>ヒント</b>が使用されています。

![フレームの組み込み：ナビゲーションピン](frame.resources/frame_inclusion_pin.png "フレームの組み込み：ナビゲーションピン")



+++

+++フレーム
入れ子になったフレームの<b>境界ボックス</b>が使用されています。

つまり、入れ子になったフレームを別のフレームの境界内に完全に含める必要があります。

タイトルは無視されます。

![フレームの含み：ネストされたフレーム](frame.resources/frame_inclusion_frame.png "フレームの含み：ネストされたフレーム")



+++

## サイズをコンテンツに合わせる

![フレーム:サイズをコンテンツに合わせる](frame.resources/graph-frames_fit-size-to-content.png "フレーム:サイズをコンテンツに合わせる")

グラフに調整を加えると、フレームがそのコンテンツに合わせて適切に調整されなくなる場合があります。 この場合、1つの中グリッドセルのパディングで、フレームの位置とサイズをコンテンツのスパンに合わせて自動調整することができます。

これを行うには、フレームのタイトルまたはヘッダーバーの<b>人民元</b> （[表示方法](#appearance)を参照）をクリックし、コンテキストメニューの<b>コンテンツにサイズを合わせる</b>をクリックします。

>[!NOTE]
>
> このオプションは、*1つ*&#x200B;以上のグラフオブジェクトがフレームの[包含ルール](../../../../interface/the-graph-view/graph-items/frame/frame.md)を満たしている場合に使用できます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 説明テキストを調整する

フレームに説明がある場合は、可能であれば、説明の横の空白を使用するように調整されます。

含めるオブジェクトがそのスペースに収まらない場合、フレームのHeightは説明が収まるように調整されます。

</td>
<td style="border: 0;" valign="top">

![フレーム:コンテンツに合わせてサイズを調整（説明あり）](frame.resources/graph-frames_fit-description.png "フレーム:コンテンツに合わせてサイズを調整（説明あり）")

</td>
</tr>
</table>

+++例
![フレーム:サイズをコンテンツに合わせる(GIF)](frame.resources/graph-frames_fit-size-to-content.gif "フレーム:サイズをコンテンツに合わせる(GIF)"){width="640px"}



+++

## 自動拡張

![フレーム：自動拡張](frame.resources/graph-frames_auto-expand.png "フレーム：自動拡張")

グラフが大きくなると、フレームのコンテンツの配置を変更する必要が生じることがあります。 ノードを移動して追加するスペースを確保したり、コンテンツを読みやすくするためにより多くの間隔を空ける必要がある場合があります。

これらの調整を容易にするために、[選択したオブジェクト](#inclusion-rules)を動かす際に、フレームを自動で広げることが可能です。<b>Shift</b>を押しながらオブジェクトを動かすと、フレームの境界線がオブジェクトの境界内に収まるように自動で調整されます。

これは、複数のオブジェクトを含む選択範囲にも適用されます。 その場合、各オブジェクトのホストフレームは同時に調整されます。

オブジェクトがフレームの境界で完全に囲まれていなくても、オブジェクトの[包含の規則](#inclusion-rules)を満たす場合、フレームは、<b>Shift</b>キーが押されるとすぐに、そのオブジェクトを中グリッドのセルのパディングで完全に囲むように調整されます。

>[!NOTE]
>
> フレームの自動調整をトリガーまたはキャンセルするには、移動中に任意の時点で<b>Shift</b>キーを押したり離したりできますが、調整を効果的に適用するには、移動の完了時に&#x200B;*Shift*&#x200B;を押す必要があります。

+++例
![フレーム：自動拡張(GIF)](frame.resources/graph-frames_auto-expand.gif "フレーム：自動拡張(GIF)"){width="640px"}



+++
