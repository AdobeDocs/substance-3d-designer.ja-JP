---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/project-configuration-files-sbsprj.html"
breadcrumb-title: ''
description: Substance 3D DesignerでSBSPRJプロジェクト設定ファイルを使用して、プロジェクト設定を管理する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Project Configuration Files - SBSPRJ
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: プロジェクト構成ファイル – SBSPRJ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '1001'
ht-degree: 0%

---


# 概要

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

<b>プロジェクト構成ファイル</b>は、Substance 3D Designerの構成に使用される、最も複雑で拡張性の高いファイルです。

次の「子」プロジェクトが前の「親」を展開またはオーバーライドする複数のプロジェクト設定ファイルを使用できるという点で特別です。 Designerは、明示的に必要な場合を除き、親の設定やデフォルト設定に頼ることができるため、設定を変更したりプロジェクトファイルに追加したりしないでください。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSPRJファイルアイコン](project-configuration-files-sbsprj.resources/project-configuration-files-sbsprj-01.png "SBSPRJファイルアイコン")

</td>
</tr>
</table>

デフォルトでは、Designerには2つのアクティブなプロジェクト設定があります。

<b>既定のプロジェクト： </b>すべての既定の設定が含まれます。Designerは新規インストール時に付属しています。*読み取り専用です。変更または削除できません。*

<b>ユーザープロジェクト： </b>既定は読み取り専用であるため、*ユーザーによるすべての変更*&#x200B;は既定でこのプロジェクトに反映されます。 *削除できません。*

この基本的な設定により、デフォルトのライブラリやその他の設定を壊したり変更したりすることはできませんが、それでも単一のアマチュアのユーザーが複雑な設定を気にすることなく自分の変更を追加することができます。

## 展開またはオーバーライド

連続するプロジェクトのほとんどの設定は、前のプロジェクトの設定よりも<b>優先</b>されます。 例えば、カスタムプロジェクトファイル内の別の接線空間プラグインは、デフォルトまたはユーザープロジェクトで定義されているTSプラグインを上書きします。 したがって、明示的に必要な場合を除き、子プロジェクトの設定を上書きまたは変更しないことをお勧めします。

ただし、親の設定を上書きするのではなく、親の設定に対して<b>展開</b>する設定もあります。 これらの設定で最も顕著なのは、ライブラリパスとフィルターであるため、ライブラリを上書きするのではなく、常にライブラリにコンテンツを追加します。 さらに、エイリアス（相対ファイルパスのパスキーワード）が展開され、重複が定義されている場合はオーバーライドされます。 これにより、コンテンツファイルパスと参照を詳細に制御できます。

## プロジェクトファイルの内容

プロジェクトファイルには、次の設定を含めることができます。

<b>3D ビュー: </b>既定のシェーダー、HDR、およびシーンの状態の定義。

<b>エイリアス： </b>相対パスのキーワードエイリアス。

<b>ベイク: </b>名前付け規則をベイクするための設定です。

<b>全般： </b>グラフテンプレート、接線空間プラグイン、標準および画像形式の既定値。

<b>ライブラリ： </b>ライブラリに表示する監視対象のパス。

<b>スクリプト： </b>コールバックスクリプトとインタープリター。

<b>バージョン管理: </b>バージョン管理をDesignerに統合するための設定。

## プロジェクトファイルの変更

プロジェクトの構成は、他のすべての種類と同様に、（<b>.sbsprj</b>という拡張子を持つ）構造化XMLファイルとして保存されます。このファイルは、Designer UIまたは外部テキストエディターを使用して変更できます。

## Substance 3D Designer内

プロジェクトファイルの管理およびプロジェクト設定の変更の詳細については、[プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)ページを参照してください。

プロジェクトファイルには、[ライブラリ](../../interface/the-library/the-library.md)のカスタム<b>カテゴリ</b>と<b>フィルター</b>も含まれています。これらの詳細については、[カスタムコンテンツとフィルターの管理](../../interface/the-library/managing-custom-content/managing-custom-content-and-filters.md)ページで確認できます。

## XMLを外部編集

