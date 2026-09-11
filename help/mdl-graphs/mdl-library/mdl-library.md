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
source-git-commit: ea2e2d76d225a0e17c84c3312934f62aa5ef3915
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---


# MDLライブラリ

[MDL グラフ](../../mdl-graphs/mdl-graphs.md)に関連するコンテンツと、Substance 3D Designerに含まれるマテリアルのライブラリです。 また、[ライブラリ](../../interface/the-library/the-library.md)でのカスタムコンテンツのインストールと管理についても説明します。

## ライブラリ内のMDLコンテンツ

MDL グラフで使用できるノードは、[Library](../../interface/the-library/the-library.md)の<b>mdl</b>セクションで利用できます。 ノードは、定義されているMDL モジュールに従ってフィルタに配置されます。\
モジュールがサブフォルダーに格納されている場合、この階層はライブラリで&#x200B;*カテゴリ*&#x200B;として&#x200B;*ミラー*&#x200B;されます。

このセクションには、次のソースからのコンテンツが含まれます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 組み込みコンテンツ

Designerには、オーサリングMDL グラフの基本的な構成要素と、すぐに使用できる完全なマテリアルMDL モジュールが含まれています。

このコンテンツは、次のインストールディレクトリの下のこの場所に保存されます： `./resources/view3d/iray/`

### カスタムコンテンツ

組み込みのコンテンツに加えて、*独自の* MDL モジュールをライブラリに追加できます。

実際、[プロジェクトMDL モジュール](../../interface/preferences-window/project-settings/project-settings.md)の<b>MDL</b>セクションに記載されているディレクトリに見つかった設定は、プロジェクトファイル全体で&#x200B;*累積的に*&#x200B;このセクションに追加されます。

### NVIDIA vMaterial

NVIDIAの[vMaterials](https://developer.nvidia.com/vmaterials)ライブラリがインストールされている場合は、その&#x200B;*独自のカテゴリ*&#x200B;の下のライブラリに&#x200B;*自動的に追加*&#x200B;されます。

</td>
<td style="border: 0;" valign="top">

![ライブラリのMDLリソース](mdl-library.resources/mdl-library.png "ライブラリのMDLリソース")

ライブラリの&#x200B;*「mdl」セクション、vMaterialsライブラリ、およびカスタムコンテンツはフレーム化されています*

</td>
</tr>
</table>

## 3D ビュー内のMDLコンテンツ

Irayレンダラーを使用する場合、ライブラリで使用可能なすべてのMDL モジュールを[3D ビュー](../../interface/3d-view/3d-view.md)で使用できます。

<b>マテリアル</b>メニューを開き、*シーンマテリアルのサブメニュー*&#x200B;を開いて、利用可能なMDL モジュールを参照します。 リストには次のものが含まれます。

* 組み込みコンテンツ
* カスタムコンテンツ
* NVIDIA [vMaterials](https://developer.nvidia.com/vmaterials)
* [MDLグラフ](../../mdl-graphs/mdl-graphs.md)を読み込みました

![3DビューのMDLマテリアル](mdl-library.resources/mdl-apply-in-3dview-material-list.png "3DビューのMDLマテリアル")

*3DビューのMDLマテリアル*
