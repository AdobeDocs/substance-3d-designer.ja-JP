---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/manage-parameters/parameter-presets.html"
breadcrumb-title: ''
description: Substance 3D Designerでパラメータープリセットを作成し、使用して、パラメーター設定を保存および適用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exposing a parameter > Parameter presets
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パラメータープリセット
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---


# パラメータープリセット

パラメータープリセットを使用すると、一連のパラメーターに対して事前に設定された値を大量に保存および転送できます。これらは多くのシナリオで役立ち、可能性の広いパラメーターが大量に存在する場合に最も役立ちます。

プリセットの保存と読み込みには2つの方法があります。いずれも、以下に詳述するように、異なるユースケースがあります。

![プリセットの読み込み/保存ドロップダウンメニュー](parameter-presets.resources/parameter-presets-01.gif "プリセットの読み込み/保存ドロップダウンメニュー"){width="512px"}

## 外部プリセット

外部プリセットには、ディスク上の外部ファイルである\*.SBSPRSファイルが含まれます。 これらは異なるグラフやノード間で転送できますが、アプリケーション内でのみ転送できます。 その主な目的はまさにこうです。つまり、多くの値を転送するには大きすぎて1つずつコピーできないということです。

外部プリセットは、[グラフインスタンス](../../../compositing-graphs/creating-compositing-gra/graph-instances-sub-gra/graph-instances-sub-graphs.md)のすべての特定のパラメーター、[原子ノード](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/atomic-nodes.md)のほとんどの特定のパラメーター（[例外は公開できないパラメーター](../../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)）、およびSubstanceグラフの[パラメーター](../../graph-parameters/graph-parameters.md)パラメーターの公開された入力パラメーターで使用できます。

これらは、このメニューから簡単に保存して読み込むことができます。 保存したSBSPRSファイルは、他のノードまたはグラフにロードできます。

>[!NOTE]
>
> 部分的な一致も有効です。読み込まれたノードに存在しないSBSPRSに保存されたパラメータは、単に無視されます。 つまり、ほとんど同じようなノード（[タイルSamplerの色やグレースケールバージョンなど](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-sampler/tile-sampler.md)）間でプロパティを転送できます。 すべての共有パラメーターが読み込まれます。 照合は識別子とタイプに基づいて行われます。

![埋め込みプリセットの編集](parameter-presets.resources/parameter-presets-02.gif "埋め込みプリセットの編集"){width="512px"}

## 埋め込みプリセット

埋め込みプリセットは、外部プリセットとは動作が異なります。 主な利点は、SBSまたはSBSARファイルに格納されることです。そのため、Substance Painter、Maya、3DS Maxに簡単に転送してロードすることができます（現在、Substance 3D Sampler、UE4、Unityでは使用できません）。 ユーザーはSBSPRSファイルを混乱させる必要はありません。

ノードとグラフの間で転送することはできません（転送には外部プリセットを使用する必要があります）。 また、グラフのプロパティの入力パラメーターで、プレビューモード内の場合にのみ作成できます。

ワークフローは次のとおりです。

1. <b>入力パラメーター</b>の<b>プレビューモード</b>に切り替えます
1. 値を目的の結果に設定
1. 「プリセット」ドロップダウンの横にある<b>+</b>をクリックして、新しい埋め込みプリセットを作成すると、プリセットがすぐに作成され、保存されます

埋め込まれたプリセットの名前は変更できますが、後から変更することはできません。 ドロップダウンの横にある歯車アイコンと「+」アイコンをクリックすると、修正と削除を行うことができます。 プリセットを削除するには、プリセットの横にあるマイナス記号を押します。

プリセットを有効にするために行う必要はもうありません。SBSARとして公開されると、読み込み後にプリセットがSubstance Painterで利用できるようになります。

>[!IMPORTANT]
>
> [コンテキスト内の編集](../../../interface/preferences-window/preferences-window.md)を使用すると、<b>プリセット</b>タブが無効になります。
