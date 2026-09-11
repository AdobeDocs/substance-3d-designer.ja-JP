---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: シーンメニューの「シーンを書き出し」アクションを使用して、Designerで行ったすべての編集内容を含む3D シーンを書き出します。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シーンの書き出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# シーンの書き出し

Designerで行ったすべての編集内容を含むシーンを書き出す必要がある場合は、[3D ビュー](../../interface/3d-view/3d-view.md)の「シーン」メニューにある「シーンを書き出し…」アクションを使用します。

USD形式への書き出しの場合、シーンの内容は[シーンブラウザー](../../interface/3d-view/scene-browser/scene-browser.md)に表示されるツリーと一致します。

その他の形式の場合、シーンの内容とその内部構造は、選択したファイル形式でサポートされる機能によって異なります。

>[!NOTE]
>
> Designerによってシーンに追加されたすべてのアイテムは、書き出されるシーンに含まれます。デフォルトディレクトリ、デフォルトカメラ、すべてのマテリアルはその他のライトをコピーします。

![シーン書き出しアクション](../../assets/exportActions.png "シーン書き出しアクション"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## シーンを書き出し

</td>
<td style="border: 0;" valign="top">

### シーンをレイヤーとして書き出し

</td>
<td style="border: 0;" valign="top">

### テクスチャ

</td>
</tr>
</table>

## シーンを書き出し

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

「シーン」メニューの「シーンを書き出し…」操作は、編集された3D シーンを破壊的に書き出します。シーンは&#x200B;*統合*&#x200B;され、元の画像への参照はすべて失われます。

つまり、元のシーンを編集しても、書き出されたシーンには影響しません。

</td>
<td style="border: 0;" valign="top">

![書き出されたシーンファイル – 統合](../../assets/exportFlattened.png "書き出されたシーンファイル – 統合"){zoomable="yes"}

</td>
</tr>
</table>

## シーンをレイヤーとして書き出し

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

「シーンをレイヤーとして書き出し…」操作は、<b>USD</b>形式(.usd、.usda、.usdc、.usdz)に書き出され、*非破壊的*&#x200B;です。主な書き出しファイルは、*一連の参照*&#x200B;を支援し、新しいシーンで編集されたすべての要素は、別々のUSDファイルに保存されます。

つまり、元のシーンに対する編集内容は、書き出されたシーンに引き継がれます。

</td>
<td style="border: 0;" valign="top">

![書き出されたシーンファイル – 階層](../../assets/exportLayered.png "書き出されたシーンファイル – 階層"){zoomable="yes"}

</td>
</tr>
</table>

書き出されるファイルは、次の構造に従います。

* <b>メインファイル</b>
  * <b>.layers</b>：下のサブレイヤーを参照し、マテリアルのオーバーライドを宣言します。これは、Designerによって作成されたマテリアルのコピーにジオメトリをバインドします。
    * <b>.assembly</b>: .シーン#ファイルを参照し、オーバーライドされたジオメトリを宣言します。これにより、オーバーライドされたマテリアルの影響を受けたジオメトリのDesignerによって再計算されたデータが取得されます。
      * <b>.シーン#</b>：元のシーンを参照します。
    * <b>.カメラ</b>: Designerによってシーンに追加されたカメラを宣言します。
    * <b>.light</b>: Designerによってシーンに追加されたライトを宣言します。
    * <b>.マテリアル</b>: Designerによってシーンに追加されたマテリアルのコピーを宣言します。このコピーには、書き出されたテクスチャが使用されます。

## テクスチャ

テクスチャは、エクスポートされたファイルの横のディレクトリにエクスポートされ、そのファイルの名前に&#39;<b>\_テクスチャ</b>&#39;というサフィックスが付けられます。

<b>PNG</b>形式を使用しますが、<b>EXR</b>形式を使用するHDRテクスチャ（浮動小数点）は除きます。
