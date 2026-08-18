---
helpx_url: ""
breadcrumb-title: ''
description: ディスプレイスメントポップアップを使用すると、3Dシーンのメッシュに適用されたディスプレイスメントとテッセレーションを簡単に調整できます。
helpx_creative_field: ""
helpx_description: ""
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dビュー – ディスプレイスメントポップアップ
user-guide-description: ''
user-guide-title: ''
source-git-commit: c7b3b375144c8b58a8e7a7a408895a23e9bd1143
workflow-type: tm+mt
source-wordcount: '437'
ht-degree: 2%

---


# ディスプレイスメントポップアップ

<table style="margin-top: 32px; margin-bottom: 32px">
    <tr style="vertical-align: top; border: 0">
        <td style="border: 0">
            <p>3Dビューツールバーで使用できるディスプレイスメントポップアップでは、メッシュのディスプレイスメントとテッセレーションを直接制御できます。</p>
            <p>次の3つのパラメーターがあります。<ul>
                <li>高さスケール</li>
                <li>高さレベル</li>
                <li>テッセレーション</li></ul>
        </td>
        <td style="width: 60%; margin-left: 32px; border: 0">
            <img src="./displacement.resources/3d-view-displacement-popup-mograph.gif" alt="3Dビューのディスプレイスメントポップアップ" />
        </td>
    </tr>
</table>

## 高さスケール

メッシュ頂点の法線に沿ったディスプレイスメントの最大距離をシーン単位で指定します。<br>
Heightマップの値1.0の移動距離です。

Substanceグラフがマテリアルに接続されており、そのグラフに[出力ノード](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)が含まれている場合
<code>heightScale</code> 使用方法を選択した場合、ポップアップのHeightスケールパラメーターがそのマテリアルに対して&#x200B;*無効*になります
現在グラフによって動かされているからです。

>[!TIP]
> 
>[Heightを通常のワールドユニット](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/normal-map/height-normal-world-units/height-to-normal-world-units.md)ノードに使用し、&#39;Height深度&#39;パラメーターを&#39;Heightスケール&#39;値と一致させます
>ディスプレイスメントを使用する際に正しいシェーディングを確保する。

## 高さレベル

Heightの&#x200B;*中間点*として使用されるHeightマップのグレースケール値。
つまり、0.0の標高として使用されるしきい値です。

このしきい値を下回ると頂点が後方にディスプレイスされ、しきい値を上回ると
頂点を前方にディスプレイスする。

## テッセレーション

テッセレーションでは、セグメントに頂点を追加して個々のメッシュ面を分割してから接続します
1つの面が**6**&#x200B;になるように、すべての頂点の中心に新しい頂点が作成されます。

このパラメータは、面を再帰的に再分割する回数を定義します。

テッセレーションパラメーターの&#x200B;*スコープ*&#x200B;は、現在使用されている&#x200B;*レンダラー*によって異なります。適用できます
メッシュ単位またはマテリアル単位。

### メッシュ単位

[ラスタライザー](../3d-renderers/3d-renderers.md#rasterizer)または[GPU パストレーサー](../3d-renderers/3d-renderers.md#gpu-pathtracer)レンダラーを使用する場合、シーン内の各メッシュオブジェクトには&#x200B;*個の要素があります*
サブディビジョン値

サブディビジョンは状況に応じて適用されます。*不均一なHeight値*を持つサーフェスのみが最適化されるように、または
*非フラットHeightマップ*&#x200B;は、パラメーター値に関係なく細分割されます。

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
 ボタンをクリックし、プロパティドックで**レンダリング設定/診断モード**&#x200B;に移動して、**ワイヤーフレームを選択します
 （ワールドスペース）**&#x200B;オプション。

### OpenGL

次を使用します <img src="../3d-view.resources/3d-view-scene-toolbar-wireframe.png" width="22" /> **ワイヤーフレーム**
 をクリックします。
