---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/preferences-window/version-control.html"
breadcrumb-title: ''
description: Gitやその他のシステムと統合するには、Substance 3D Designer環境設定でバージョン管理を設定します。
helpx_creative_field: ""
helpx_description: Designer > Interface > Preferences window > Version control
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: バージョン管理
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '873'
ht-degree: 0%

---


# バージョン管理

>[!IMPORTANT]
>
> Substance 3D Designerバージョン<b>14.0.0</b>は、Perforceサポートを<b>Python 3</b>にアップグレードします。
> 
> 必要に応じて、他のスクリプトやバージョン管理環境を調整してください。

Designerでは、[Perforce](https://www.perforce.com/) (P4)バージョン管理システムをPythonで統合できます。

この統合により、[エクスプローラー](../../../interface/the-explorer-window/the-explorer-window.md)のパッケージのコンテキストメニューにカスタムの&#39;バージョン管理&#39;サブメニューが追加され、P4のパッケージのステータスに一致するカスタムアイコンが追加されます。

## P4を準備中

[P4V](https://www.perforce.com/products/helix-core-apps/helix-visual-client-p4v)で、以下のようにワークスペース名とパスをメモします。

![P4Vワークスペース情報](../../../assets/p4v-workspace-strings.jpg "P4Vワークスペース情報"){zoomable="yes"}

任意のテキストエディターまたはIDEで、Designerのインストールにある次のスクリプトを開きます： &#39;*tools/version\_control/perforce.py*&#39;。

19行目で、システム上の<b>&#39;p4&#39;実行可能ファイル</b>の場所へのパスを編集します。\
次の例では、このパスは&#39;*c:/Program Files/Perforce/p4.exe*&#39;です。

```
## Editable variables

cPerforceP4AbsPath = os.path.abspath("c:/Program Files/Perforce/p4.exe")

cVerbose = False
```


## Designerでの設定

バージョン管理は、Designerの[環境設定](../../../interface/preferences-window/preferences-window.md)で利用可能な[プロジェクト設定](../../../interface/preferences-window/project-settings/project-settings.md)で構成されています。

![&#39;プロジェクト設定の[バージョン管理]タブ](../../../assets/p4v-project-settings.jpg "&#39;プロジェクト設定の[バージョン管理]タブ"){zoomable="yes"}

1. 編集/環境設定に移動
1. 「プロジェクト」に移動し、ターゲット[プロジェクトファイル](../../../pipeline-and-project-con/project-configuration-fil/project-configuration-files-sbsprj.md)を選択して、「バージョン管理」タブに移動します
1. 「バージョン管理が有効」をオンにします。
1. 「ワークスペース」セクションに次の情報を入力します。

   * <b>名前：</b> P4Vから以前に取得した&#39;ワークスペース名&#39;を入力してください
   * <b>パス：</b> P4Vから以前に取得した&#39;ワークスペースパス&#39;を入力してください

Designerでの![P4の設定：ワークスペース](../../../assets/p4v-project-settings-workspace.jpg "DesignerでのP4の設定：ワークスペース"){zoomable="yes"}

### アクションの設定

これらのアクションは、エクスプローラー内のパッケージのコンテキストメニューで使用できます。 ほとんどのバージョン管理ツールのコンセプトに一致する事前定義されたアクションがあります。

* 必要に応じて、すべてのアクションラベルを変更できます。
* すべてのアクションを有効にするには、スクリプトが必要です。

次のものを使用できます。

* *アクションにつき*&#x200B;スクリプト1つ
* *すべての*&#x200B;アクションに対する1つのスクリプト

すべてのアクションのスタータースクリプトは、Designerのインストール&#39;*tools/version\_control/perforce.py*&#39;で利用できます。

>[!IMPORTANT]
>
> 利用できるようにするには、パッケージを&#39;ワークスペースパス&#39;の下（&#39;*f:/Dev/perforce*&#39;の下）に保存する必要があります

1. <b>アクション</b>グループで、<b>追加</b>アクションの[...]ボタンをクリックします
1. Designerのインストールで、次のスクリプトを選択します： &#39;*tools/version\_control/perforce.py*&#39;
1. スクリプトは、他のすべてのアクション用に自動的に設定されます。

Designerでの![P4の設定： actions](../../../assets/p4v-project-settings-actions.jpg "DesignerでのP4の設定： actions"){zoomable="yes"}

### カスタムアクションの設定

すべてのバージョン管理ツールは異なり、多くの機能が含まれているため、カスタムアクションを追加できます。

1. 「項目を追加」をクリック
1. 新しいアクションのラベルを入力し、スクリプトパスを設定します

### スクリプトインタプリタの設定

1. 「Interpreters」セクションで、「Add item」をクリックします。
1. スクリプトファイルの拡張子または接尾辞と、インタプリタの実行可能ファイルへのパスを設定します
1. perforce.pyスクリプトを編集して、「p4」バイナリの場所を更新します

Designerでの![P4の設定：インタープリター](../../../assets/p4v-project-settings-interpreters.jpg "DesignerでのP4の設定：インタープリター"){zoomable="yes"}

## バージョン管理の使用方法

1. 新しいパッケージを作成
1. 「ワークスペースのパス」ディレクトリにパッケージを保存します。
1. パッケージで「RMB」をクリックします。「バージョン管理」サブメニューにアクセスできるようになりました。
1. ワークスペースのパッケージファイルのステータスに応じて、いくつかのアクションを使用できます。

   * <b>追加：</b>ファイルを&#39;追加&#39;としてマークします
   * <b>送信：</b>選択したパッケージを送信します。 このアクションにより、変更メッセージを指定するためのダイアログが表示されます（以下を参照）
   * <b>元に戻す：</b>変更を元に戻します。 このアクションにより、元に戻すファイルを選択するためのダイアログが表示されます（以下を参照）
   * <b>チェックアウト：</b>デポからファイルをチェックアウトします
   * <b>最新バージョンの取得：</b>デポから最新バージョンを取得します
   * <b>状態の更新：</b>パッケージファイルの状態を更新します

   <table>
   <tr style="border: 0;">
   <td style="border: 0;" valign="top">

   ![&#39;送信&#39;ダイアログ](../../../assets/p4v-submit.jpg "&#39;送信&#39;ダイアログ"){zoomable="yes"}

   </td>
   <td style="border: 0;" valign="top">

   ![&#39;元に戻す&#39;ダイアログ](../../../assets/p4v-revert.jpg "&#39;元に戻す&#39;ダイアログ"){zoomable="yes"}

   </td>
   </tr>
   </table>

>[!NOTE]
>
> すべてのアクションで複数選択がサポートされています
> 
> P4およびその他のバージョン管理ツールで、読み取り専用のファイル権限を使用して変更を制限する場合は、変更を行う前にパッケージをチェックアウトする必要があります。
> 
> 読み取り専用のパッケージファイルはSDで変更できません。

パッケージには、ステータスに応じて次のアイコンが表示されます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![パッケージアイコン：最新](../../../assets/p4-up-to-date.png "パッケージアイコン：最新")

最新

</td>
<td style="border: 0;" valign="top">

![パッケージアイコン：チェックアウト済み](../../../assets/p4-checked-out.png "パッケージアイコン：チェックアウト済み")

チェックアウトしました

</td>
<td style="border: 0;" valign="top">

![パッケージアイコン：追加](../../../assets/p4-added.png "パッケージアイコン：追加")

追加用にマーク

</td>
<td style="border: 0;" valign="top">

![パッケージアイコン：デポにありません](../../../assets/p4-not-in-depot.png "パッケージアイコン：デポにありません")

車庫にない

</td>
</tr>
</table>

最新でないパッケージには、警告記号が付いています。

## アクションスクリプト

各アクションで実行されるコマンドは、以下のように構築されます。

my\_script <b>*ワークスペース名WorkspacePath ActionName[アクション引数]*</b>

<b>ワークスペース名：</b>ワークスペースの名前

<b>WorkspacePath:</b>ワークスペースのルートディレクトリのパス

<b>アクション名：</b>アクションの名前：

* 「追加」アクションの&#x200B;*追加：*
* 「チェックアウト」アクションの&#x200B;*チェックアウト：*
* 「送信」アクションの&#x200B;*送信：*
* 「元に戻す」操作の&#x200B;*復帰：*
* [最新バージョンの取得]アクションの&#x200B;*get\_last\_version:*
* 「ステータスを取得」アクションの&#x200B;*get\_status:*

ラベルは、プロジェクト設定で「 」文字を「\_」に置き換えて設定します – 例： &quot;My Action&quot; => &quot;My\_Action&quot;

アクションの<b>ActionArgs:</b>引数：

* *-desc*: &#39;送信&#39;操作で使用される説明文字列
* *-files:*&#x200B;ファイルの一覧
* *-files\_list:*&#x200B;行ごとのファイルのリストを含むテキストファイル

<b>get\_status</b>：指定したファイルの状態に応じて値を返します：

* 0：未定義のステータス
* 1：保管庫に保管されていません
* 2：以前のバージョン（最新ではありません）
* 3：最新バージョン（最新）
* 4:チェックアウト済み
* 5：追加用にマーク済み
* その他のアクション：
  * 0：成功
  * その他：エラー
