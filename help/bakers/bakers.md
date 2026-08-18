---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/bakers.html"
breadcrumb-title: ''
description: Substance 3D Designerベイカーを使用してメッシュベースの情報を計算し、テクスチャファイルに変換する方法を説明します。
helpx_creative_field: ""
helpx_description: Designer > Bakers
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベイカー
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68389d2a09ef1db6c14073029efdbfd9d48c83c8
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---


# ベイカー

ベイク処理とは、**メッシュベースの情報をテクスチャに転送**&#x200B;する操作を指します。 これらの情報は、シェーダやSubstanceフィルタによって読み取られ、より高度なエフェクトやテクスチャが生成されます。

>[!NOTE]
>
> ベイク処理の詳細については、[ベイク処理に関するドキュメント](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/home)を参照してください。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

ベイクウィンドウには、[エクスプローラー](../interface/the-explorer-window/the-explorer-window.md)ウィンドウのメッシュファイルを使用してアクセスできます。 メッシュ名を右クリックして「**モデル情報をベイク処理**」を選択し、ベイク処理ウィンドウを開きます。

</td>
<td width="33.33%" style="border: 0;" valign="top">

![&#39;ベイクモード情報&#39;オプション、3Dシーンリソースのコンテキストメニュー](../assets/sd-mesh-right-click.png "&#39;ベイクモード情報&#39;オプション、3Dシーンリソースのコンテキストメニュー")

</td>
</tr>
</table>

![ウィンドウのベイク処理](../assets/sd-window-overview.png "ウィンドウのベイク処理")

## 概要

のベーキングウィンドウは、以下に説明するいくつかのパネルに分割されています。

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### ベイクする要素

このパネルは、ベイク処理に使用するローポリメッシュの部分を制御します。

ローポリゴンメッシュファイル内で見つかったジオメトリが一覧表示されます。 デフォルトでは、リストはファイル内で見つかった個々のマテリアルに基づいていますが、関連する場合は代わりにサブメッシュに切り替えることができます。 ベイクプロセス中に無視する要素のチェックを外すことができます。

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-mesh-selection.png)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### 出力

このパネルは、ベイク処理されたテクスチャの配置場所を制御します。

</td>
<td style="border: 0;" valign="top">

![](../assets/sd-output.png)

</td>
</tr>
</table>

| *パラメーター* | *説明* |
| --- | --- |
| **メソッド** | ベイク処理されたテクスチャをSubstanceパッケージと一緒に格納する方法を制御します。有効な値：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>埋め込み</strong> ：ベイク処理されたテクスチャは、特定の名前でSubstanceパッケージの横にあるサブフォルダーに保存されます。</li><li data-preserve-html="true"><strong>リンク</strong> （デフォルト） ：ベイク処理されたテクスチャは定義されたフォルダーに保存され、パッケージ化されたSubstanceー内で参照されます。</li></ul> |
| **フォルダー** | 保存時のベイク処理されたテクスチャの場所。 3つのドットボタンをクリックしてファイルダイアログを開き、書き出しフォルダーを選択します。右側にチェックマークが表示され、フォルダーが実際に存在するかどうかが示されます。 |
| **名前** | ベイク処理されたテクスチャの命名規則。 3つのドットボタンをクリックしてドロップダウンを開き、他のプレースホルダー（ベーカネーム、カスタム、マテリアル、メッシュ）を挿入します。 |
| **サンプル** | ファイル名をシミュレートして、命名規則をテストします。 |
| **メッシュ固有のフォルダーにリソースを配置する** | 有効な場合、ベイク処理されたテクスチャはメッシュファイルという名前のフォルダに保存されます。 |

### 高精細メッシュ

このパネルは、ハイポリゴンメッシュリストおよび関連する設定をコントロールします。 詳細については、[共通パラメーター](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters)を参照してください。

![高精細メッシュ](../assets/sd-high.png "高精細メッシュ")

### デフォルト値

詳細については、[共通パラメーター](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/common-parameters)を参照してください。

![既定値](../assets/sd-default-values.png "既定値")

### ベイカーのレンダーリストと設定

**ベイカーレンダリングリスト**&#x200B;では、生成するベイク処理されたテクスチャを選択できます。 デフォルトでは、リストは空です。

* **新しいパン屋を追加しています：** [パン屋の追加]ボタンをクリックしてください。
* **ベイカーを削除する：**&#x200B;リストからベイカーを選択し、「Delete baker」ボタンをクリックします。
* **パン屋を一番上に移動する：**&#x200B;リストでパン屋を選択し、[一番上に移動]をクリックします。
* **パン屋さんの下へ移動する：**&#x200B;リストからパン屋さんを選択し、[下へ移動]ボタンをクリックします。

継承の各ベイカーは、デフォルトでデフォルト値（上記を参照）を使用します。 たとえば、サイズ（解像度）は、パン屋の行のセルをクリックして上書きできます。 これは、線上の他の設定についても同様です。

リスト内のベイカーをクリックすると、ベイカーパラメータービューが特定のパラメーターで更新されます。

特定のパラメーターの詳細については、「[ベイカー設定](https://experienceleague.adobe.com/en/docs/substance-3d/bakers/bakers-settings/bakers-settings)」を参照してください。

![ベーカーレンダリングリスト](../assets/sd-baker-list.png "ベーカーレンダリングリスト")
