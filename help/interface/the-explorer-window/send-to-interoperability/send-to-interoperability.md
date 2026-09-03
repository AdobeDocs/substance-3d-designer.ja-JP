---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/interface/the-explorer-window/send-to-interoperability.html"
breadcrumb-title: ''
description: Substance 3D Designerの「相互運用に送信」機能を使用して、マテリアルを他のアプリケーションに書き出します。
helpx_creative_field: ""
helpx_description: Designer > Interface > The Explorer window > Send to...  Interoperability
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 送信先...  互換性
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 1%

---


# 送信先...  互換性

![DesignerからSubstance 3Dアプリケーションに送信](send-to-interoperability.resources/send-to-interoperability-01.png "DesignerからSubstance 3Dアプリケーションに送信"){width="512px"}

Adobe Substance 3D Designerは、[Substance 3D Sampler](https://www.adobe.com/jp/products/substance3d-sampler.html)、[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)および[Substance 3D Stager](https://www.adobe.com/jp/products/substance3d-stager.html)と相互運用できます。 これにより、*送信*&#x200B;と&#x200B;*再送信*&#x200B;を行ってすばやく作業し、Substance 3Dエコシステム全体で容易に繰り返すことができます。

通常、ワークフローは次のようになります。

1. [Substanceグラフのプロパティ](../../../compositing-graphs/graph-parameters/graph-parameters.md)に<b>Type</b>属性を設定します
1. [エクスプローラー](../the-explorer-window.md)パネルで、送信するパッケージを選択します
1. エクスプローラーの<b>Publish/送信</b>ドロップダウンで、対象のアプリケーションを選択します
1. グラフに変更を加える
1. 手順3を繰り返してパッケージを再送信し、既存の送信済みアセットに変更を適用します

>[!WARNING]
>
> 相互運用性機能は、<b>Steam</b>バージョンでは&#x200B;*利用できません*。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## グラフタイプの設定

Substanceグラフには多くの機能があります。 グラフの正確な機能を事前に定義して、正しく送信できるようにしておく必要があります。

[Substanceグラフのプロパティ](../../../compositing-graphs/graph-parameters/graph-parameters.md)の<b>属性</b>セクションには、<b>種類</b>のオプションがあり、次のオプションを含むドロップダウンがあります。

</td>
<td style="border: 0;" valign="top">

![Substanceグラフの種類の属性](send-to-interoperability.resources/send-to-interoperability-02.jpg "Substanceグラフの種類の属性")

</td>
</tr>
</table>

* **未指定**&#x200B;は、設定していない場合の既定の型です。 送信先のアプリケーションによっては、異なる解釈が行われる場合があります。 [Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)は、例えばデフォルトでマテリアルに設定されます。
* **標準マテリアル**&#x200B;は、マルチチャンネルPBRマテリアル用で、適切に[出力](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)とラベル付けされています。
* **デカールマテリアル**&#x200B;は、アルファチャンネルを含むマルチチャンネルのPBRマテリアルで、[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)または[Substance 3D Sampler](https://www.adobe.com/jp/products/substance3d-sampler.html)でデカールとして適用されます。
* **アトラスマテリアル**&#x200B;は、複数のアトラス画像で構成されるマルチチャンネルPBRマテリアル用で、Designerまたは[Substance 3D Sampler](https://www.adobe.com/jp/products/substance3d-sampler.html)の[Atlas Scatterノード](../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/atlas-scatter/atlas-scatter.md)で使用します。
* **Filter**&#x200B;は、両方とも[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)または[Substance 3D Sampler](https://www.adobe.com/jp/products/substance3d-sampler.html)で使用される、汎用フィルター用です。
* **メッシュベースのジェネレーター**&#x200B;は、複数入力のマスクジェネレーター用です。 これは[Substance 3D Painter](https://www.adobe.com/jp/products/substance3d-painter.html)のみが使用しています。
* **テクスチャジェネレーター**&#x200B;は、2Dプロシージャやノイズなどの単一チャンネルマップ用です。
* **環境光**&#x200B;は、単一チャンネルの照明環境用で、シーンやオブジェクトに光を当てるために使用します。
* **ライトテクスチャ**&#x200B;は、物理的なライトに適用される単一チャンネルテクスチャ用です。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## 「送信先」メニュー

送信処理では、背後からSubstance 3Dアセットファイル(SBSAR)に[公開](../../../compositing-graphs/publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)個の1つ以上のパッケージが必要でした。

コンテンツの送信は、次の方法で実行できます。

* パッケージを右クリックして、コンテキストメニューの<b>送信先…</b>サブメニューを開き、ターゲットアプリケーションの<b>送信先…</b>オプションを選択します。
* エクスプローラーパネルの上部にある「![](send-to-interoperability.resources/send-to-interoperability-03.jpg) <b>Publish/送信</b>」ボタンをクリックし、ターゲットアプリケーションの「<b>送信先…</b>」オプションを選択します。

</td>
<td style="border: 0;" valign="top">

![エクスプローラーの[Publish]/[送信]メニュー](send-to-interoperability.resources/send-to-interoperability-04.jpg "エクスプローラーの[Publish]/[送信]メニュー")

</td>
</tr>
</table>

### 再送信

*既に*&#x200B;回送信されたパッケージを&#x200B;*同じターゲット*&#x200B;アプリケーションに再度送信すると、ターゲットアプリケーションのアセットが新しいバージョンで&#x200B;*更新*&#x200B;されます。

## Player に送信

[Substance Player](https://helpx.adobe.com/substance-3d-player/home.html)は、*両方* <b>Substance 3Dファイル</b> (SBS)と<b>Substance 3Dアセット</b> (SBSAR)をサポートしています。

Playerに送信するには、Substance Playerの実行可能ファイルがユーザーによって&#x200B;*手動で配置*&#x200B;されている必要があります。次の手順が実行されます：

* Designerのインストール後にPlayerが&#x200B;*見つからない*&#x200B;かどうかを確認するメッセージが表示されたら、
* <b>[ツール]</b>メニューで、<b>[Substance Player] > [検索…]</b>オプションを使用すると、いつでも検索できます。

PlayerでDesignerからファイルを受け取るには、ユーザーがSubstance 3D Designer *のインストールディレクトリ*&#x200B;を手動で指定する必要があります。次の手順を実行できます：

* Playerのインストール後にDesignerが&#x200B;*見つからなかった*&#x200B;かどうかを確認するメッセージが表示されたら、
* <b>[オプション]</b>メニューで、<b>[Adobe Substance 3D Designerの検索]</b>オプションを使用していつでも検索できます。

>[!NOTE]
>
> Substance 3Dファイル(SBS)をPlayerに送信すると、Substance 3Dアセット(SBSAR)が&#x200B;*一時ファイル*&#x200B;として発行されます。

## 問題

パッケージを送信すると、次のようなエラーが発生する場合があります。

```
Error sending package to Substance 3D Painter. Check the console for details. SBSAR export failed.
```


これは通常、標準のエラーと警告が原因です。問題を解決するには、これらを修正してください。

* グラフに[出力](../../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードが定義されていません。 出力ノードを追加し、それらに接続します。
* [関数グラフ](../../../function-graphs/function-graphs.md)の[Get nodes](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/get-nodes/get-nodes.md)の変数が見つからないか、壊れています。 影響を受けるノードの&#x200B;*黄色の警告バッジ*&#x200B;で追跡します。
