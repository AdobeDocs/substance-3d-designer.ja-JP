---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/best-practices/filesize-reduction-guidelines.html"
breadcrumb-title: ''
description: Substanceグラフのファイルサイズを縮小して、パフォーマンスとストレージの要件を最適化するためのガイドラインについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Best Practices > Filesize Reduction Guidelines
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: Filesizeの削減ガイドライン
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '822'
ht-degree: 1%

---


# 概要

場合によっては、[Substance 3Dアセット(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)の合計ファイルサイズが重要な要素になることがあります。 このページでは、ファイルサイズを縮小する際に留意すべき重要な領域と設定について説明します。

ファイルサイズは主に[埋め込みビットマップ](../../resources/bitmap-resource/bitmap-resource.md)によって決定されます。 これらは、リンク、埋め込み、またはベイク処理され、リソースとして[Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)ファイル(SBS)に追加されたファイルです。 グラフで使用されているビットマップ（つまり、直接またはノードチェーンを介して出力に接続されているビットマップ）のみが、Substance 3Dアセットで公開されます。 Substance 3Dファイルでは、ビットマップのリソースはファイルの外部に保存されるので、ビットマップがファイルのサイズに影響することはありません。

>[!IMPORTANT]
>
> すべての[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードの[出力サイズ](../../compositing-graphs/output-size/output-size.md)プロパティが&#x200B;*絶対* [継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)に設定されていることを確認してください。 そうでない場合は、参照されている[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)は、公開されたSubstance 3Dアセットファイルにデフォルトの256\*256解像度で保存されます。これにより、* 1つ以上の出力の品質に影響します*。

## ファイルサイズの係数

SBSARのファイルサイズの合計に影響を与える要因はいくつかあります。 以下に簡単な説明を示します。

+++解決策
明らかに大きな効果がある。 Substanceファイルを大きな解像度で動作させる場合もあります。その場合は、できる限り小さな解像度を使用してください。 標準の解像度マスクを使用して、小さなビットマップを大きく見せることができます。

*見つかった場所：外部ソフトウェア、またはDesignerでのビットマップの読み込み/再書き出し。*

+++

+++ファイルのカラーモード
書き出す前に画像エディターで設定すると、Rawビットマップ形式を使用する場合に、カラーモードもファイル化に影響します。 グレースケールのみのビットマップは、RGB(A)画像よりも小さくなります。

*[出力ノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)を正しくセットアップしているときに、外部ソフトウェアで見つかった場合、またはDesignerでビットマップを読み込み/再書き出しした場合。*

+++

+++ファイル形式
画像のファイル形式によって違いが生じますが、無視できる場合もあります。 Photoshopのようなプログラムでは、JPGの圧縮率をわずかに制御でき、適切な中間段階を迎える場合があります。

*見つかった場所：外部ソフトウェア、またはDesignerでのビットマップの読み込み/再書き出し。*

+++

+++グラフでの使用
ビットマップノードのモードは、Designerによるファイルの圧縮方法にも影響します。グラフでグレースケールモードファイルをカラービットマップとして使用すると、ファイルが大きくなります。 これらを正しく設定してください。

*ビットマップノードプロパティで見つかりました：[。](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)*

+++

+++パッケージ内のビットマップ形式
リソースプロパティで、「Raw」圧縮と「Jpeg」圧縮の間で選択できます。 これは、最終結果に大きな影響を与える可能性があります。

*見つかった場所：ビットマップリソースプロパティ、エクスプローラウィンドウ。*

+++

+++パッケージのビットマップ圧縮品質
「Jpeg」ビットマップ形式を使用する場合、以下のスライダーは画質とファイルサイズに影響を与える可能性があります。 このスライダは予測可能な動作ではありませんが、1は最高画質のJPG圧縮に対応し、0.5は最小サイズに対応します。

*見つかった場所：ビットマップリソースプロパティ、エクスプローラウィンドウ。*

+++

+++公開時の圧縮モード
SBSARにパブリッシュする場合、圧縮は「自動」、「最高」、「なし」のいずれかを選択できます。これらは、「Raw」ビットマップ形式を使用している場合に大きな違いを生み出します。 また、輸出速度にも大きな影響を与えます。 通常、「なし」は品質の向上を提供しないため、使用はお勧めしません。

*見つかった場所： SBSARパッケージの最終公開設定。*

+++

## Filesizeの比較

次の表は、すべての設定が相互に与える影響を示しています。 使用されているビットマップは、4096 x 4096の生成されたノイズの画像で、Photoshopから画質8で24ビットTGAまたはJPGとして書き出されます。 TGAはグレースケールおよびRGBAモードとしても書き出されました。

グラフでは、1つの出力にコネクトされた1つのビットマップノードが配置されるだけです。 ビットマップモードは、ソースファイルモードに応じて設定されます。

右側の表は完全な結論を導き出すものではありませんが、視覚的な結果とファイルサイズを比較する際に、次の情報を確認できます。

* 「RAWビットマップ+圧縮（最適）」を選択すると、許容されるファイルサイズで最高品質が得られます。
* 圧縮済みソースファイルを使用すると、多くの場合、ファイルサイズが小さくなりますが、品質が低下します。
* ファイルサイズは最小ですが、JPGパッケージフォーマットはquality 0.5で最低の画質が得られます。
* グレースケールは、ファイル化したときに必ずしも小さくなるとは限りませんが、同様の設定ではカラーよりも画質が高くなります。

>[!NOTE]
>
> **Jpegビットマップ形式**
> 
> 法線マップ、ベクトルマップなどの高精度を必要とする特殊マップは、アーティファクトが非常に目立つことがあるので、Jpeg圧縮に設定しないようにしてください。

| 元の画像 | カラーTGA | カラーJPG | グレースケールTGA | グレースケールJPG |
| --- | --- | --- | --- | --- |
| <b>Rawビットマップ形式</b>圧縮モード： *なし* | 48 MB | 48 MB | 16 MB | 16 MB |
| <b>Rawビットマップ形式</b>圧縮モード： *最適* | 9.11 MB | 3.37 MB | 5.06 MB | 4.75 MB |
| <b>Jpegビットマップ形式</b>圧縮品質： *1* | 5.09 MB | 1.94 MB | 6.30 MB | 2.49 MB |
| <b>Jpegビットマップ形式</b>圧縮品質： *0.5* | 231 KB | 230 KB | 626 KB | 569 KB |
| <b>Jpegビットマップ形式</b>圧縮品質： *0* | 407 KB | 433 KB | 990 KB | 808 KB |
