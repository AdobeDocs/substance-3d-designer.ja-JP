---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters.html"
breadcrumb-title: ''
description: ワークフローの構成を改善するために、Substance合成グラフでパラメーターを管理および整理する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Manage parameters
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パラメーターを管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 3%

---


# パラメーターを管理

Designerでは、パラメーターを直接調整する以外の方法で制御する必要がある場合に、次のような便利なアクションを提供します。

* ノードのすべてのパラメーターの値を[コピーして貼り付け](#copy-paste-parameters)
* 後で再利用できるように、ノードの値またはすべてのパラメーターを[プリセットファイル](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)に保存します
* [ノードのパラメーター](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)を公開してアクセス可能にし、リンク付けします
* [他のパラメーターの値に従ってパラメーターを表示または非表示にする](../../compositing-graphs/visible-control-vis/visible-if-control-visibility-of-inputs-outputs-and-parameters.md)
* [Substance関数グラフ](../../function-graphs/function-graphs.md)を使用して、パラメーターの値を計算します

## パラメーターのアクション

パラメータの管理に使用できるツールは、次の場所にあります。

### グローバルアクション

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

ノードのプロパティがプロパティドックに表示されている場合、次のセクションヘッダーの&#39;<b>パラメーターの管理</b>&#39;メニューを使用して、ノードパラメーターをグローバルに管理できます。

* [atomicノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)の場合：特定のパラメーター
* [インスタンスノード](../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)の場合：インスタンスパラメーター

</td>
<td width="33.33%" style="border: 0;" valign="top">

![プロパティのグローバル&#39;パラメーターの管理&#39;メニュー](../../assets/manage-parameters-menu-global.png "プロパティのグローバル&#39;パラメーターの管理&#39;メニュー"){zoomable="yes"}

</td>
</tr>
</table>

このメニューのアクションは、そのセクションに一覧表示されているパラメーター&#x200B;*すべて*&#x200B;に影響します：

* <b>パラメーターの公開：</b> &#39;パラメーターの一括公開&#39;ダイアログを開きます。 公開されている各パラメーターに対して、アクションは新しいグラフ入力を作成し、そのグラフ入力を使用して関数を自動的に設定します。 [この専用ページ](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)のパラメーターの公開について詳しく説明します。
* <b>パラメーターのコピー：</b>以下の[パラメーターのコピーと貼り付け](#copy-paste-parameters)のセクションを参照してください。
* <b>パラメーターの貼り付け：</b>以下の[パラメーターのコピーと貼り付け](../../compositing-graphs/manage-parameters/manage-parameters.md)のセクションを参照してください。
* <b>パラメーターをプリセットファイルとして保存する：</b> [この専用ページ](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)のパラメータープリセットの詳細をご覧ください。
* <b>プリセットファイルからパラメーターを適用する：</b> [この専用ページ](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)のパラメータープリセットの詳細をご覧ください。
* <b>すべてリセット：</b>すべてのパラメーターを既定値と範囲にリセットします。 関数がパラメーターに適用されると、その関数は破棄されます。

>[!NOTE]
>
> 一部のアトミックノードでは使用できないアクションがあります。 以下の[Atomic nodesの制限](#atomic-nodes-limitations)を参照してください。

### 単一パラメーターのアクション

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

*単一*&#x200B;パラメーターを管理する場合は、パラメーターラベルの反対側にある&#39;<b>関数の管理</b>&#39;メニューを使用してください。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![プロパティのローカルの[パラメーターの管理]メニュー](../../assets/manage-parameters-menu.png "プロパティのローカルの[パラメーターの管理]メニュー"){zoomable="yes"}

</td>
</tr>
</table>

[Substance関数グラフ](../../function-graphs/the-function-graph/the-function-graph.md)は、次の3つの方法でそのパラメーターに適用できます。

* <b>新しいグラフ入力として公開：</b>新しいグラフ入力を作成し、そのグラフ入力を使用して関数を自動的に設定します。 [この専用ページ](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)のパラメーターの公開について詳しく説明します。
* <b>空の関数：</b>最初から関数を作成します。
* <b>定数値：</b>パラメーターの現在の値に設定された[定数値ノード](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)から始まる関数を編集します。
* <b>リセット：</b>パラメーターを既定値と範囲にリセットします。 パラメーターに関数が適用された場合、その関数は破棄されます。

>[!NOTE]
>
> コピー/ペーストおよびプリセットファイルアクションは、すべてのパラメーターに対してグローバルであるため、単一のパラメーターには使用できません。

### ノードコンテキストメニュー

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

上記の&#x200B;*グローバル*&#x200B;メニューの一部のパラメーターアクションは、ノードのコンテキストメニューで使用できます。 ノードの[RMB]をクリックし、[パラメータの管理]に移動してアクセスします。

このメニューでは、コピー/ペースト操作を実行できないことに注意してください。 前述のように、ノードのプロパティに表示されます。

このメニューには、以下に示すアトミックノードに関する制限と同じ制限が適用されます。

</td>
<td width="50.00%" style="border: 0;" valign="top">

![&#39;ノードコンテキストメニューの[パラメーターの管理]メニュー](../../assets/manage-parameters-node-menu.png "&#39;ノードコンテキストメニューの[パラメーターの管理]メニュー"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## パラメーターのコピー&amp;ペースト

ソースノードのすべてのパラメータ値をコピーし、ターゲットノードに貼り付けることができます。 ソースノードとターゲットノードのパラメーターは、それらの識別子と種類の両方に基づいて<b>一致します</b>。

たとえば、識別子が&#39;scale&#39;で型が&#39;Float&#39;のパラメータ&#39;Scale&#39;を、識別子も&#39;scale&#39;で型が&#39;Float&#39;の別のパラメータ&#39;Shape Scale&#39;にコピーして貼り付けることができます。

この機能は、[パラメータープリセットファイル](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)を使用する場合と同様に動作します。 実際、クリップボードにコピーされたデータは、SBSPRSプリセットファイルに保存されたデータと同じであり、任意のテキストエディターにペーストしてレビューおよび編集することができます。

</td>
<td style="border: 0;" valign="top">

![パラメーターのコピーと貼り付け](../../assets/copy-paste-parameters.gif "パラメーターのコピーと貼り付け"){zoomable="yes"}

</td>
</tr>
</table>

## Atomicノードの制限

特定の実装と制御のため、一部の[原子ノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)では使用できない機能があります。

これらのアクション…

* [パラメータをコピー/貼り付け](#copy-paste-parameters)
* [プリセットファイルの保存と適用](../../compositing-graphs/manage-parameters/parameter-presets/parameter-presets.md)

...これらのアトミックノードには使用できません。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)

[カーブ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/curve/curve.md)

[距離](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/distance/distance.md)

[FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md)

[グラデーション (ダイナミック)](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-dynamic/gradient-dynamic.md)

</td>
<td style="border: 0;" valign="top">

[グラデーションマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/gradient-map/gradient-map.md)

[入力カラー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[入力グレースケール](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[入力値](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)

[出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)

</td>
<td style="border: 0;" valign="top">

[ピクセルプロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)

[SVG](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/svg/svg.md)

[テキスト](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/text/text.md)

[均一カラー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md)

[バリュープロセッサー](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)

</td>
<td style="border: 0;" valign="top">



</td>
</tr>
</table>
