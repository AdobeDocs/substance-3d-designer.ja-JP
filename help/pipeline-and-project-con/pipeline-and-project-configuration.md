---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration.html"
breadcrumb-title: ''
description: Substance 3D Designerでパイプラインとプロジェクトを設定し、ワークフローと出力を最適化します。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パイプラインとプロジェクトの構成
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '596'
ht-degree: 0%

---


# パイプラインとプロジェクトの構成

Substance 3D Designerには、パイプライン使用のためにアプリケーションを設定する強力なシステムがあります。 階層型の「**プロジェクト**」ファイルの高度なシステムを通じて、すべての構成とライブラリのコンテンツをバージョン管理しつつ、StudioまたはProject標準に即座に構成できます。 このシステムの主な目的は、パイプラインに関連するすべての設定を一元化しながら、複数の設定を上書きして相互に拡張できるようにすることです。

>[!WARNING]
>
> このシステムは、要件が単純なシングルユーザーを対象としたものではなく、*大規模なプロジェクトやチームが存在し*&#x200B;組織のニーズが高いスタジオを対象としています。 このシステムをフルに活用するには、かなりの量の計画と準備を行い、ある程度の自動化されたセットアップを推奨します。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 構成ファイル階層

Designerには3つの階層または構成ファイルがあり、それぞれ目的が異なります。 Windowsの場合、すべてのファイルは&#x200B;*～User\AppData\Local\Adobe\Adobe Substance 3D Designerにあります。*

この図は、新規インストール後の、Designerのデフォルト設定での異なるファイル間の関係を示しています。

</td>
<td style="border: 0;" valign="top">

![構成ファイル階層](pipeline-and-project-configuration.resources/pipeline-and-project-configuration-01.png "構成ファイル階層")

</td>
</tr>
</table>

* <b>[User\_Preferences.XML](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)</b>には、一般的なプログラム設定が含まれていますが、1つを除くすべてがプロジェクトパイプラインに関連していません。 このファイルは一意であり、スワップアウトできません。Designerはこの正確なファイルを使用するようにハードコードされています。\
  このファイルには、設定ファイルへの参照が1つだけ含まれています。
* <b>[Default\_Configuration.SBSCFG](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)</b>は、名前が異なる他のSBSCFGファイルとスワップアウトできますが、同時に使用できるSBSCFGファイルは1つだけです。\
  プロジェクトファイルへの複数の参照が含まれています。 *既定の構成では、これらのファイルは明示的に定義されていませんが、ハードコードされています！*
* <b>[Project.SBSPRJ](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)</b>ファイルには、プロジェクト/パイプラインに関連する設定が含まれています。 階層に複数のプロジェクトを定義し、前に定義したプロジェクトをオーバーライドまたは展開できます。

## Designerパイプラインの設定

このページの子ページではすべての種類のファイルについて詳しく説明していますが、Designerのカスタム設定を理想的に定義する方法の概要は次のとおりです。

1. <b>プロジェクトファイルに追加する設定を識別してグループ化します。</b> これはスタジオごとに異なり、一定の計画が必要です。\
   ほとんどの場合、少なくとも2つのプロジェクトを定義する必要があります。1つはグローバルなスタジオ全体のデフォルト（標準テンプレート、シェーダーファイル、ベイク設定など）用で、もう1つはライブラリコンテンツなどのより具体的なコンテンツ用です。 異なるプロジェクトを同時に実行している場合は、それぞれに複数のプロジェクト構成を作成することをお勧めします（合計で3つ以上）。
1. <b>関連する[SBSPRJファイル](../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)を作成し、それらをバージョン管理の下に配置してコンテンツを配置します。</b> Designerパイプラインおよびライブラリのコンテンツと、実際のプロジェクトのコンテンツおよびリソース（3Dモデル、テクスチャ、コード）を分離するために、*別のリポジトリ*&#x200B;を作成することを強くお勧めします。
1. <b>すべてのプロジェクトファイルを一覧表示する[ SBSCFG構成](../pipeline-and-project-con/configuration-list-sbscfg/configuration-list-sbscfg.md)ファイルを作成し、バージョン管理</b>の下に配置します。 複数のプロジェクトがある場合は、プロジェクトごとに構成を作成できます。
1. <b>各ユーザーの[User\_Preferences.xml](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)が関連する構成ファイルを参照するように設定します。</b>\
   すべてのユーザーに手動で行わせることも、XMLファイルに行を挿入してスクリプトを作成することもできます。 [関連ページの詳細情報](../pipeline-and-project-con/user-preferences-aut/user-preferences-automating-setup.md)。