Windowsの場合、[メモ帳++](https://notepad-plus-plus.org)は無料で利用できます。 macOSでは、[Sublime Text](https://www.sublimetext.com/)は代替手段です。 しかし、適切なインデント、セクションの折りたたみ、構文の強調表示を備えたエディターであれば、作業が非常に簡単になります。

エディターでSBSPRJファイルを開くと、UIのタブに対応するセクションを含む、非常に単純な構造化レイアウトが表示されます。 全ての設定がここで文書化されるわけではありません。

![XML編集](project-configuration-files-sbsprj.resources/project-configuration-files-sbsprj-02.png "XML編集")

## 相対パスとエイリアス

エイリアスと組み合わされた相対パスは、プロジェクト構成の中でもより複雑で最も重要な部分の1つです。このセクションではそれらの点を明確にします。 特定のプロジェクトファイルに対してカスタムエイリアスを追加する操作は、[プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)で行います。

ファイルが複数のユーザーのPCでシステム内の他のファイルを参照する場合の大きな問題の1つは、絶対ファイルパスが機能しないことです。 ユーザーは、完全に異なる場所にSVNリポジトリを定義できます。 C:/John/Gamedev/SubstanceLibraryまたはD:/Dev/SubstanceLibrary)。 エイリアスと相対パスの両方が連携してこの問題を解決します。 他のユーザーのファイルを開いて、ローカルにあるユーザーの特定の場所で使用されているカスタムノードを探す場合があります。この場合、同じ方法で定義されている可能性は低くなります。

<b>エイリアス</b>は、パスの一部を置き換えるキーワードです。 これは、%TEMP%のようなWindows環境変数に似ています。この環境変数では、1つの単語で頻繁に使用されるパスが置き換えられ、そのパスが一元的に定義されます。 メリットは、あらゆる場所でパスが簡素化されることです。また、このパスを再配置すると、すべての参照を一度に変更できます。

>[!NOTE]
>
> **エイリアスの例**
> 
> | エイリアス | 実際のパス値 |
> | --- | --- |
> | <b>sbs</b> | *C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages* |
> | <b>カスタム</b> | *D:\Dev\CustomProject\Substance* |
> 
> デフォルトのライブラリはデフォルトで&#x200B;*C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages*&#x200B;にあり、デフォルトのコンテンツを使用するすべてのグラフがこのディレクトリを参照します。 完全なパスを参照する代わりに、&#39;<b>SBS</b>&#39; （引用符なし）のエイリアスが定義されています。 デフォルトのライブラリの場合、SBSパスの正確な値は、インストール時に、ユーザーがDesigner用に選択したディレクトリに設定されます。
> 
> 内部的には、参照にエイリアスを持つパスが含まれている場合、次の方法で参照が変更されます。
> 
> **C:\Program Files\Adobe\Adobe Substance 3D Designer\resources\packages\blur\_hq.sbs => <b>sbs://</b>blur\_hq.sbs**

<b>相対パス</b>は、常に定義されているファイルに対する相対パスです。 つまり、設定ファイルの現在の場所によってパスの大部分が決定され、主にサブフォルダーを追加するだけで、それに基づいてエイリアスパスが決定されます。 <b>したがって、sbsprjファイルは、監視するフォルダーの横に配置することを強くお勧めします。</b>

例えば、*CustomProject.sbsprj*&#x200B;を含む&#x200B;*C:/Versioncontrol/Substance/*&#x200B;にあるリポジトリと、ノードを含む&#x200B;*/Base*&#x200B;および&#x200B;*/Tools,*&#x200B;の2つのフォルダーを考えてみましょう。

BaseとToolsの2つの相対エイリアスを定義するには、SBSPRJファイル内で次のように指定します。

### C:/Versioncontrol/Substance/CustomProject.sbsprj

```
   <urlaliases> 

    <size>2</size> 

    <_2 prefix="_"> 

     <path>file:Base</path> 

     <name>BaseAlias</name> 

    </_2> 

    <_1 prefix="_"> 

     <path>file:Tools</path> 

     <name>ToolsAlias</name> 

    </_1> 

   </urlaliases>
```


この構成ファイルの結果は次のようになります。

**BaseAlias://**&#x200B;は&#x200B;*C:/Versioncontrol/Substance/ベース/*&#x200B;になり、**ToolsAlias://**&#x200B;は&#x200B;*C:/Versioncontrol/Substance/ツール/.*&#x200B;になります。

*C:/Versioncontrol/path/*&#x200B;のみを定義する場合、Substanceは&#x200B;**&quot;file:.&quot;**&#x200B;と表示され、ファイル自体の場所を示すドットが表示されます。
