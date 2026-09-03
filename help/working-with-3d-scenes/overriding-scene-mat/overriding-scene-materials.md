---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/working-with-3d-scenes/overriding-scene-materials.html"
breadcrumb-title: ''
description: 3Dシーンの既存のマテリアルをオーバーライドして、テストやプレビュー用に独自のSubstanceマテリアルに置き換えます。
helpx_creative_field: ""
helpx_description: Designer > Working with 3D scenes > Overriding scene materials
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シーンマテリアルをオーバーライドする
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '898'
ht-degree: 0%

---


# シーンマテリアルをオーバーライドする

既存のマテリアルで3Dシーンを操作する場合、これらのマテリアルをオーバーライドして独自のマテリアルに置き換える必要があります。

マテリアルはゼロから作成することも、[Substanceグラフに抽出](../../working-with-3d-scenes/extracting-materials-val/extracting-materials-values-and-textures.md)されたシーンのマテリアルの調整バージョンを作成することもできます。

![シーンマテリアルをオーバーライドし、微調整してシーン状態にリセットします](overriding-scene-materials.resources/overriding-scene-materials-01.gif "シーンマテリアルをオーバーライドし、微調整してシーン状態にリセットします"){zoomable="yes"}

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

## シーンのマテリアルをオーバーライド

</td>
<td style="border: 0;" valign="top">

### シーンの状態にリセット

</td>
<td style="border: 0;" valign="top">

### 接続されたマテリアル

</td>
</tr>
</table>

## シーンのマテリアルをオーバーライド

シーンで使用されているマテリアルは、新しいマテリアルまたは既存のマテリアルの編集されたバージョンである独自のバージョンでオーバーライドできます。

「材料をオーバーライド」アクションは、次の2つの場所にあります。

