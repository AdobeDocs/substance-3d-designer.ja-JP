---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/best-practices/performance-optimization-guidelines.html"
breadcrumb-title: ''
description: グラフのパフォーマンスを向上させ、処理時間を短縮するための、Substance 3D Designerのパフォーマンス最適化ガイドラインについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Performance optimization guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パフォーマンス最適化ガイドライン
user-guide-description: ''
user-guide-title: ''
source-git-commit: 583588c4e12e3d0857c2b16200945e36ea523151
workflow-type: tm+mt
source-wordcount: '1027'
ht-degree: 0%

---


# パフォーマンス最適化ガイドライン

## Substance グラフ

[グラフ](../../compositing-graphs/substance-compositing-graphs.md)が複雑になるほど、レンダリングに必要な処理能力が高まります。 <b>複雑さとレンダリング速度のバランスを取ってください</b>。\
ゲームなどのリアルタイムグラフィックスアプリケーションで使用する場合は、*特に*&#x200B;重要です。

一般に、実行時に変更可能なカスタムパラメーターを表示するノードは、<b>グラフの終わりにできるだけ近い場所</b>に配置する必要があります。

これは、各ノードの出力が可能な限りキャッシュされるためです。 したがって、ツィーク可能ノードのグラフが上がるほど、これらの表示されるパラメーターのいずれかが変更されるたびに多くの出力を処理する必要があります。 表示したノードがノードの終わりに近い場合、グラフと出力ノードの間にあるいくつかのノードのみを再計算する必要があります。

たとえば、グラフの先頭で均一カラーをツィークすると、次のすべてのノードが再計算されます。 出力の直前に配置したHSLノードを微調整すると、このノードのみが再計算され、グラフのパフォーマンスが大幅に向上します。

次のガイドラインに注意してください。

### パフォーマンスに関する一般設定

+++GPU エンジンは、CPU エンジンよりもはるかに高速です
サポートされていない（統合された）グラフィックカードがない場合は、GPU Substance エンジンを使用します（ホットキーF9で変更）。

+++

+++グラフの親解像度の切り替えが遅い
グラフ、キャッシュ、およびすべてのサムネールを再計算します。 不必要な再計算が大量に発生する（8192解像度に書き出す場合など）ことを避けるため、書き出しダイアログの[[バッチ] </b>タブ](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)を使用することをお勧めします。<b>

+++

+++極端な場合は、メモリキャッシュを増やす必要があります
アプリケーション[は、画像キャッシュに使用できるRAMの容量を制限](../../interface/preferences-window/preferences-window.md)しますが、これを上書きして増やすことができます（注意）。

+++

### グラフ最適化

+++ノードの解決策と継承全般に注意してください。
値を大きくするとパフォーマンスに重大な影響が生じるため、マテリアルの使用方法と、使用するデータ・サイズを減らすことができるかどうかを検討してください。

[ノードの解像度（出力サイズ）](../../compositing-graphs/output-size/output-size.md)と[グラフの継承](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)について詳しく知ることをお勧めします。

+++

+++カラーが不要な場合はグレースケールを使用
カラー操作はグレースケール操作の4倍の時間がかかります。 また、カラーとグレースケールの間の文字変換も最小限に抑えることをお勧めします。

+++

+++16ビットが不要な場合は8ビットを使用します
Substance engine (SSE2) *のCPUバージョンは、実際には16ビットの色または8ビットのグレースケールをサポートしていません*。 GPUエンジンは、8/16ビットとグレースケール/カラーの4つの組み合わせをすべてサポートしています。 *現在、UnityおよびUnreal EngineプラグインではCPUエンジンのみが使用されています*。

+++

+++可能な限りノード出力サイズを最小化する
場合によっては、ノードのサイズを小さくしても最終結果には影響しませんが、パフォーマンスに影響することがあります。 例えば、同じ出力サイズに設定された均一カラーノードをドキュメントで使用しても意味がありません。均一カラーを絶対[16px x 16px]に設定し、その後のノードを「親を基準」に設定する必要があります。 通常、この方法は、パーリン雑音などの低周波画像に適しています。

+++

+++16*16ピクセルより小さい画像は使用しないでください
これにより、レンダリングのパフォーマンスが低下します。

+++

+++ブレンドノードを使用する場合は、不要な場合はAlphaブレンドを無効にします


