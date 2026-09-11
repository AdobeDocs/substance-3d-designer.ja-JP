---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/creating-a-substance-compositing-graph/graph-instances-sub-graphs.html"
breadcrumb-title: ''
description: グラフインスタンスとサブグラフを使用して、再利用可能なグラフコンポーネントやモジュール化されたマテリアルワークフローを作成できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Creating a Substance compositing graph > Graph instances and subgraphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラフインスタンスとサブグラフ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 7e53313d3c368803a95ebb1f9eee712ae2a05817
workflow-type: tm+mt
source-wordcount: '601'
ht-degree: 0%

---


# グラフインスタンスとサブグラフ

![](graph-instances-sub-graphs.resources/sub-graph.png)

グラフインスタンスとは、<b>別のグラフを参照</b>するノードです。 ホストグラフのインスタンス化によって参照されるグラフは、ホストグラフの<b>サブグラフ</b>と呼ばれることがあります。

インスタンスを使用すると、グラフを1つ以上のグラフで何度も再利用できるようになります。これは異なるパッケージ間でも可能です。

## なぜグラフインスタンスを使用する必要があるのですか？

<b>グラフを複数のサブグラフに分割</b>すると、*はるかに*&#x200B;効率的に<b>作業できます。</b>

Designerで複数のノードのチェーンを複製する場合は、再利用と更新を容易にするために、そのチェーンをサブグラフに分割しておくことをお勧めします。

>[!NOTE]
>
> *カスタム*&#x200B;フィルターのサブグラフーの簡単な設定を示すプロジェクトファイルは、このドキュメントの[サンプルSubstanceグラフ](../../../compositing-graphs/sample-compositing-graphs/sample-substance-compositing-graphs.md)のセクションにあります。

### グラフインスタンスの作り方を教えてください。

グラフ Aをエクスプローラーから別のグラフ Bにドラッグして、グラフ Aを参照する<b>インスタンス化</b>を作成します。

ノードを選択し、コンテキストメニューの「選択項目からグラフを作成」を使用すると、グラフを新しいノードにすばやく分割できます。 次に、新しいグラフの識別子を指定するように求められます。これは一意である必要があります。

選択したノードがグラフ内の他のノードに接続されていた場合、新しいグラフに[Input](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/input/input.md)および[Output](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)のノードも作成して、これらの接続をサブグラフに引き継ぐ必要があることに注意してください。

また、元のノードを、新しいノードを参照するインスタンス化で置き換える場合は、後で手動で行う必要があります。

最後に、プロジェクトを共有可能なSbsar ファイルに公開するときに、サブグラフをユーザーに表示するかどうかを決める必要があります。 [グラフのプロパティ](../../../compositing-graphs/graph-parameters/graph-parameters.md)で、&#39;SBSARで表示&#39;パラメーターを参照してください。

### 継承に関する言葉

サブグラフを使用するもう1つの利点は、サブグラフの各インスタンスを<b>使用中のコンテキストに適応</b>できることです。 言い換えると、同じグラフの2つのインスタンスで、異なる出力解像度、ビット深度およびタイリングモードを使用できます。

これは、グラフで作業するための<b>基本コンセプト</b>です。インスタンスをさらに使用する準備が整ったら、[Substanceグラフの継承](../../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)について詳しく学ぶことを強くお勧めします。

グラフインスタンスとサブグラフのコンセプトはSubstance機能グラフにも当てはまりますが、このページで説明する継承はSubstanceグラフにのみ当てはまります。

### 独自のノードをグラフインスタンスライブラリに追加できますか？

<b>はい、可能です</b>ただし、特定の設定が必要です。 詳細については、このドキュメントの[カスタムコンテンツとフィルターの管理](../../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)ページを参照してください。

### グラフインスタンスのソースグラフを検査できますか？

![(tick)](graph-instances-sub-graphs.resources/check.svg)はい。**Substance 3Dファイル(SBS)**&#x200B;から読み込まれたグラフのインスタンスの場合は、*のみ*&#x200B;です。 これらのインスタンスノードには&#x200B;*濃い赤*&#x200B;ラベルがあります。\
ノードを右クリックしてコンテキストメニューを開き、[**参照を開く**]オプションを選択します。

>[!NOTE]
>
> ソースグラフを検査するときに、[環境設定](../../../interface/preferences-window/preferences-window.md)の&#x200B;**グラフ**&#x200B;セクションで&#x200B;**コンテキスト内編集**&#x200B;オプションが&#x200B;*オン*&#x200B;の場合は、インスタンスのグラフの入力データを使用できます。

![(minus)](graph-instances-sub-graphs.resources/forbidden.svg) **Substance 3Dアセット(SBSAR)**&#x200B;インスタンスから読み込まれたグラフは既にコンパイルされているため、*検査できません*。 公開されたグラフのリストとそのパラメーターを確認するには、**エクスプローラー**&#x200B;パネルにアセットを読み込むだけです。 これらのインスタンスノードには&#x200B;*緑*&#x200B;ラベルがあります。\
ノードを右クリックしてコンテキストメニューを開き、[**パッケージの読み込み**]オプションを選択します。

>[!NOTE]
>
> **アトミックノード**
> 
> *Atomic*&#x200B;ノードは、Substanceエンジンのコードによって直接実装され、グラフの&#x200B;*ではなく*&#x200B;インスタンスであるため、atomicという名前が付けられています。[Substanceグラフ](../../../compositing-graphs/substance-compositing-graphs.md)の他のノードに対する&#x200B;*すべて*&#x200B;の&#x200B;*最小の構成要素*&#x200B;です。
