---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/getting-started/activation-and-licenses.html"
breadcrumb-title: ""
description: Substance 3D Designerをアクティベートし、すべての機能にアクセスするためのライセンスを管理する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Getting started > Activation and licenses
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ライセンス認証とライセンス
user-guide-description: ""
user-guide-title: ""
source-git-commit: 21ee545724852c876444dcf3ed4a82af8d1e3715
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%
---

# アプリケーションタイプごとのアクティベーションプロセス

アクティベーションプロセスは、Designerをどこから購入したか、またはどこからアクセスできるかによって異なります。

| エディション | アクティベーションプロセス |
|:-----------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Creative Cloudデスクトップ(CCD) | CCDアプリから製品をインストールし、起動します。 ライセンスに問題がある場合は、次のページに移動してください。[サブスクリプションのエラーが原因で、アプリが起動しない](https://helpx.adobe.com/jp/creative-cloud/apps/troubleshoot/launch-issues/apps-wont-launch-due-to-subscription-error.html) / [アカウント、プラン、請求に関するヘルプ](https://helpx.adobe.com/jp/account/individual.html) |
| スチーム | Steamライブラリから直接製品を起動します。 |
| Substance（スタンドアロン） | 以下のアクティベーションプロセスを参照してください。 |

## ライセンス認証手順（Substance版）

### ライセンス認証ウィザードの使用

Designerを初めて起動すると、アクティベーションウィザードが開き、ライセンス認証プロセスがガイドされます。

次の3つの選択肢があります。

* <b>この製品の評価</b> ：従来の体験版は利用できなくなりました。 代わりに、各Substance 3Dアプリケーションの30日間の無料体験を[ここ](https://www.adobe.com/creativecloud/3d-augmented-reality.html)から、またはCreative Cloudデスクトップから開始できます。 各体験版は他のSubstance 3Dアプリケーションから独立しているため、一度に1つずつ、または一度に試すことができます。
* <b>ライセンスファイルを使ってライセンス認証する</b>: 2022年9月30日より前に[Substance 3D Webサイト](https://store.substance3d.com/user)のアカウントページからダウンロードしたライセンスファイル(<b>\*.key</b>)を使って製品をライセンス認証します。
* <b>アカウントを使用したライセンス認証</b> ：従来のSubstanceアカウントはライセンス認証に使用できなくなりました。

>[!IMPORTANT]
>
> ライセンスファイルをアクティベーションウィザードと共にインストールするには、Designerを管理者として実行し、ウイルス対策を一時的に無効にしてください。

![ライセンス認証ウィザード](activation-and-licenses.resources/activation-wizard.png "ライセンス認証ウィザード")

### 手動アクティベーション

次のフォルダーにlicense.keyファイルを入れて、Designerを手動でアクティベートできます。

<table data-preserve-html="true" style="table-layout:auto">
    <tbody>
        <tr>
            <th style="text-align: left;">Platform</th>
            <th style="text-align: left;">バージョン</th>
            <th colspan="2" style="text-align: left;">パス</th>
        </tr>
        <tr>
            <td rowspan="4" style="text-align: left;"><b>Windows</b></td>
            <td rowspan="2" style="text-align: left;"><b>11.2</b>以上</td>
            <td style="text-align: left;"><code>AppData&#92;Local</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Local&#92;Adobe&#92;Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><code>AppData&#92;Roaming</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Roaming&#92;Adobe&#92;Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>11.1</b>以前</td>
            <td style="text-align: left;"><code>AppData&#92;Local</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Local&#92;Allegorithmic&#92;Substance Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><code>AppData&#92;Roaming</code></td>
            <td style="text-align: left;"><code>C:&#92;Users&#92;&#91;username&#93;&#92;AppData&#92;Roaming&#92;Allegorithmic&#92;Substance Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>macOS</b></td>
            <td style="text-align: left;"><b>11.2</b>以上<br/></td>
            <td colspan="2" style="text-align: left;"><code>/Users/&#91;username&#93;/Library/Application Support/Adobe/Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>11.1</b>以前<br/></td>
            <td colspan="2" style="text-align: left;"><code>/Users/&#91;username&#93;/Library/Application Support/Allegorithmic/Substance Designer</code></td>
        </tr>
        <tr>
            <td rowspan="2" style="text-align: left;"><b>Linux</b></td>
            <td style="text-align: left;"><b>11.2</b>以上</td>
            <td colspan="2" style="text-align: left;"><code>/home/&#91;username&#93;/.local/share/Adobe/Adobe Substance 3D Designer</code></td>
        </tr>
        <tr>
            <td style="text-align: left;"><b>11.1</b>以前<br/></td>
            <td colspan="2" style="text-align: left;"><code>/home/&#91;username&#93;/.local/share/Allegorithmic/Substance Designer</code></td>
        </tr>
    </tbody>
</table>

>[!NOTE]
>
> 上記のパスの一部のディレクトリは、デフォルトで非表示になっている場合があります。 ファイルエクスプローラーにパスを手動で入力するか、隠しファイルを表示して表示します。

>[!IMPORTANT]
>
> ファイル名が`license.key`であることを確認してください。ファイル名がでない場合、アプリケーションでファイルを見つけることができません。

### 環境変数

Designerが`license.key`ファイルをチェックする場所は、[環境変数](../../pipeline-and-project-con/environment-variables/environment-variables.md)で上書きできます。