+++

+++ブラーとワープは、最もCPUに負荷をかけるノードです


+++

+++一部のノイズジェネレーターは、描画されるパターンの量の影響を受けます
たとえば、[Tile Generator](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/tile-generator/tile-generator.md)ノードは、追加したパターンの処理が遅くなります。

+++

+++一部のノイズはスケール係数の影響を受けます
この要素は、実際にはより多くのパターンを描画します。 影響を受けるノードには、ノイズ、セルパターンなどが含まれます。ホワイトノイズパターンが必要な場合は、スケール値が非常に大きいノイズを使用せずに、[ホワイトノイズ](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise/white-noise.md)または[ホワイトノイズ高速](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md)のノードを使用します。

+++

+++逆に、いくつかの非常に高速なノイズ発生器があります
[高速のホワイトノイズ](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/white-noise-fast/white-noise-fast.md)、[フラクタル和ベース](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/fractal-sum-base/fractal-sum-base.md)、[異方性ノイズ](../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/noises/anisotropic-noise/anisotropic-noise.md)などです。

+++

+++場合によっては、大量の画像サンプリング機能に注意してください
[ピクセルプロセッサ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/pixel-processor/pixel-processor.md)を除き、関数はCPUエンジンで実行されます。 [Value Processors](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/value-processor/value-processor.md)または[FXmaps](../../function-graphs/fxmaps/fxmaps.md)で大量のイメージサンプリング（$pos座標の変更）を行う場合、VRAMとCPU RAMの切り替えが頻繁に発生し、パフォーマンスの遅延が発生する可能性があります。

+++

### モバイル使用の最適化

+++ワープおよびFXマップの使用はお勧めしません
パフォーマンスの面で非常に高コストです。

+++

+++ぼかしノードを使用しない
代わりにダウンスケール変換を使用してください。

+++

+++できるだけグレースケールで作業
グラフの最後でカラーモードに切り替えます。

+++

+++出力間でノードをできるだけ共有する


+++

### 埋め込みビットマップのサイズ最適化

[ビットマップ](../../resources/bitmap-resource/bitmap-resource.md)の[出力サイズ](../../compositing-graphs/output-size/output-size.md)は、既定では[&#39;絶対&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されています。 つまり、ビットマップがノードチェーンを介して出力に接続されている場合、最終的な出力は必ず埋め込まれたビットマップのサイズになります。\
ビットマップの後に挿入するノードの出力サイズは[&#39;入力に対する相対&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されます。 これは、ノードがビットマップのサイズを継承し、このサイズをノードチェーンから出力に伝えることも意味します。 これを修正するには、ビットマップの後のノードの出力サイズを[&#39;親に相対的&#39;](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定する必要があります。

グラフがダイナミック解像度に設定されている場合は、埋め込まれたビットマップの出力サイズを親に相対的に変更できます。\
こうすると、ビットマップのサイズが親グラフに基づいて変わり、グラフがビットマップで必要な解像度よりも高い解像度を処理している状況にはならなくなります。

>[!WARNING]
>
> [Bitmap](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードを「親に相対的」に設定し、そのノードをSubstance 3D グラフ (SBSAR)に[公開](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)すると、元のサイズではなく&#x200B;**256x256**&#x200B;の解像度でビットマップが保存されます。 代わりに、ビットマップノードの[継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)を&#39;絶対&#39;として[出力サイズ](../../compositing-graphs/output-size/output-size.md)に維持し、ビットマップノードの直後に、[変形 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)ノードを&#39;親に相対的&#39;に設定することをお勧めします。

![埋め込みビットマップの最適化1](performance-optimization-guidelines.resources/input-1.jpg "埋め込みビットマップの最適化1")

![埋め込みビットマップの最適化2](performance-optimization-guidelines.resources/relativetoparent.jpg "埋め込みビットマップの最適化2")

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

また、ビットマップリソースのフォーマットをJpegに設定して、パブリッシュされるSubstance 3Dアセット(SBSAR)のサイズを最小限に抑えることをお勧めします。

</td>
<td style="border: 0;" valign="top">

![埋め込みビットマップの最適化3](performance-optimization-guidelines.resources/format.jpg "埋め込みビットマップの最適化3")

</td>
</tr>
</table>