* マテリアルメニューを開き、目的のマテリアルのサブメニューに移動します
* シーンオブジェクトでShift+LMBを押して選択し、RMBをクリックしてコンテキストメニューを開きます

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![&#39;3Dビュー&#39;ビューポートのマテリアルを上書き – アクション](overriding-scene-materials.resources/overriding-scene-materials-02.png "&#39;3Dビュー&#39;ビューポートのマテリアルを上書き – アクション"){zoomable="yes"}

*3Dビュービューポートのアクション*

</td>
<td style="border: 0;" valign="top">

![[マテリアルのオーバーライド] - [マテリアル]メニューのアクション](overriding-scene-materials.resources/overriding-scene-materials-03.png "[マテリアルのオーバーライド] - [マテリアル]メニューのアクション"){zoomable="yes"}

*マテリアルメニューのアクション*

</td>
</tr>
</table>

Designerのコンテキストでは、シーンの内部の記述に米ドルを使用しています。オーバーライドとは、可能な限りオリジナルと一致するマテリアルのコピーを&#x200B;*作成*&#x200B;し、シーンのメッシュの&#x200B;*マテリアルバインディング*&#x200B;をオリジナルからコピーに変えることを意味します。

>[!NOTE]
>
> コピーはシーン内のルートの下の&#39;<b>material</b>&#39;フォルダー（USDの&#39;Scope&#39;）に作成され、元のIDと同じIDに数値のサフィックス（例： &#39;rustedMetal\_0&#39;）を使用します

これは、次の2つの重要な点を意味します。

1. 元の素材は一切変更されません。
1. Designerで行った作業はすべてコピーに適用されます。

元のシーンのマテリアルを復元する場合や、必要に応じて簡単な編集前後のチェックを行う場合は、同じ「マテリアルのオーバーライド」アクションを使用して、オーバーライドのオン/オフをいつでも切り替えることができます

コピーがオリジナルと一致するように作成されることを考えると、ほとんどの場合、マテリアルをオーバーライドしても、Substanceグラフをコピーに接続するかプロパティを変更するまで、外観は変化しません（次の注を参照）。

>[!NOTE]
>
> オーバーライドが適用されると、Designerは影響を受けるメッシュの接線と従法線を計算します。特にこれらのメッシュに法線のスケールとバイアスが定義されていないか、別のメッシュを使用している場合、時間がかかり、メッシュのアスペクトが変わることがあります。

>[!IMPORTANT]
>
> <b>AdobeStandardMaterial</b>のシェーディングモデルはSubstance 3Dエコシステム全体でサポートされていますが、業界標準ではないため、Blenderなどのサードパーティ製アプリケーションでは&#x200B;*サポートされない場合があります*。
> 
> Substance 3Dアプリケーションの外部で最高の相互運用性を実現するために、現在は、サポートするマテリアルプロパティおよび効果がはるかに少ない場合でも、<b>UsdPreviewSurface</b> シェーディングモデルの使用をお勧めします。

## シーンの状態にリセット

オーバーライドされた状態を維持したままマテリアルの初期状態に戻す必要がある場合、マテリアルのコピーはすべて初期値にリセットできます。

マテリアルプロパティ値が修正された場合、またはグラフからテクスチャが適用された場合、プロパティは初期値またはテクスチャに戻ります。

マテリアルは、完全に、またはプロパティごとにリセットできます。

マテリアルのサブメニューまたはメッシュのコンテキストメニューの「マテリアルをシーンの状態にリセット」アクションを使用して、マテリアルを完全にリセットします。

アクションは、次の3つの場所で見つけることができます。

* マテリアルメニューを開き、目的のマテリアルのサブメニューに移動します
* シーンオブジェクトでShift+LMBを押して選択し、RMBをクリックしてコンテキストメニューを開きます
* そのマテリアルのプロパティの上部にあるハンバーガーメニュー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![マテリアルをシーンの状態にリセット – &#39;3D VIew&#39;ビューポートでの動作](overriding-scene-materials.resources/overriding-scene-materials-04.png "マテリアルをシーンの状態にリセット – &#39;3D VIew&#39;ビューポートでの動作"){zoomable="yes"}

*3Dビュービューポートのアクション*

</td>
<td style="border: 0;" valign="top">

![マテリアルをシーンの状態にリセット – 「マテリアル」メニューのアクション](overriding-scene-materials.resources/overriding-scene-materials-05.png "マテリアルをシーンの状態にリセット – 「マテリアル」メニューのアクション"){zoomable="yes"}

*マテリアルメニューのアクション*

</td>
<td style="border: 0;" valign="top">

![マテリアルをシーンの状態にリセット – 「プロパティ」ドックのアクション](overriding-scene-materials.resources/overriding-scene-materials-06.png "マテリアルをシーンの状態にリセット – 「プロパティ」ドックのアクション"){zoomable="yes"}

*マテリアルのプロパティのアクション*

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

このアクションは、マテリアルの一部の側面のみをリセットする場合に備えて、マテリアルプロパティの&#x200B;*プロパティごと*&#x200B;にも使用できます。

マテリアルプロパティのハンバーガーメニューを開き、「デフォルトのシーン状態にリセット」アクションを見つけます。

</td>
<td style="border: 0;" valign="top">

![シーンの状態にリセット – マテリアルプロパティのアクション](overriding-scene-materials.resources/overriding-scene-materials-07.png "シーンの状態にリセット – マテリアルプロパティのアクション"){zoomable="yes"}

</td>
</tr>
</table>

## 接続されたマテリアル

繰り返しますが、Designerはシーンのマテリアルを直接変更するのではなく、シーン内にコピーを作成し、メッシュをそのコピーにバインドします（元のコピーはバインドされません）。

また、Designerの「マテリアル」メニューには、デフォルトでシーンのマテリアルリストと一致する&#x200B;*独自の*&#x200B;個別のマテリアルリストがあります。 このリストには、いつでも新しいマテリアルを追加できます。

これは、Designerのみで作成および管理される&#x200B;*別*&#x200B;データセットです。 これらのマテリアルは、シーンの元のマテリアルをオーバーライドするコピーに&#x200B;*接続*&#x200B;されます。

![マテリアルのオーバーライド – データ回路図](overriding-scene-materials.resources/overriding-scene-materials-08.png "マテリアルのオーバーライド – データ回路図"){zoomable="yes"}

シーンブラウザーでDesignerによって作成されたコピーに、「マテリアル」メニューに表示されているいずれかのマテリアルを接続できます。シーンーでコピーに対して「RMB」をクリックし、「接続マテリアル」サブメニューを開きます。

サブメニューには、シーン内のすべてのマテリアルと、「マテリアル」メニューから手動で作成したマテリアルが一覧表示されます。

![マテリアルを接続する](overriding-scene-materials.resources/overriding-scene-materials-09.gif "マテリアルを接続する"){zoomable="yes"}
