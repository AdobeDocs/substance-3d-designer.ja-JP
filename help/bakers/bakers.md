---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: Substance 3D Designer ベイカーを使用して、メッシュベースの情報を計算してテクスチャファイルに変換する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベイカー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 2e92fd4d2b50ba675396d016e31e4a60d338711b
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# ベイカー

ベイクとは、**メッシュに基づく情報をテクスチャに転送する**&#x200B;操作を指します。 これらの情報は、シェーダやSubstanceフィルタによって読み取られ、より高度なエフェクトやテクスチャが生成されます。

>[!NOTE]
>
> ベイク処理について詳しくは、[ベイク処理ドキュメント](https://experienceleague.adobe.com/ja/docs/substance-3d/bakers/home)を参照してください。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

ベイクウィンドウには、[エクスプローラー](../interface/the-explorer-window/the-explorer-window.md)ウィンドウのメッシュファイルからアクセスできます。 メッシュ名を右クリックして「**モデル情報を烘焙**」を選択し、ベイクウィンドウを開きます。

</td>
<td width="33.33%" style="border: 0;" valign="top">

3D シーンリソースのコンテキストメニューの![&#39;モード情報のベイク&#39;オプション](bakers.resources/bakers-01.png "&#39;3D シーンリソースのコンテキストメニューのモード情報のベイク&#39;オプション")

</td>
</tr>
</table>

![ベイク処理ウィンドウ](bakers.resources/bakers-02.png "ベイク処理ウィンドウ")

## 概要

のベイクウィンドウは、次に示すいくつかのパネルに分かれています。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### ベイクするエレメント

このパネルは、ローポリメッシュのどの部分を使用してベイクを行うかを制御します。

ローポリゴンメッシュファイル内にあるジオメトリが一覧表示されます。 デフォルトでは、リストはファイル内で見つかった個々のマテリアルに基づいていますが、関連がある場合は代わりにサブメッシュに切り替えることができます。 ベイクプロセス中に無視するエレメントのチェックを外すことができます。

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/bakers-03.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 出力

このパネルは、ベイクされたテクスチャの場所を制御します。

</td>
<td style="border: 0;" valign="top">

![](bakers.resources/bakers-04.png)

</td>
</tr>
</table>

| *パラメーター* | *説明* |
| --- | --- |
| **メソッド** | テクスチャをSubstanceパッケージと一緒に保存する方法を制御します。有効な値：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>埋め込み</strong> :ベイクされたテクスチャは、特定の名前でSubstanceパッケージの横にあるサブフォルダーに保存されます。</li><li data-preserve-html="true"><strong>リンク</strong> （デフォルト） ：ベイク処理されたテクスチャは定義されたフォルダーに保存され、パッケージ化されたSubstanceー内で参照されます。</li></ul> |
| **フォルダー** | 保存時のベイク処理されたテクスチャの場所。 3つのドットボタンをクリックしてファイルダイアログを開き、書き出しフォルダーを選択します。右側にチェックマークが表示され、フォルダーが実際に存在するかどうかが示されます。 |
| **名前** | ベイク処理されたテクスチャの命名規則。 3つのドットボタンをクリックしてドロップダウンを開き、他のプレースホルダー（ベーカネーム、カスタム、マテリアル、メッシュ）を挿入します。 |
| **サンプル** | ファイル名をシミュレートして、命名規則をテストします。 |
| **メッシュ固有のフォルダーにリソースを配置する** | 有効な場合、ベイク処理されたテクスチャはメッシュファイルという名前のフォルダに保存されます。 |

### 高精細メッシュ

このパネルは、ハイポリゴンメッシュリストおよび関連する設定をコントロールします。 詳細については、[共通パラメーター](https://experienceleague.adobe.com/ja/docs/substance-3d/bakers/bakers-settings/common-parameters)を参照してください。

![高精細メッシュ](bakers.resources/bakers-05.png "高精細メッシュ")

### デフォルト値

詳細については、[共通パラメーター](https://experienceleague.adobe.com/ja/docs/substance-3d/bakers/bakers-settings/common-parameters)を参照してください。

![既定値](bakers.resources/bakers-06.png "既定値")

### ベイカーのレンダーリストと設定

**ベイカーレンダリングリスト**&#x200B;では、生成するベイク処理されたテクスチャを選択できます。 デフォルトでは、リストは空です。

* **新しいパン屋を追加しています：** [パン屋の追加]ボタンをクリックしてください。
* **ベイカーを削除する：**&#x200B;リストからベイカーを選択し、「Delete baker」ボタンをクリックします。
* **パン屋を一番上に移動する：**&#x200B;リストでパン屋を選択し、[一番上に移動]をクリックします。
* **パン屋さんの下へ移動する：**&#x200B;リストからパン屋さんを選択し、[下へ移動]ボタンをクリックします。

継承の各ベイカーは、デフォルトでデフォルト値（上記を参照）を使用します。 たとえば、サイズ（解像度）は、パン屋の行のセルをクリックして上書きできます。 これは、線上の他の設定についても同様です。

リスト内のベイカーをクリックすると、ベイカーパラメータービューが特定のパラメーターで更新されます。

特定のパラメーターの詳細については、「[ベイカー設定](https://experienceleague.adobe.com/ja/docs/substance-3d/bakers/bakers-settings/bakers-settings)」を参照してください。

![ベーカーレンダリングリスト](bakers.resources/bakers-07.png "ベーカーレンダリングリスト")
