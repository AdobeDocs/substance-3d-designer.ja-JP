---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/working-with-3d-scenes/exporting-scenes.html"
breadcrumb-title: ''
description: Designerで行ったすべての編集内容を含む3Dシーンを書き出すには、「 3Dシーンを表示」メニューの「シーンを書き出し」アクションを使用します。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Exporting scenes
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シーンの書き出し
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '373'
ht-degree: 1%

---


# シーンの書き出し

Designerで行ったすべての編集を含むシーンを書き出す必要がある場合は、[3Dビュー](../../interface/3d-view/3d-view.md)の「シーン」メニューにある「シーンを書き出し…」アクションを使用します。

USD形式への書き出しの場合、シーンのコンテンツは[Scene browser](../../interface/3d-view/scene-browser/scene-browser.md)に表示されているツリーと一致します。

他の形式の場合、シーンの内容とその内部構造は、選択したファイル形式でサポートされる機能によって異なります。

>[!NOTE]
>
> Designerによってシーンに追加されたすべてのアイテムは、書き出されたシーンに含まれます。デフォルトカメラ、デフォルトエンバイロメント、すべてのマテリアルは、その他のライトをコピーします。

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

「シーン」メニューの「シーンの書き出し…」アクションは、編集された3Dシーンを破壊的に書き出します。シーンは&#x200B;*統合*&#x200B;され、元のシーンへの参照は失われます。

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

「シーンをレイヤーとして書き出し…」アクションは、<b>USD</b>形式(.usd、.usda、.usdc、.usdz)に書き出され、*非破壊的*&#x200B;です。主な書き出しファイルは、*参照の連鎖*&#x200B;を支援し、新しいシーンの編集されたすべての要素は、別々のUSDファイルに保存されます。

つまり、元のシーンの編集は、書き出されたシーンに引き継がれます。

</td>
<td style="border: 0;" valign="top">

![書き出されたシーンファイル – 階層化](../../assets/exportLayered.png "書き出されたシーンファイル – 階層化"){zoomable="yes"}

</td>
</tr>
</table>

書き出されるファイルは、次の構造に従います。

* <b>メインファイル</b>
  * <b>.layers</b>：下のサブレイヤーを参照し、マテリアルのオーバーライドを宣言します。これは、Designerによって作成されたマテリアルのコピーにジオメトリをバインドします。
    * <b>.assembly</b>: .scene#ファイルを参照し、オーバーライドされたマテリアルによって影響を受けたジオメトリのDesignerによって再計算されたデータを取り込むジオメトリを宣言します。
      * <b>.scene#</b>：元のシーンを参照します。
    * <b>.camera</b>: Designerによってシーンに追加されたカメラを宣言します。
    * <b>.light</b>: Designerによってシーンに追加されたライトを宣言します。
    * <b>.material</b>: Designerによってシーンに追加されたマテリアルのコピーを宣言します。このコピーには、書き出されたテクスチャが使用されます。

## テクスチャ

テクスチャは、書き出されたファイルの横のディレクトリに書き出され、その名前に&#39;<b>\_textures</b>&#39;という接尾辞が付けられます。

<b>PNG</b>形式を使用しますが、<b>EXR</b>形式を使用するHDRテクスチャ（浮動小数点）は除きます。
