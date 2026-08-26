---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/spline-paths-tools/path-tools/mask-to-paths.html"
breadcrumb-title: ''
description: マスクからパスノードを使用して、マスクテクスチャをプロシージャパス生成用のパスデータに変換します。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Spline  Path Tools > Path Tools > Mask to Paths
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: パスにマスク
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1113'
ht-degree: 0%

---


# パスにマスク

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![ノードアイコン](../../../../../../assets/mask-to-paths-icon.png "ノードアイコン")

<b>イン：</b>スプラインおよびパスツール>パスツール

</td>
<td width="100.00%" style="border: 0;" valign="top">

## 説明

グレースケール入力パターン<b>Mask</b>を、出力<b>Paths</b>でエンコードされたパスセグメントの一覧に変換します。

生成されたパスの開始位置と、リスト内でのパスの順序を制御できます。

生成されたパスは、専用ノード（例： [パス2D変形](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/path-2d-transform/path-2d-transform.md)、[パスワープ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-warp/paths-warp.md)）を使用してさらに処理するか、[スプラインへのパス](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)ノードを使用してスプラインに変換し、それらに沿ってシェイプをマップまたは散乱することができます。

</td>
</tr>
</table>

>[!NOTE]
>
> パスのエンコードに使用される方法については、[パス形式の仕様](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-format-spe/paths-format-specifications.md)のページで説明しています。

## 入力コネクタ

<b>マスク</b> *グレースケール*\
パスのリストに変換する入力パターン。

## 出力コネクタ

<b>プレビュー</b> *色*&#x200B;マスクの上に合成されたプレビューで、パラメーターの効果を視覚化するのに役立ちます。

<b>パス</b> *色*\
カラー画像でエンコードされたパスのリスト。 各パスは、エンコードされたセグメントのリストを記述します。\
結果は、別のパス処理ノードを使用して処理するか、[Paths to Spline](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-to-spline/paths-to-spline.md)ノードに送信して、さらにスプラインとして処理することができます。

## パラメーター

<b>スムーズマスク</b> *フロート*\
定型入力にスムージングを適用します。\
入力パターンのエッジが非常にシャープで、通常は斑点が生じる場合に便利です。

<b>マスクのしきい値</b> *浮動小数点*&#x200B;図形の外側（値&lt;マスクのしきい値）と内側（値>マスクのしきい値）を分離するために使用される<b>マスク</b>のグレースケール値です。

<b>パスの小数点以下の桁数</b> *フロート*&#x200B;生成されるセグメントの量を暗黙的に制御します。\
デシメーション値を大きくすると、丸いシェイプはやや多角形になりますが、デシメーション値を使用しないと、1ピクセルあたりに1セグメント程度が生成されます。\
合理的な量を選択すると、直線の中間点を大幅に増やすことなく、直線と曲線の両方の形状に合った形状になります。

<b>開いているパスを閉じる</b> *ブール値*&#x200B;オープンパスの開始と終了の頂点の間にセグメントを作成します。\
これを無効にすると、パターンを横切る不要な線が予期しない方法で修正される場合がありますが、パスが閉じられなくなる可能性があります。

<b>コーナーのしきい値</b> *フロート*\
パスにエンコードされた各頂点には、ハード（コーナー）かスムーズ（滑らか）かを示すフラグを保持できます。\
このパラメーターを使用すると、隣接するセグメント間の角度に応じて、コーナーをマークすることができます。\
*注意：*&#x200B;この&#39;corner&#39;フラグは現在、既存のノードではサポートされていませんが、[パス頂点プロセッサ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/paths-vertex-processor/paths-vertex-processor.md)ノードで使用できます。 [パスのプレビュー](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/spline-paths-tools/path-tools/preview-paths/preview-paths.md)ノードで角を表示することもできます。

<b>パスのスタートアップモード</b> *整数*&#x200B;マスク内の図形の周りに生成される各パスの始点とする頂点の選択方法です。\
生成された<b>パスを専用ノードを使用してスプライン</b>に変換する場合、複数のスプラインノードがスプラインの始点と終点を使用するため、これは大きな影響を与えます。\
*– 最も鋭角の頂点：*&#x200B;前後の頂点との角度が最も低い頂点\
*– 指定された方向の頂点：*&#x200B;指定された方向の最後の頂点\
* – 指定位置に最も近い頂点
* 指定した位置から最も遠い頂点
* カスタムスタートアップ関数：*カスタム関数を使用して、各パスの始点として使用する頂点を選択します

<b>スタートアップの方向</b> *フロート*&#x200B;開始頂点を選択する方向を示す角度です。 パスごとに、この方向の最後の頂点が選択されます。\
この値は、X左方向のベクトルを回転するために使用される&#x200B;*回転の数*&#x200B;です。 つまり、0は方向ベクトル(-1, 0)を設定し、0.25（90度）は方向ベクトル(0, 1)を設定します。\
*注意：*&#x200B;このパラメーターは、<b>パススタートアップモード</b>が[指定された方向の頂点]に設定されている場合に使用できます

