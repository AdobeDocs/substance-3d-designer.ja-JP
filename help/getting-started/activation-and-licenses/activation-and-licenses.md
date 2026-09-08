---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ''
description: Substance 3D Designerをアクティベートし、すべての機能にアクセスするためのライセンスを管理する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライセンス認証とライセンス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '416'
ht-degree: 1%

---


# アプリケーションタイプごとのアクティベーションプロセス

アクティベーションプロセスは、Designerをどこから購入したか、またはどこからアクセスできるかによって異なります。

| エディション | アクティベーションプロセス |
| --- | --- |
| Creative Cloud デスクトップ | [HelpXドキュメント](https://helpx.adobe.com/support/substance-3d-designer.html)の専用ページを参照してください。 問題が発生した場合、[Creative Cloudのドキュメント](https://helpx.adobe.com/creative-cloud/user-guide.html)に詳細な回答が記載されている場合があります。 |
| スチーム | Steamライブラリから直接製品を起動します。 |
| Substance（スタンドアロン） | 以下のアクティベーションプロセスを参照してください。 |

## ライセンス認証手順（Substance版）

### ライセンス認証ウィザードの使用

次の3つの選択肢があります。

* <b>この製品の評価</b> ：従来の体験版は利用できなくなりました。 代わりに、各Substance 3Dアプリケーションの30日間の無料体験を[ここ](https://www.adobe.com/creativecloud/3d-augmented-reality.html)から、またはCreative Cloudデスクトップから開始できます。 各体験版は他のSubstance 3Dアプリケーションから独立しているため、一度に1つずつ、または一度に試すことができます。
* <b>ライセンスファイルを使ってライセンス認証する</b>: 2022年9月30日より前に[Substance 3D Webサイト](https://store.substance3d.com/user)のアカウントページからダウンロードしたライセンスファイル(<b>\*.key</b>)を使って製品をライセンス認証します。
* <b>アカウントを使用したライセンス認証</b> ：従来のSubstanceアカウントはライセンス認証に使用できなくなりました。

>[!IMPORTANT]
>
> ライセンスファイルをアクティベーションウィザードと共にインストールするには、Designerを管理者として実行し、ウイルス対策を一時的に無効にしてください。

![ライセンス認証ウィザード](../../assets/activation-wizard.png "ライセンス認証ウィザード")

### 手動アクティベーション

次のフォルダーにlicense.keyファイルを入れて、Designerを手動でアクティベートできます。

<table data-preserve-html="true">
<colgroup> <col/> <col/> <col/> <col/> </colgroup><tbody><tr><th style="text-align: left;">Platform</th>
<th style="text-align: left;">バージョン</th>
<th colspan="2" style="text-align: left;">パス</th>
</tr><tr><td rowspan="4" style="text-align: left;"><b>Windows</b></td>
<td rowspan="2" style="text-align: left;"><b>11.2</b>以上</td>
<td style="text-align: left;">AppData/ローカル</td>
<td style="text-align: left;">C:\Users\[ユーザー名]\AppData\Local\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;">AppData/ローミング</td>
<td style="text-align: left;">C:\Users\[ユーザー名]\AppData\Roaming\Adobe\Adobe Substance 3D Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>11.1</b>以前</td>
<td style="text-align: left;">AppData/ローカル</td>
<td style="text-align: left;">C:\Users\[ユーザー名]\AppData\Local\Allegorithmic\Substance Designer</td>
</tr><tr><td style="text-align: left;">AppData/ローミング</td>
<td style="text-align: left;">C:\Users\[ユーザー名]\AppData\Roaming\Allegorithmic\Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Mac</b></td>
<td style="text-align: left;"><b>11.2</b>以上<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[ユーザー名]/Library/Application Support/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b>以前<br/>
</td>
<td colspan="2" style="text-align: left;">/Users/[ユーザー名]/Library/Application Support/Allegorithmic/Substance Designer</td>
</tr><tr><td rowspan="2" style="text-align: left;"><b>Linux</b></td>
<td style="text-align: left;"><b>11.2</b>以上</td>
<td colspan="2" style="text-align: left;">/home/[ユーザー名]/.local/share/Adobe/Adobe Substance 3D Designer</td>
</tr><tr><td style="text-align: left;"><b>11.1</b>以前<br/>
</td>
<td colspan="2" style="text-align: left;">/home/[ユーザー名]/.local/share/Allegorithmic/Substance Designer</td>
</tr></tbody></table>

>[!NOTE]
>
> 上記のパスの一部のディレクトリは、デフォルトで非表示になっている場合があります。 ファイルエクスプローラーでパスを手動で入力するか、隠しファイルを表示して表示します。

>[!IMPORTANT]
>
> ファイルの名前が&#x200B;**license.key**&#x200B;であることを確認してください。名前が指定されていない場合、アプリケーションはファイルを見つけることができません。

### 環境変数

Designerが<b>license.key</b>ファイルをチェックする場所は、[環境変数](../../pipeline-and-project-con/environment-variables/environment-variables.md)で上書きできます。
