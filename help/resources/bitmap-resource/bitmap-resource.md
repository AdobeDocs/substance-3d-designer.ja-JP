---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/resources/bitmap-resource.html"
breadcrumb-title: ''
description: Substance 3D Designerでビットマップリソースを読み込み、作成し、使用して、テクスチャベースのマテリアルを作成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Resources > Bitmap resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ビットマップリソース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '684'
ht-degree: 2%

---


# ビットマップリソース

ビットマップリソースは、Substanceパッケージ内のリソースです。 [atomicビットマップノードとは異なります。 アトミックビットマップノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)は、[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)内のビットマップを具体的に表したものです。

ビットマップは、Substance 3D Designerで最も一般的な非Graphリソースであり、通常は次のいずれかの用途に使用されます。

* [Designerによって内部的にベイク](../../bakers/bakers.md)されたベイク済みマップ、または別のアプリケーションによって外部でベイクされたアプリケーションです。
* パターン、経年劣化マップ、デカールなどのヘルパーテクスチャ。
* 描画のためのシンプルなグレースケールマスクです。[ビットマップノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)を使用して内部で作成するか、外部アプリを使用して作成します。

## ビットマップストレージ

通常、ビットマップは、Designerが扱う最大のリソースです。 そのため、Designerでは2つの主要なファイルタイプでこれらのファイルを処理する方法を理解していると便利です。

### Substance 3Dファイル(SBS)内

ビットマップがSBSにどのように保存されるかは、[リンクするか読み込むかに依存します。最初に概念を理解していることを確認してください。](../../resources/importing-linking-and-new/importing-linking-and-new-resources.md) 読み込まれたビットマップは、[ビットマップペイントツール](../../resources/bitmap-resource/bitmap-painting-tools/bitmap-painting-tools.md)を使用して編集できます。

SVG（ベクトルグラフィック）リソースとは異なり、ビットマップは、新しいリソースとして作成された場合や読み込まれた場合でも、常に外部に保存されます。 新しいSubstanceパッケージの場合、.SBSファイルがディスクに保存されるまで、それらはメモリに保持されます。 ディスクに保存されると、ビットマップはSBSファイルの横の&#x200B;*/resources*&#x200B;フォルダーに保存されます。

### Substance 3Dアセット(SBSAR)

[SBSARファイル](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)にはビットマップが埋め込まれています。つまり、ビットマップは最終的なSBSARファイルサイズに大きな影響を与えます。 ファイルサイズへの影響については、このページで詳しく説明します。 [SBSARファイルが公開されると、](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html)はグラフの出力の計算に使用されるビットマップのみが埋め込まれます。 未使用のビットマップはすべて最適化され、最終的なSBSARパッケージから除外されます。ファイル化には影響しません。

## ファイルタイプ、カラーモード、解像度

Substance 3D Designerでは、ビットマップのデータを簡単に編集および並べ替えできますが、次の点に注意してください。

* 解像度を2の累乗に設定します。つまり、<b>256、512、1024、2048、</b>などの標準のリアルタイムテクスチャサイズに従います。Designerは、この範囲外のテクスチャを最も近い解像度に再スケールします。 正方形の縦横比である必要はありません。
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

[公開されたSubstance 3Dアセット](https://helpx.adobe.com/substance-3d/unlisted/documentation/sddoc/publishing-sbsar-file-200574380.html) (SBSAR)に埋め込まれたビットマップのファイルサイズを最小化する方法に関する推奨事項については、[ベストプラクティス](../../best-practices/best-practices.md)の[ファイルサイズを縮小するガイドライン](../../best-practices/filesize-reduction-gui/filesize-reduction-guidelines.md)のページを参照してください。
