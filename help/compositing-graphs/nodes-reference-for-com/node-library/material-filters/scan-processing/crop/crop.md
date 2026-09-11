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
source-git-commit: 2c331b568074714ea71231410f997f965e2bcdaa
workflow-type: tm+mt
source-wordcount: '259'
ht-degree: 3%

---


# 切り抜き

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![](crop.resources/crop-10.png){width="128px"}

![](crop.resources/crop-grayscale.png){width="128px"}

<b>イン：</b> マテリアルフィルター > スキャン処理

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

切り抜きは、使い慣れた切り抜きツールのパラメトリックな非破壊的バージョンです。 画像内の領域を選択すると、選択されていない領域が破棄された状態で結果が返されます。

これは、アトミックノードを使用した切り抜き操作はそれほど簡単ではないので、多くの方法で便利です。 特に、非正方形の画像を変換する場合は、このノードが便利です。 この場合は、入力解像度を正しく設定してください。

理解することが非常に重要です。このノードを簡単に使用するには、編集しているパラメータを持つノードとは異なるノードをプレビューする機能を十分に活用する必要があります。\
簡単に言うと、このノード（元の、切り抜かれていない画像）の入力として使用しているノードを&#x200B;**ダブルクリック**&#x200B;し、その直後に続く切り抜きノードを&#x200B;**シングルクリック**&#x200B;します。 その後、切り抜く領域に合わせて切り抜きギズモを変更できます。

</td>
</tr>
</table>

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>入力サイズ</b> <i>0 - 8192</i> | 入力画像の解像度と縦横比。 非正方形の画像では非常に重要です。 |
| <b>背景</b> <i>（カラー値） / （グレースケール値）</i> | 切り抜きによってカバーされない領域の背景の均一値。 |
| <b>変形</b> <i>（変換行列）</i> | 結果を回転およびスケールします。 カンバスを直接操作して、結果を変更できます。 |
| <b>オフセット</b> <i>0.0 - 1.0</i> | 結果を移動または変換します。 カンバスを直接操作して、結果を変更できます。 |
| <b>標準（カラーバージョンのみ）</b> <i>False/True</i> | 入力をNormalmapとして扱うかどうかを指定します。 |
