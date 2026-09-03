---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/bakers/bakers-legacy-interface.html"
breadcrumb-title: ''
description: 以前のバージョンに慣れているユーザー向けに、Substance 3D Designer ベイカーの従来のインターフェイスについて説明します。
helpx_creative_field: ""
helpx_description: Designer > Bakers > Bakers Legacy Interface
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベイカーレガシーインターフェイス
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '378'
ht-degree: 3%

---


# ベイカーレガシーインターフェイス

バージョン6.0.4より前の[Adobe Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)で使用できるベイカーインターフェイスについて説明します。

## 概要

![](bakers-legacy-interface.resources/bakers-legacy-interface-01.png)

ベイカーパネルは4つの部分に分かれています。

### 1:シーン

![](bakers-legacy-interface.resources/bakers-legacy-interface-02.png)

メッシュのどの部分がベイク処理プロセスに関係しているかを定義できます。

バージョン6の新機能では、マテリアル別に選択することもできます。

![](bakers-legacy-interface.resources/bakers-legacy-interface-03.png)

### 2:ベイカー

![](bakers-legacy-interface.resources/bakers-legacy-interface-04.png)

![](bakers-legacy-interface.resources/bakers-legacy-interface-05.png)ボタンを押すと、目的のベイカーを処理リストに追加できます

>[!NOTE]
>
> パンはリスト順（上から下へ）に従って処理されます。これは、法線マップなど、烘焙の結果を別のベイクプロセスで再利用する場合に重要になることがあります

ベイカーレイアウトの「+」をクリックすると、スタックにベイカーを追加できます（スタックには必要な数のベイカーを追加できます）。

.![](bakers-legacy-interface.resources/bakers-legacy-interface-06.png)

![](bakers-legacy-interface.resources/bakers-legacy-interface-07.png)キーを押すと、一覧からベイクプロセスを削除できます

ベイク処理プロセスを選択して![](bakers-legacy-interface.resources/bakers-legacy-interface-08.png)を使用すると、ベイク処理プロセスの一覧を並べ替えることができます

### 3:ベイカーパラメーター

![](bakers-legacy-interface.resources/bakers-legacy-interface-09.png)

このセクションには、現在選択されているベイカーに固有のオプションが表示されます。

### 4：共通パラメーター

![](bakers-legacy-interface.resources/bakers-legacy-interface-10.png)

ベイカー間で共有されているパラメーターが表示されます。

>[!NOTE]
>
> デフォルトでは、これらのパラメータの1つを変更すると、すべてのベイカーに影響します。ただし、すべてのベイカーに共通のオーバーライドパラメータにチェックを入れた場合は、変更は現在のベイカーに対してローカルになります。

* **[リソース名]**&#x200B;フィールドでは、必要に応じて、生成されたビットマップの名前を変更できます。
* **ファイル形式**&#x200B;のドロップダウンリストでは、既定のファイル形式（WindowsまたはOS/2ビットマップ形式、「BMP」）を変更できます。
* **&#x200B;**&#x200B;**[メッシュ固有のフォルダにリソースを配置する]チェックボックスをオンにすると、生成されたビットマップをモデルと同じレベルで保存するか、[Resources]という名前の新しいサブフォルダ内に保存するかを指定できます。**
* **メソッド**&#x200B;を使用すると、新しいビットマップSubstanceをリソースパッケージにリンクするか埋め込むかを指定できます。
* **フォルダー**&#x200B;では、マップを保存する場所を定義できます。

ベイカーウィンドウの右下にある「OK」ボタンを押すと、ベイクプロセスが開始されます。

バージョン6の新機能：「キャンセル」ボタンを使用して、ベイクプロセスをキャンセルできるようになりました。

![](bakers-legacy-interface.resources/bakers-legacy-interface-11.png)
