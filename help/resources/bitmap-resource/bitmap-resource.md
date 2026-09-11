---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: テクスチャベースのマテリアル作成のために、Substance 3D Designerでビットマップリソースを読み込み、作成、使用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ビットマップリソース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '648'
ht-degree: 2%

---


# ビットマップリソース

ビットマップリソースは、Substanceパッケージ内のリソースです。 [atomicビットマップノードとは異なります。 アトミックビットマップノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)は、Substance グラフ[内のビットマップを表します。](../../compositing-graphs/substance-compositing-graphs.md)

ビットマップは、Substance 3D Designerで最も一般的なグラフ以外のリソースであり、通常は次のいずれかの用途に使用されます。

* [Designer](../../bakers/bakers.md)によって内部でベイクされたベイク済みマップ、または他のアプリケーションによって外部で送信されたアプリケーションです。
* パターン、経年劣化マップ、デカールなどのヘルパーテクスチャ。
* 描画のためのシンプルなグレースケールマスクです。[ビットマップノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)を使用して内部で作成するか、外部アプリを使用して作成します。

## ビットマップストレージ

通常、ビットマップは、Designerが扱う最大のリソースです。 そのため、Designerでは2つの主要なファイルタイプでこれらのファイルを処理する方法を理解していると便利です。

### Substance 3Dファイル内(SBS)

SBSでのビットマップの保存方法は、[リンクするか読み込むかによって異なります。最初に、この概念をよく理解してください。](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) 読み込まれたビットマップは、[ビットマップペイントツール](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)を使用して編集できます。

SVG(ベクターグラフィック)リソースとは異なり、ビットマップは、新しいリソースとして作成された場合や読み込まれた場合でも、常に外部に保存されます。 新しいSubstanceパッケージの場合、.SBSファイルがディスクに保存されるまで、それらはメモリに保持されます。 ディスクに保存されると、ビットマップはSBSファイルの横の&#x200B;*/resources*&#x200B;フォルダーに保存されます。

### Substance 3Dアセット(SBSAR)

[SBSARファイル](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)にはビットマップが埋め込まれています。つまり、ビットマップは最終的なSBSARファイルサイズに大きな影響を与えます。 ファイルサイズへの影響については、このページで詳しく説明します。 SBSARファイルが公開されると、グラフの出力の計算に使用されるビットマップのみが埋め込まれます。 未使用のビットマップはすべて最適化され、最終的なSBSARパッケージから除外されます。ファイル化には影響しません。

## ファイルタイプ、カラーモード、解像度

Substance 3D Designerでは、ビットマップのデータを簡単に編集および並べ替えできますが、次の点に注意してください。

* 解像度を2の累乗に設定します。つまり、<b>256、512、1024、2048、</b>など、標準のリアルタイムテクスチャサイズに従います。Designerは、この範囲外のテクスチャを最も近い解像度に再スケールします。 正方形の縦横比である必要はありません。
* 多くのファイルタイプがサポートされていますが、使用するケースに最適なファイルタイプを選択してください。 PNGやTGAなどの<b>可逆圧縮や非圧縮</b>のファイルタイプは、JPGやDDSよりも画質が高くなります。
* 必要なカラー、グレースケール、またはアルファチャンネルに応じて、<b>カラーモードを正しく設定</b>してください。

## ビットマップ属性

パッケージ内のビットマップリソースには、カスタマイズ可能な属性が多数あります。 ほとんどの属性には大きな目的がなく、ライブラリフィルター用ですが、少数の属性はファイルサイズに影響します。

| 属性名 | 目的 |
| --- | --- |
| 識別子 | パッケージ内のビットマップリソースを参照するために使用される関数は、一意である必要があります。 |
| ファイルパス | リソースによって参照されるビットマップのディスク上のパスです。 |
| 説明 | このリソースの[エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)および[ライブラリ](../../interface/the-library/the-library.md)のツールヒントに表示された説明です。 |
| カテゴリ | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| ラベル | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| 作成者 | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| 作成者の URL | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| タグ | [ライブラリ](../../interface/the-library/the-library.md)の[リソースの並べ替えとキュレーション](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)に使用されます。 |
| ユーザーデータ | オプションの追加データ。ビットマップでは使用されません。 |
| ライブラリで表示 | ビットマップを[ライブラリビューで非表示にするかどうかを決定します。](../../interface/the-library/the-library.md) |
| ビットマップ形式 | RawまたはJpegは、SBSARファイルサイズに大きな影響を与えます。 詳しくは、[ファイル化の削減ガイドライン](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)を参照してください。 |
| ビットマップ圧縮品質 | Jpeg圧縮にのみ影響し、画質/ファイルサイズのバランスを決定します。 |

## Filesizeの縮小

[公開されているSubstance 3Dアセット(SBSAR)](../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)に埋め込まれたビットマップのファイルサイズを最小化する方法に関する推奨事項については、[ベストプラクティス](../../best-practices/best-practices.md)の[ファイルサイズを縮小するガイドライン](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)のページを参照してください。
