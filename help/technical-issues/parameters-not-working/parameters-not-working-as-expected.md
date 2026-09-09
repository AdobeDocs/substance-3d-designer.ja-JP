---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/parameters-not-working-as-expected.html"
breadcrumb-title: ''
description: Substanceグラフのパラメーターが正常に機能しない問題をトラブルシューティングし、解決策を見つけます。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Parameters not working as expected
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パラメーターが予期したとおりに機能しない
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '303'
ht-degree: 5%

---


# パラメーターが予期したとおりに機能しない

ここでは、Substance 3D Designerでパラメーターが正常に機能しない一般的な原因の一覧を示し、それぞれのトラブルシューティング手順を説明します。

## プレビューモードでパラメーターが機能せず、公開されたSubstance 3Dアセット(SBSAR)です

<b>![（エラー）](../../assets/error.svg)問題</b>

Designerで[プレビューモード](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)を使用しているとき、またはそのグラフのSubstance 3Dアセット(SBSAR)のパラメーターリスト[公開済み](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)に含まれているときに、グラフの公開パラメーターの一部が&#x200B;*表示されていません*。

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

不足しているパラメーターは可能性が高い[静的パラメーター](../../glossary/glossary.md)です。グラフが&#x200B;*cooked*&#x200B;になった後（つまり、アルゴリズムを迅速かつ効率的に実行するために処理された後）、*その場で編集することはできません*。 グラフが&#x200B;*編集*&#x200B;または&#x200B;*公開*&#x200B;されるたびに、Designerでクッキングが行われます。 このような制限の影響を受けるパラメーターは、このドキュメントの[パラメーターの公開](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)ページの[制限](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)セクションに記載されています。

そのため、静的パラメーターはDesignerでは表示および編集できますが、公開されたSubstance 3Dアセットでは&#x200B;*非表示*&#x200B;になります。 Substance 3Dアセットに公開する前に、[プレビューモード](../../compositing-graphs/manage-parameters/exposing-a-parameter/exposing-a-parameter.md)を使用して、これらの制限が有効であることを確認できます。

静的パラメーターの一覧を次に示します。

| ノード | パラメーター |
| --- | --- |
| すべてのノード | タイリングモードのピクセル比 |
| [均一な色](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/uniform-color/uniform-color.md) | カラーモード |
| [ピクセルプロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md) | カラーモード |
| [ブレンド](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md) | 描画モードAlpha描画モードで切り抜く領域 |
| [FX-Map](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/fx-map/fx-map.md) | ブレンドモード |
| [象限](../../function-graphs/fxmaps/the-quadrant-node/the-quadrant-node.md) | パターン入力画像アルファ入力画像フィルター |

## パラメーターに適用されたSubstance関数グラフの結果が正しくありません

<b>![（エラー）](../../assets/error.svg)問題</b>

負の整数を使用した場合、ノードパラメータに適用されたSubstance関数グラフが期待値を出力しません。

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

負の整数は現在サポートされていません。 回避策として、[整数2](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/constant-nodes/constant-nodes.md)の値に負の整数の値を使用し、[ノード](../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/vector-and-swizzle-nodes/vector-and-swizzle-nodes.md)を使用して値を抽出します。
