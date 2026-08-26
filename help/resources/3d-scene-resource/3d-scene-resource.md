---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/resources/3d-scene-resource.html"
breadcrumb-title: ''
description: Substance 3D Designerで3Dシーンリソースを読み込んで使用し、マテリアルのプレビューとテストを行う方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Resources > 3D scene resource
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3D シーンリソース
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 1%

---


# 3D シーンリソース

このページでは、Substance 3D Designerの&#x200B;**3Dシーン**&#x200B;リソースの種類について説明します。サポートされているファイル形式とその使用方法も含まれます。

## 概要

3Dシーンリソースは、様々なワークフローで使用できます。

* [メッシュマップをベイク処理する](../../bakers/bakers.md)
* [3Dビュー](../../interface/3d-view/3d-view.md)で[Substanceグラフ](../../compositing-graphs/substance-compositing-graphs.md)から&#x200B;*テクスチャ*&#x200B;をプレビューします

次の3Dシーンファイル形式がサポートされています。

* [USD](https://graphics.pixar.com/usd/release/index.html) (\*.usd)
* [USDA](https://graphics.pixar.com/usd/release/index.html) (\*.usda)
* [USDZ](https://graphics.pixar.com/usd/release/index.html) (\*.usdz)
* [Autodesk FBX](https://www.autodesk.com/products/fbx/overview) (\*.fbx)
* [Wavefront OBJ](https://www.fileformat.info/format/wavefrontobj/egff.htm) (\*.obj)
* [Autodesk 3D Studioメッシュ](https://knowledge.autodesk.com/support/3ds-max/learn-explore/caas/CloudHelp/cloudhelp/2022/ENU/3DSMax-Data-Exchange/files/GUID-A16ECF7F-70E5-4F9F-8EAD-35F5CFB485A2-htm.html) (\*.3ds)
* [コラダ](https://www.khronos.org/collada/) (\*.dae)
* [Autodesk AutoCAD図面](https://knowledge.autodesk.com/support/autocad/learn-explore/caas/CloudHelp/cloudhelp/2019/ENU/AutoCAD-Core/files/GUID-D4242737-58BB-47A5-9B0E-1E3DE7E7D647-htm.html) (\*.dxf)

## メッシュストレージ

3Dシーンは&#x200B;*のみ*&#x200B;リンクできます。つまり、ディスク上の位置に留まり、アプリケーションで参照されるだけです。

3Dシーンリソースを含むパッケージが[Substance 3D](https://www.adobe.com/jp/products/substance3d/3d-augmented-reality.html)アセット(SBSAR)として公開されると、メッシュは&#x200B;*埋め込まれず*&#x200B;ですが、破棄されます。

## メッシュマップをベイク処理する

3Dシーンをパッケージにリンクすることは、そのシーンのジオメトリから[メッシュマップ](../../bakers/bakers.md)をベイクする唯一の方法です。 開始するには、次の手順を実行します。

* パッケージの&#x200B;*RMB*&#x200B;をクリックし、コンテキストメニューの<b>リンク/3Dメッシュ</b>オプションを選択します
* サポートされている3Dシーンファイルを選択
* <b>[Udimメッシュとしてリンク]</b>ダイアログプロンプトが表示された場合、UVタイルをベイクしない限り、*いいえ*&#x200B;をクリックしてください
* [エクスプローラー](../../interface/the-explorer-window/the-explorer-window.md)にリソースを読み込んだ状態で、*RMB*&#x200B;をクリックし、コンテキストメニューの<b>モデル情報のベイク</b>オプションを選択します
* [モデル情報のベイク](../../bakers/bakers.md)ダイアログが表示され、メッシュマップのベイク処理を設定および実行できます

![メッシュマップのベイク処理](../../assets/bake-model-information.gif "メッシュマップのベイク処理"){width="512px"}

## UDIM/UVタイルの使用

メッシュリソースがリンクされ、アプリケーションが0 ～ 1の範囲外のUVを持つことを検出すると、このメッシュをUDIMメッシュ（UVタイルとも呼ばれる）として処理するかどうかを尋ねられます。 これは後で変更できる設定です。UVタイルを使用していることが確実でない限り、<b>いいえ</b>と答えてください。

UVタイルの動作がアクティブな場合、ベイク処理は異なる動作をし、検出された各UVタイルのテクスチャをベイク処理します。

## リソース/シーンと状態

アプリケーションは、3Dビューに表示される内容を2つの異なるファイルに分割します。 実際の3Dモデルまたはメッシュは、エクスプローラに表示されるリソースです。 ライト、カメラ、およびその他の設定の設定は、「<b>状態</b>」と呼ばれます。 ステートは、外部.sbssscnファイルに保存して、後で再び読み込むことができます。 .sbsscnファイルはリソースではありません。追加の構成ファイルであり、3Dビューの[シーンメニューからのみ読み込むことができます。](../../interface/3d-view/3d-view.md)
