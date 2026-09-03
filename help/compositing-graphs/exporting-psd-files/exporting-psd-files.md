---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/exporting-psd-files.html"
breadcrumb-title: ''
description: Substance合成グラフをPSDファイルとして書き出し、Adobe Photoshopやその他の画像編集ワークフローで使用する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Exporting PSD files
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: PSD ファイルの書き出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '471'
ht-degree: 1%

---


# PSD ファイルの書き出し

Substance 3D Designerでは、テクスチャをAdobe PhotoshopドキュメントまたはPSDファイルに書き出すことができます。このページでは、グラフのノードをレイヤーに変換するために使用する特別なインタフェースについて説明します。**このプロセスは自動的に行われるものではありません。多数のコントロールできますが、制限があり、ノードとレイヤー間の正確な一致を取得できない場合がよくあります。** また、明示的に設定しない限り、グラフと同じ出力がPSDに含まれる保証はありません。 一般に、正確性と正確性が高ければ高いほど、ユーザーはより多くの労力を必要とします。 一般に、非破壊的な方法で密接に複製できるのは、[ブレンドノード](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/blend/blend.md)のみです。 調整レイヤーはサポートされていません。また、レイヤースタイルや、レイヤー描画モード以外のスタイルもサポートされていません。

[Substance 3D Designerでは、ビットマップファイルに書き出すこともできます。](../../compositing-graphs/exporting-bitmaps/exporting-bitmaps.md)

## PSD書き出しダイアログ

PSD書き出しダイアログは、1つの方法でのみ開くことができます。 PSDに書き出すグラフの[グラフビュー](../../interface/the-graph-view/the-graph-view.md)で、![](exporting-psd-files.resources/exporting-psd-files-01.png) <b>ツール</b>ボタンをクリックし、<b>PSDエクスポーター</b>を選択します。 <b>グラフビュー</b>内にインターフェイスが表示されます。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![PSDエクスポータのユーザーインターフェイス](exporting-psd-files.resources/exporting-psd-files-02.png "PSDエクスポータのユーザーインターフェイス")

</td>
<td style="border: 0;" valign="top">

1. <b>ファイル名と場所：</b>ここにエクスポートするフォルダーとファイル名を設定します。 「書き出し」ボタンを押して、書き出し処理を実行します。
1. <b>グループの追加：</b>レイヤーグループを追加します
1. <b>[レイヤーの追加]ドロップダウン：</b>レイヤーを追加するには、2つの方法のいずれかを選択します。 *マウスの右ボタンでノードをドラッグ*&#x200B;して、スタックにレイヤーを追加することもできます。
1. <b>[レイヤーの削除]ドロップダウン：</b>選択したレイヤーまたはすべてのレイヤーを削除します。
1. <b>レイヤーのスタック：</b>ここで実行した場合、ほとんどのセットアップ作業が行われます。 インターフェイスは、Photoshopの限られたオプションをミラーリングします。 レイヤー名、描画モード、不透明度を設定します。 レイヤーに2つのサムネールがある場合、2番目のサムネールはAlphaチャンネルを表します。

</td>
</tr>
</table>

## ワークフロー

Photoshopはマルチ出力マテリアルを直接サポートしていないため、PSDを設定する方法は複数あります。 以下に、最も一般的な方法の概要を示します。

* すべての出力に対して複数のフォルダーを設定します。 ベースカラー用のフォルダー、標準フォルダー、粗さなど
* 右マウスボタンで出力をドラッグし、適切なグループにドロップします。 単純なものにしておきたいなら、PSDはこれだけにしておいてもいいでしょう。
* PSDをさらに広げるには：グラフの左に戻り、該当するグラフのステップの間の該当するグループにドロップします。 出力/グループ間でレイヤーを共有することはできません。

まれに、出力がより重要なPSDになる場合があります。このような場合は、ブレンドモードのみを使用してグラフを作成することができます。 この場合、より編集可能なバージョンのグラフをレイヤー化された文書として再作成することが可能です。