<b>スタートアップターゲットの位置</b> *フロート2*&#x200B;開始の頂点を選択するために使用される画像内の位置です。\
選択した<b>パススタートアップモード</b>に従って、各パスについて、この位置に最も近い頂点または最も遠い頂点が選択されます。\
*注意：*&#x200B;このパラメーターは、<b>パスのスタートアップモード</b>が&#39;指定された位置に最も近い頂点&#39;または&#39;指定された位置から最も遠い頂点&#39;に設定されている場合に使用できます

<b>スタートアップ関数</b> *浮動小数点*&#x200B;開始頂点を選択するために使用する関数です。 Float値を返します。\
各頂点に対して関数が実行され、関数が&#x200B;*最高の結果*&#x200B;を返す頂点が選択されます。\
使用可能な変数：\
*-*&#x200B;頂点。コーナー（実数）*:*&#x200B;頂点のスコアをコーナーの候補として指定します\
*-* vertex.pos(Float2)*:*&#x200B;イメージスペース内の頂点の位置\
*注意：*&#x200B;このパラメーターは、パススタートアップモードが&#39;指定された位置に最も近い頂点&#39;または&#39;カスタムスタートアップ関数&#39;に設定されている場合に使用できます

<b>注文モード</b> *整数*&#x200B;生成されたパスの並べ替え方法です。\
パスの位置またはサイズの境界ボックス&#x200B;*1&rbrace; (Bbox)は、パスを並べ替える基準として使用できます。*\
複数のスプラインノードがスプラインの順序を使用するため、生成された<b>パスを専用ノードを使用してスプライン</b>に変換する場合には、この操作が大きな影響を及ぼします。\
*– レガシー（高速）:*&#x200B;このノードの以前のバージョンで使用されていたメソッドです。パフォーマンスが大幅に向上しています\
*– 方向に沿ってボックスの中心の位置で並べる：*&#x200B;パスは、指定された方向に沿って最初から最後まで、ボックスの中心の位置に従って並べられます\
*- Bboxによる経路の左上の位置：*&#x200B;経路は、経路の左上コーナーの位置に従って、指定された方向に沿って最初から最後に並べられます\
*- Bboxサイズ別 – 最大から最小へ：*&#x200B;パスは、Bboxのサイズに従って、最大から最小へと並べ替えられます\
*- Bboxサイズ別 – 最小から最大まで：*&#x200B;パスは、Bboxのサイズに従って最小から最大まで並べ替えられます\
*– カスタム順序関数：*&#x200B;カスタム関数を使用してパスを順序付けます

<b>順序の指定</b> *フロート*&#x200B;その方向に沿ってパスを最初から最後に並べ替えるのに使用される方向を示す角度です。\
値は、X左方向のベクトルを回転するために使用される&#x200B;*回転の数*&#x200B;です。 つまり、0は方向ベクトル(-1, 0)を設定し、0.25（90度）は方向ベクトル(0, 1)を設定します。

<b>順序付け関数</b> *Float*&#x200B;パスの並べ替えに使用する関数です。 Float値を返します。\
パスは、この関数の値に従って&#x200B;*昇順*&#x200B;で並べ替えられます。 つまり、各パスの関数の結果は、パスの並べ替えに使用された&#x200B;*並べ替えキー*&#x200B;になります。\
使用可能な変数：
* bbox.center (Float2):パスBboxの中心の位置
* bbox.topleft (Float2):パスBboxの左上隅の位置
* bbox.size (Float2):パスのボックスのサイズ（X：幅、Y:Height）

## 例

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-Before.jpg" alt="MaskToPaths-Variant2-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant2-After.jpg" alt="MaskToPaths-Variant2-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
<td style="border: 0;" valign="top">

<table>
  <tr>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-Before.jpg" alt="MaskToPaths – バリアント1-Before">
      <br><i>前</i>
    </td>
    <td>
      <img src="../../../../../../assets/MaskToPaths-Variant1-After.jpg" alt="MaskToPaths – バリアント1-After">
      <br><i>後</i>
    </td>
  </tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例2](../../../../../../assets/MaskToPaths-Demo2.gif "ノードの例2"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ノードの例1](../../../../../../assets/MaskToPaths-Demo1.gif "ノードの例1"){zoomable="yes"}

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![ノードの例3：起動モード](../../../../../../assets/MaskToPaths-Demo3.gif "ノードの例3：起動モード"){zoomable="yes"}

</td>
<td style="border: 0;" valign="top">

![ノードの例3：並べ替えモード](../../../../../../assets/MaskToPaths-Demo4.gif "ノードの例3：並べ替えモード"){zoomable="yes"}

</td>
</tr>
</table>
