---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/pipeline-and-project-configuration/configuration-list-sbscfg.html"
breadcrumb-title: ''
description: Substance 3D DesignerでSBSCFG構成リストを使用して、プロジェクト設定とプリセットを管理する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Configuration List - SBSCFG
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 構成リスト – SBSCFG
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 0%

---


# 構成リスト – SBSCFG

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

構成ファイルには、プロジェクトの一覧とエンジン互換性モードのみが含まれているため、[プロジェクト構成ファイル](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)よりも簡単です。 これらは、単一のプロジェクトファイルよりも上位レベルのプロジェクト/環境構成リストとして機能します。

異なる環境に対して複数の構成を持つことができ、これらのファイルはSBSPRJファイルと一緒にバージョン管理の下に保つことができます。

</td>
<td width="25.00%" style="border: 0;" valign="top">

![SBSCFGファイルアイコン](../../assets/sbscfg.png "SBSCFGファイルアイコン")

</td>
</tr>
</table>

## 構成ファイルの変更

これらのファイルはシンプルですが、SBSPRJファイルと同様に、2つの異なる方法で変更することができます。

### プロジェクト設定

ハイライト表示されたセクションは、コンフィギュレーションファイルに関連する部分です。上記で定義したSBSCFGファイルに保存されているプロジェクトをリストに追加するだけです。

![プロジェクト設定](../../assets/config-ui.png "プロジェクト設定")

### XMLとしての外部編集

Windowsの場合は<b>メモ帳++</b>が最適な無料オプションです。macOSの場合は<b>Sublime Text</b>が代わりに使用できます。 しかし、適切なインデント、セクションの折りたたみ、構文の強調表示を備えたエディターであれば、作業が非常に簡単になります。

エディタでSBSCFGファイルを開くと、UIに対応するセクションを含む、非常に単純な構造化レイアウトが表示されます。

```
<?xml version="1.0" encoding="UTF-8"?> 

<root> 

 <projects> 

  <projectfiles> 

   <size>1</size> 

   <_1 prefix="_"> 

    <path>custom_project.sbsprj</path> 

   </_1> 

  </projectfiles> 

 </projects> 

 <preferences> 

  <configuration> 

   <compatibilitymode>sbs_engine_v6</compatibilitymode> 

  </configuration> 

 </preferences> 

</root>
```


デフォルトのプロジェクトとユーザープロジェクトは明示的にリストされず、追加のプロジェクトはこれらの後に定義されることに注意してください。

上記の例では、[相対パス](../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)も使用しています。 相対パスのロジックは、CFGファイルとPRJファイルでは少し異なることに注意してください。CFGファイルの場合は、上記のように、**パス**&#x200B;の前に「file:/」と入力しないでください。 代わりに、パスは定義されたCFGファイルの場所に追加されます。

## デフォルトのライブラリの削除

現時点では、デフォルトのライブラリを削除することはできません。 Designerの多くの機能が失われてしまうので、どうせそうするのはお勧めできません。
