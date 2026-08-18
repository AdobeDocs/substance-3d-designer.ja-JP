---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: グラフインスタンスとサブグラフを使用して、再利用可能なグラフコンポーネントとモジュール化されたマテリアルワークフローを作成します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラフインスタンスとサブグラフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: b0053a42604f68604350a6bb3a2148970536c3c7
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 0%

---


# グラフインスタンスとサブグラフ

![](../../../assets/sub-graph.png)

グラフインスタンスは、<b>別のグラフを参照</b>するノードです。 ホストグラフのインスタンスノードによって参照されるグラフは、ホストグラフの<b>サブグラフ</b>と呼ばれることがあります。

インスタンスを使用すると、グラフは1つ以上のグラフで何度も再利用でき、異なるパッケージ間でも再利用できます。

## グラフインスタンスを使用する理由

<b>グラフを複数のサブグラフに分割</b>すると、*はるかに*&#x200B;より効率的に<b>作業できます。</b>

Designerで複数のノードのチェーンを複製する場合は、再利用と更新を容易にするために、そのチェーンをサブグラフに分割しておくことをお勧めします。

>[!NOTE]
>
> *カスタム*&#x200B;フィルターのサブグラフの簡単な設定を示すプロジェクトファイルは、このドキュメントの[Substanceグラフのサンプル](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)セクションにあります。

### グラフインスタンスを作成するにはどうすればよいですか？

エクスプローラーからグラフAを別のグラフBにドラッグして、グラフAを参照する<b>インスタンスノード</b>を作成します。

ノードを選択し、コンテキストメニューの「選択範囲からグラフを作成」を使用すると、ノードを新しいグラフにすばやく分割できます。 次に、新しいグラフの識別子を設定するよう求められます。この識別子は一意である必要があります。

選択したノードがグラフ内の他のノードに接続されていた場合、それらの接続をサブグラフに引き継ぐには、新しいグラフに[入力](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)および[出力](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードも作成する必要があることに注意してください。

また、元のノードを、新しいグラフを参照するインスタンスノードに置き換えるのは、後から手動で行う必要があります。

最後に、プロジェクトを共有可能なSBSARファイルに公開するときに、サブグラフをユーザーに公開するかどうかを決める必要があります。 [グラフのプロパティ](../../../compositing-graphs/graph-parameters/graph-parameters.md)で、&#39;Exposed in SBSAR&#39;パラメーターを参照してください。

### 遺伝に関する言葉

サブグラフを使用するもう1つの利点は、サブグラフの各インスタンスを<b>使用中のコンテキストに適応</b>できることです。 つまり、同じグラフの2つのインスタンスの出力解像度、ビット深度、タイリングモードが異なる場合があります。

これはグラフを操作する<b>基本概念</b>です。インスタンスをさらに使用する準備ができたら、[Substanceグラフでの継承](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)について詳しく学ぶことを強くお勧めします。

グラフインスタンスとサブグラフの概念はSubstance関数グラフにも適用されますが、このページで説明する継承はSubstanceグラフにのみ適用されます。

### 独自のグラフインスタンスをノードライブラリに追加できますか？

<b>はい、可能です</b>ただし、特定の設定が必要です。 詳細については、このドキュメントの[カスタムコンテンツとフィルターの管理](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/creating-library-filters-for-projects-170459772.html)ページを参照してください。

### グラフインスタンスのソースグラフを検査できますか？

![(tick)](../../../assets/check.svg)はい。**Substance 3Dファイル(SBS)**&#x200B;から読み込まれたグラフのインスタンスの場合は、*のみ*&#x200B;です。 これらのインスタンスノードには&#x200B;*濃い赤*&#x200B;ラベルがあります。\
ノードを右クリックしてコンテキストメニューを開き、[**参照を開く**]オプションを選択します。

>[!NOTE]
>
> ソースグラフを検査するときに、[環境設定](../../../interface/preferences-window/preferences-window.md)の&#x200B;**グラフ**&#x200B;セクションで&#x200B;**コンテキスト内編集**&#x200B;オプションが&#x200B;*オン*&#x200B;の場合は、インスタンスのグラフの入力データを使用できます。

![(minus)](../../../assets/forbidden.svg) **Substance 3Dアセット(SBSAR)**&#x200B;インスタンスから読み込まれたグラフは既にコンパイルされているため、*検査できません*。 公開されたグラフのリストとそのパラメーターを確認するには、**エクスプローラー**&#x200B;パネルにアセットを読み込むだけです。 これらのインスタンスノードには&#x200B;*緑*&#x200B;ラベルがあります。\
ノードを右クリックしてコンテキストメニューを開き、[**パッケージの読み込み**]オプションを選択します。

>[!NOTE]
>
> **アトミックノード**
> 
> *Atomic*&#x200B;ノードは、Substanceエンジンのコードによって直接実装され、グラフの&#x200B;*ではなく*&#x200B;インスタンスであるため、atomicという名前が付けられています。[Substanceグラフ](../../../compositing-graphs/substance-compositing-graphs.md)の他のノードに対する&#x200B;*すべて*&#x200B;の&#x200B;*最小の構成要素*&#x200B;です。
