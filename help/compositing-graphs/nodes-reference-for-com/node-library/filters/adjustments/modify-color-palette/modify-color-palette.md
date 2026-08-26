---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/filters/adjustments/modify-color-palette.html"
breadcrumb-title: ''
description: '[カラーパレットを修正]ノードを使用して、テクスチャから抽出されたカラーパレットを調整および変換します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Filters > Adjustments > Modify Color Palette
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: カラーパレットを修正
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '857'
ht-degree: 0%

---


# カラーパレットを修正

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![色の量子化アイコン](../../../../../../assets/ModifyColorPalette.png "色の量子化アイコン"){width="200px"}

<b>イン:</b>フィルター/調整

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

番号付きパレットのカラーを変更し、IDマップを使用して画像に適用します。

IDマップのインデックスをパレットのカラーのインデックスと一致させることで、カラーを選択できます。

例えば、パレットのカラー#2は、ID値が2のIDマップ内のすべてのピクセルに適用されます。

このノードは、次のノードと組み合わせて使用できます： [色のクオンタイズ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)、[カラーパレットの作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)、[カラーパレットの適用](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md)、[カラーパレットの表示](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)。

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">



</td>
<td style="border: 0;" valign="top">

### 出力コネクタ

</td>
<td style="border: 0;" valign="top">

### パラメーター

</td>
</tr>
</table>

## 入力コネクタ

|  |  |
| --- | --- |
| <b>ID</b> *グレースケール*&#x200B;プライマリ | カラーを変更して出力に分配するために、カラーの選択に使用する入力IDマップ。   IDマップは、全体（例えば、シェイプ）の一部であるピクセルがすべて同じ一意の識別値を保持する画像です。 この場合、値は整数です。   IDマップは、[クオンタイズカラー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)ノードを使用して作成できます。 |
| <b>パレット</b> *色* | ピクセルの行としてエンコードされたRGBカラーの順序付けされたリスト。 パレットには、最大256色を保持できます。 これは、ノードが変更するパレットです。   パレットは、[色を量子化](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/quantize-color/quantize-color.md)または[カラーパレットを作成](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/create-color-palette-16/create-color-palette-16.md)のノードを使用して作成できます。 |

## 出力コネクタ

|  |  |
| --- | --- |
| <b>出力</b> *色* | 修正したパレットの色をIDマップのインデックスにマッピングした結果。 |
| <b>パレット</b> *色* | 指定した色の変更が適用された、更新されたパレット。   パレットは、[カラーパレットを適用](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/apply-color-palette/apply-color-palette.md)ノードを使用して別の画像に適用するか、[カラーパレットを表示](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/filters/adjustments/view-color-palette/view-color-palette.md)ノードを使用して表示できます。 |

## パラメーター

|  |  |
| --- | --- |
| <b>カラー選択モード</b> *整数* | 変更するパレット内のターゲットカラーを選択する方法。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>カラーインデックス：</b>ターゲット色のインデックス</li> <li data-preserve-html="true"><b>画像領域：</b> IDマップ内でインデックスをサンプリングする位置です。 このモードを選択すると、2Dビューで位置ギズモを使用して簡単に選択できるようになります</li> </ul> |
| <b>カラー位置</b> *Float2* *&#39;カラー選択モード&#39;が&#39;イメージスペース&#39;に設定されている場合に使用可能* | IDマップ内で索引をサンプリングする位置。   2Dビューのギズモを使用すると、画像内の位置を簡単に選択できます。   ヒント： IDマップの抽出元の量子化されたイメージを表示し、[カラーパレットを修正]ノードを選択してギズモを表示できます。 これにより、カラーを選択してより直感的に変更できるようになります。 |
| <b>カラーインデックス</b> *整数* *&#39;色選択モード&#39;が&#39;カラーインデックス&#39;に設定されている場合に使用できます* | ターゲットカラーのインデックス。   パレットの色は左から右に並べられ、最初の色のインデックスは0です。 |
| <b>カラー選択スプレッド</b> *フロート* | 選択範囲が隣接するカラーに達する範囲を制御します。   色は、*立方体*&#x200B;に配置され、幅、Height、および深度は、色の各構成要素が0から1に増加するグラデーションです(例： 赤、緑、青(RGB)。   このパラメーターは、立方体の選択したカラーの周囲にある他のカラーも変更可能な範囲を調整します。1は立方体の幅の全体です。 |
| <b>カラー選択のコントラスト</b> *フロート* | 隣接するカラー上での選択範囲の減衰グラデーションを制御します。   色は、*立方体*&#x200B;に配置され、幅、Height、および深度は、色のコンポーネントが0から1に増加するグラデーションです(例： 赤、緑、青(RGB)。   このパラメータは、選択したカラーの周囲の立方体の他のカラーの上に選択範囲のフォールオフを調整します。ここで、0は選択したカラーから最も遠いカラーへの滑らかなグラデーションで、1は完全に含まれたものから含まれないものへのカットオフです。 |
| <b>距離のカラースペース</b> *整数* | 色は、*立方体*&#x200B;に配置され、幅、Height、および深度は、色のコンポーネントが0から1に増加するグラデーションです(例： 赤、緑、青(RGB)。   このパラメーターを使用すると、立方体のカラーの分布に使用されるカラースペースを選択できます。このカラースペースにより、隣接するカラーが変更されます。   ユースケースに適したカラースペースを選択できます。<ul data-preserve-html="true"> <li data-preserve-html="true"><b>Lab (Color):</b>標準化された知覚的カラースペースです。「感じる」近くの色が実際には立方体で近くなるように色を分配します。 これは、ディスプレイ上で表示される画像に適しています。</li> <li data-preserve-html="true"><b>RGB（データ）:</b>色は赤、緑、青に分割され、人間の知覚を無視してそれらの軸に沿ってまっすぐに分布しています。 これは、法線マップなどの未加工データを保持するイメージに適しています。</li> </ul> |
| <b>モード</b> *整数* | ターゲットカラーを変更する方法：<ul data-preserve-html="true"> <li data-preserve-html="true"><b>色の上書き：</b>色を別の色に置き換えます</li> <li data-preserve-html="true"><b>HSL:</b>色相、彩度、明度のオフセットを使用してカラーを調整します</li> </ul> |
| <b>不透明度</b> *フロート* | 元のカラーと変更されたカラーの補間を制御します。1の場合は、変更されたカラーが元のカラーと完全に置き換わります。 |
| <b>色の上書き</b> *Float3* *&#39;Mode&#39;が&#39;Override color&#39;に設定されている場合に使用可能* | 元のカラーと置き換えるカラーを指定します。 |
| <b>HSL</b> *Float3* *&#39;Mode&#39;が&#39;HSL&#39;に設定されている場合に使用可能* | 元のカラーに適用される色相、彩度、明度のオフセットを制御します。 |

## 例

![カラーパレットの変更：例1](../../../../../../assets/modify_color_palette_example_1.png "カラーパレットの変更：例1"){zoomable="yes"}

![カラーパレットの変更：例2](../../../../../../assets/modify_color_palette_example_3.png "カラーパレットの変更：例2"){zoomable="yes"}

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_before.jpg" alt="modify_color_example_2_before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/modify_color_example_2_after.jpg" alt="modify_color_example_2_after">
      <br><i>後</i>
    </td>
  </tr>
</table>
