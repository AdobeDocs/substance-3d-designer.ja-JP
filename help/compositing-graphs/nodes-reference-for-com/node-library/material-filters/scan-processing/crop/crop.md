---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/crop.html"
breadcrumb-title: ''
description: 「切り抜き」ノードを使用すると、マテリアル出力を特定の領域に切り抜いて、スキャンされたマテリアルおよびテクスチャを処理できます。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Crop
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 切り抜き
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 1%

---


# 切り抜き

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/crop-10.png){width="128px"}

![](../../../../../../assets/crop-grayscale.png){width="128px"}

## 切り抜き（グレースケール）

**イン：** *マテリアルフィルター/スキャン処理*

**中級**

</td>
<td style="border: 0;" valign="top">

## 説明

切り抜きは、使い慣れた切り抜きツールのパラメトリックな非破壊的バージョンです。 画像内の領域を選択すると、選択されていない領域が破棄された状態で結果が返されます。

これは、アトミックノードを使用した切り抜き操作はそれほど簡単ではないので、多くの方法で便利です。 特に、非正方形の画像を変換する場合は、このノードが便利です。 この場合は、入力解像度を正しく設定してください。

理解することが非常に重要です。このノードを簡単に使用するには、編集しているパラメータを持つノードとは異なるノードをプレビューする機能を十分に活用する必要があります。\
簡単に言うと、このノード（元の、切り抜かれていない画像）の入力として使用しているノードを&#x200B;**ダブルクリック**&#x200B;し、その直後に続く切り抜きノードを&#x200B;**シングルクリック**&#x200B;します。 その後、切り抜く領域に合わせて切り抜きギズモを変更できます。

## パラメーター

* **入力サイズ**: *0 - 8192*&#x200B;入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。
* **背景**: *（カラー値） / （グレースケール値）*切り抜きによってカバーされない領域の背景の均一値。
* **変換**: *（変換行列）*\
  結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。
* **オフセット**: *0.0 - 1.0*\
  結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。
* **標準（カラーバージョンのみ）**: *False/True*&#x200B;入力をNormalmapとして扱うかどうか。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
