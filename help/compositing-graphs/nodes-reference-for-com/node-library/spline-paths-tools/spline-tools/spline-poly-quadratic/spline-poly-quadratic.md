---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/spline-tools/spline-poly-quadratic.html"
breadcrumb-title: ''
description: '[スプラインポリゴン二次]ノードを使用して、複数の制御点を持つ複雑な二次スプラインを作成します。'
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Spline Tools > Spline (Poly Quadratic)
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: スプライン（多二次）
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4ae20991693573dd44016a411c233b071fa96df6
workflow-type: tm+mt
source-wordcount: '1149'
ht-degree: 0%

---


# スプライン（多二次）

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](spline-poly-quadratic.resources/spline-poly-quadratic-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール> スプラインツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

いくつかの点に沿ってスプラインを生成します。 これらのポイントの数と位置は任意であるか、[ポイントリスト](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md)ノードから収集される可能性があります。

</td>
</tr>
</table>

スプラインの軌道は、個々の中間点が隣接するパスの「out」および「in」正接の合流点であるという点で、その中間点から離れてスムーズ化することができます。

<a name="inputs"></a>

## 入力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 入力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの点の座標：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた入力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 入力スプラインの数。 |
| <b>ポイントのプレビュー</b> <i>グレースケール</i> | ポイントをグレースケールイメージとしてプレビューします。 |
| <b>入力ポイントリスト</b> <i>色</i> | （「入力ポイント一覧を使用」がTrueの場合に使用可能）色画像のRGBAチャンネルにエンコードされたポイントの一覧：<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> -整数部分： Smoothness;<br> – 小数部分： Thickness。 |
| <b>ポイント番号</b> <i>整数</i> | （「入力ポイントリストを使用」がTrueの場合に使用可能）ポイントの数。 |

>[!IMPORTANT]
>
> <b>ポイントリスト</b>と<b>ポイント番号</b>コネクタは、<b>スプライン座標</b>、<b>スプラインデータ</b>および<b>スプライン量</b>コネクタと&#x200B;*互換性がありません*。これらのコネクタは異なるデータに依存しています。

<a name="outputs"></a>

## 出力

|  |  |
|:---|:---|
| <b>プレビュー</b> <i>グレースケール</i> | 出力スプラインをグレースケールイメージとしてプレビューします。 |
| <b>スプライン座標</b> <i>色</i> | 出力スプラインの座標がカラー画像のRGBAチャンネルにエンコードされました。<br><b>R</b> - X位置<br><b>G</b> - Y位置<br><b>B</b> - Height<br><b>A</b> – パックデータ：<br> – 記号：スプラインが閉じている（負）か開いている（正）;<br> -絶対値: Thickness + 1。 |
| <b>スプラインデータ</b> <i>色</i> | カラー画像のRGBAチャンネルでエンコードされた出力スプラインの追加データ。<br><b>R</b> -正接X<br><b>G</b> -正接Y<br><b>B</b> – 未使用<br><b>A</b> – 未使用 |
| <b>スプラインの量</b> <i>整数</i> | 出力スプラインの数。 |

<a name="parameters"></a>

## パラメーター

|  |  |
|:---|:---|
| <b>ポイント数</b> <i>整数</i> | スプラインの構築に使用する点の数を任意に指定します。 |
| <b>入力スプライン接続モード</b> <i>整数</i> | 入力スプラインを接続するために使用される方法：<br>- <i>自動：</i>最後の入力スプラインの終点は生成されたスプラインの始点に接続され、生成されたスプラインの終点は最初の入力スプラインの始点に接続されます。<br>- <i>手動：</i>生成されたスプラインの先端に接続する入力スプラインと、これらの接続が配置される入力スプラインを指定できます。 |
| <b>スプラインを閉じる</b> <i>ブール値</i> | スプラインの終点を始点に接続するかどうかをコントロールします。<br>始点と終点でスプラインに適用されたスムージングは、これらの点のSmoothness値によって指定されます。 |
| <b>方向を反転</b> <i>ブール値</i> | スプラインの方向を反転します。 |
| <b>入力ポイントリストを使用</b> <i>ブール値</i> | 任意のポイントリストの代わりに、[入力ポイントリスト]および[ポイント番号]入力コネクターに指定されたポイントリストを使用します。<br>ポイントのリストは、[ポイントリスト](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/spline-tools/point-list/point-list.md)ノードから提供できます。 |
| <b>入力スプラインへの接続開始</b> <i>ブール値</i> | Trueの場合、生成されたスプラインの始点は、入力スプラインの最後のスプラインの最後の点に接続されます。 |
| <b>接続スプラインインデックスの開始</b> <i>整数</i> | （[入力スプラインの接続モード]が[手動]に、[入力スプラインに始点を接続]が[真]に設定されている場合に使用可能）生成されたスプラインの始点に接続する入力スプラインのインデックス。 |
| <b>接続開始の位置</b> <i>フロート</i> | （[入力スプラインの接続モード]が[手動]に設定され、[開始点を入力スプラインに接続]が[はい]に設定されている場合に使用可能）生成されたスプラインの開始点への接続が配置される、選択された入力スプライン上の位置です。<br>この値は、選択した入力スプラインの正規化された長さです。 |
| <b>入力スプラインへの終点の接続</b> <i>ブール値</i> | Trueの場合、生成されたスプラインの終端は、入力スプラインの最初のスプラインの最初の点に接続されます。 |
| <b>接続スプラインインデックスの終了</b> <i>整数</i> | （[入力スプラインの接続モード]が[手動]に、[入力スプラインに端点を接続]が[真]に設定されている場合に使用可能）生成されたスプラインの端点に接続する入力スプラインのインデックス。 |
| <b>接続位置の終了</b> <i>フロート</i> | （[入力スプラインの接続モード]が[手動]に、[端点を入力スプラインに接続]が[はい]に設定されている場合に使用可能）生成されたスプラインの端点への接続が配置される、選択した入力スプライン上の位置。<br>この値は、選択した入力スプラインの正規化された長さです。 |
| <b>均一な分布</b> <i>ブール値</i> | Trueの場合、スプラインの点は始点から終点まで等間隔になります。 |
| <b>入力スプラインを追加</b> <i>ブール値</i> | 生成されたスプラインを、<b>スプライン</b>入力に接続されたスプラインの一覧の最後に追加します。 |
| <b>非正方形の修正</b> <i>ブール値</i> | 点の位置とThicknessを調整して、非正方形の解像度でスプラインの形状を保持します。<br>均一な分布にも影響します。 |
| <b>グローバルSmoothness調整</b> <i>フロート</i> | すべてのポイントのSmoothnessの値に均等オフセットを適用します。<br>結果のSmoothness値は[0;1]の範囲に固定されます。 |
| <b>ポイントのプロパティ</b> |  |
| <b>p#プロパティ</b> <i>浮動小数点3</i> | p#の点のプロパティを設定します。<br>- <i>Height:</i>値が小さいほどHeightが低く、深い方を表す点の位置を調整します。<br>- <i>Smoothness:</i>スプラインの滑らかさの開始点をp#でオフセットします。値が0の場合、硬い軌道になり、完全に滑らかな1になります。<br>- <i>Thickness:</i> p#のスプラインのThicknessを調整します。 Thicknessは、特定のスプラインノードによって使用されます。 |
| <b>点の座標</b> |  |
| <b>p#</b> <i>浮動小数点2</i> | テクスチャ空間のp#ポイントの位置を設定します。 |
| <b>プレビュー</b> |  |
| <b>接線を表示</b> <i>ブール値</i> | p1およびp3ポイントの正接をプレビュー出力のp2に表示します。 |
| <b>方向ヘルパーの表示</b> <i>ブール値</i> | プレビュー出力で、スプラインの始点に点を表示し、終点に矢印を表示します。 |
| <b>Thicknessの封筒を表示</b> <i>ブール値</i> | スプラインのThicknessのエッジに追加の線分を表示します。 |
| <b>ポイントラベルの表示</b> <i>ブール値</i> | 各ポイントについて、「プレビュー」出力でポイントの横にポイント名が表示されます。 |
| <b>ポイントラベルサイズ</b> <i>フロート</i> | （「ポイントのラベルを表示」が「True」に設定されている場合に使用可能）テクスチャスペースの各ポイントのラベルのサイズ。0.1はテクスチャの幅の10分の1です。 |
| <b>ポイントの表示</b> <i>ブール値</i> | スプラインの制御点を表示します。 |
| <b>ポイントサイズ</b> <i>フロート</i> | （「ポイントを表示」が「True」に設定されている場合に使用可能）テクスチャ空間内のポイントの半径。0.1はテクスチャの幅の10分の1です。 |
| <b>セグメント数</b> <i>整数</i> | プレビュー出力でスプラインの視覚化に使用するセグメントの数を調整します。<br>値を大きくすると、より滑らかな線になります。 |
| <b>Thickness (px)</b> <i>フロート</i> | プレビュー出力のスプラインの表示Thicknessをピクセル単位で調整します。 |

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-Before.jpg" alt="SplinePolyQuadratic-Variant1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="spline-poly-quadratic.resources/SplinePolyQuadratic-Variant1-After.jpg" alt="SplinePolyQuadratic-Variant1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

![ノードの例2](spline-poly-quadratic.resources/SplinePolyQuadratic-Demo.gif "ノードの例2")

</td>
</tr>
</table>
