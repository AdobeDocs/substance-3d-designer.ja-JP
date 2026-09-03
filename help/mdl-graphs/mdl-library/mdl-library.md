---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/mdl-graphs/mdl-library.html"
breadcrumb-title: ''
description: カスタムマテリアルを作成するには、Substance 3D Designerのマテリアル定義言語ライブラリにアクセスします。
helpx_creative_field: ""
helpx_description: Designer > MDL graphs > MDL library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: MDLライブラリ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# MDLライブラリ

[MDLグラフ](../../mdl-graphs/mdl-graphs.md)に関するコンテンツのライブラリとSubstance 3D Designerに含まれる資料を表示します。 また、[ライブラリ](../../interface/the-library/the-library.md)でのカスタムコンテンツのインストールと管理についても説明します。

## ライブラリ内のMDLコンテンツ

MDLグラフで使用できるノードは、[ライブラリ](../../interface/the-library/the-library.md)の<b>mdl</b>セクションにあります。 ノードは、定義されているMDLモジュールに従ってフィルタに配置されます。\
モジュールがサブフォルダーに格納されている場合、この階層はライブラリで&#x200B;*カテゴリ*&#x200B;として&#x200B;*ミラー*&#x200B;されます。

このセクションには、次のソースからのコンテンツが含まれます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 組み込みコンテンツ

Designerには、MDLグラフを作成するための基本的な構成要素と、すぐに使用できる完全なマテリアル定義を含むMDLモジュールが含まれています。

このコンテンツは、次のインストールディレクトリの下のこの場所に保存されます： `./resources/view3d/iray/`

### カスタムコンテンツ

組み込みのコンテンツに加えて、*独自の* MDLモジュールをライブラリに追加できます。

実際、[プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)の<b>MDL</b>セクションに一覧表示されているディレクトリに存在するMDLモジュールは、プロジェクトファイル間でこのセクション&#x200B;*累積的に*&#x200B;追加されます。

### NVIDIA vMaterial

NVIDIAの[vMaterials](https://developer.nvidia.com/vmaterials)ライブラリがインストールされている場合は、その&#x200B;*独自のカテゴリ*&#x200B;の下のライブラリに&#x200B;*自動的に追加*&#x200B;されます。

</td>
<td style="border: 0;" valign="top">

![ライブラリのMDLリソース](mdl-library.resources/mdl-library-01.png "ライブラリのMDLリソース")

ライブラリの&#x200B;*「mdl」セクション、vMaterialsライブラリ、およびカスタムコンテンツはフレーム化されています*

</td>
</tr>
</table>

## 3DビューのMDLコンテンツ

Irayレンダラーを使用する場合、ライブラリで利用可能なすべてのMDLモジュールを[3Dビュー](../../interface/3d-view/3d-view.md)で使用できます。

<b>マテリアル</b>メニューを開き、*シーンマテリアルのサブメニュー*&#x200B;を開いて、利用可能なMDLモジュールを参照します。 リストには次のものが含まれます。

* 組み込みコンテンツ
* カスタムコンテンツ
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* [MDLグラフ](../../mdl-graphs/mdl-graphs.md)を読み込みました

![3DビューのMDLマテリアル](mdl-library.resources/mdl-library-02.png "3DビューのMDLマテリアル")

*3DビューのMDLマテリアル*
