---
helpx_url: ""
breadcrumb-title: ""
description: ディスプレイスメントポップアップを使用すると、3D シーン内のメッシュに適用されるディスプレイスメントとテセレーションを簡単に調整できます。
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D ビュー - ディスプレイスメントポップアップ
user-guide-description: ""
user-guide-title: ""
source-git-commit: 10be7678f386c925d4bff6d59e2b85ffc04becd8
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 2%
---

# ディスプレイスメントポップアップ

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>3D ビューツールバーで使用できるディスプレイスメントポップアップでは、メッシュのディスプレイスメントとテセレーションを直接制御できます。</p>
            <p>次の3つのパラメーターがあります。<ul>
                <li>高さスケール</li>
                <li>高さレベル</li>
                <li>テッセレーション</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="3D ビューのディスプレイスメントポップアップ" />
        </td>
    </tr>
</table>

## 高さスケール

頂点の法線に沿ったディスプレイスメントの最大距離（シーン単位）。<br>
高さマップ内の値1.0の移動距離です。

Substance グラフがマテリアルに接続されており、そのグラフに[出力ノード](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)が含まれている場合
<code>heightScale</code> 使用方法を選択した場合、ポップアップのHeightスケールパラメーターは、そのマテリアルに対して&#x200B;*無効*になります
現在グラフによって動かされているからです。

>[!TIP]
> 
>[Heightを通常のワールドユニット](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md)ノードに使用し、&#39;Height深度&#39;パラメーターを&#39;Heightスケール&#39;値と一致させます
>ディスプレイスメントを使用する際に正しいシェーディングを確保する。

## 高さレベル

Heightの&#x200B;*中間点*として使用される高さマップのグレースケール値。
つまり、0.0の標高として使用されるしきい値です。

しきい値を下回ると頂点が逆方向に移動し、しきい値を上回ると
頂点が前方に移動している。

## テッセレーション

テセレーションでは、個々のメッシュ面を細かく分割し、それぞれの線分に頂点を加えてから連結します
1つの頂点が&#x200B;**6**&#x200B;になるように、中央の新しい頂点へのすべての面を配置します。

このパラメーターは、面を再帰的に再分割する回数を定義します。

テセレーションパラメーターの&#x200B;*scope*&#x200B;は、現在使用されている&#x200B;*renderer*によって異なります。適用できます
メッシュ単位またはマテリアル単位。

### メッシュ単位

[ラスタライザ](../3d-renderers/3d-renderers.md#rasterizer)または[GPU パストレーサー](../3d-renderers/3d-renderers.md#gpu-pathtracer)のレンダラーを使用する場合、シーン内の各メッシュオブジェクトには&#x200B;*個の要素が存在します*
サブディビジョン値

サブディビジョンは状況に応じて適用されます。*不均一なHeight値*を持つサーフェスのみが最適化されるように、または
*非フラットHeightマップ*&#x200B;は、パラメーター値に関係なく細分割されます。

>[!TIP]
>
>テセレーション手法には、実際に発生するテセレーションに関係なく実行される準備手順が含まれます。 （例： `Tessellation factor = 1`）
>高ポリゴンメッシュの場合、この手順は時間がかかることがあり、ディスプレイスメントを使用する際にパフォーマンスに大きな影響を与えます。
>
>テセレーションが不要な場合は、[シーンブラウザー](../scene-browser/scene-browser.md#scene-tree)に一覧表示された`Mesh`オブジェクトのプロパティで&#x200B;**Refine level**&#x200B;パラメーターを`0`に設定することで、この手法を完全に無効にできます。

### マテリアル単位

[OpenGL](../3d-renderers/3d-renderers.md#opengl)レンダラーを使用する場合、シーン内の各マテリアルには&#x200B;*個別の*サブディビジョン値があり、サブディビジョン値は次のとおりです
*そのマテリアルを使用しているすべての面*&#x200B;に適用されます。

サブディビジョンはコンテキストに依存しません。サーフェスは、カレントに関係なく、指定した時間だけ再分割されます
Height値またはテクスチャ。

## テッセレーションの視覚化

メッシュの&#x200B;**ワイヤーフレーム**&#x200B;を確認すると、テッセレーションの結果を視覚化できます。<br>
各レンダラーのワイヤーフレームを表示する手順は、以下のとおりです。

### ラスタライザ/GPU パストレーサー

次を使用します <img src="../3d-view.resources/3d-view-scene-toolbar-render-settings.png" width="22" /> **レンダラー設定**
 ボタンをクリックし、プロパティドックで&#x200B;**レンダリング設定/診断モード**&#x200B;に移動して、**ワイヤーフレームを選択します
 （ワールドスペース）**&#x200B;オプション。

### OpenGL

次を使用します <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **ワイヤーフレーム**
 をクリックします。
