---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/output-size.html"
breadcrumb-title: ''
description: Substance合成グラフの出力サイズを設定し、テクスチャの解像度と画質をコントロールします。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Output size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 出力サイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 4f8830fa9ab6012f0a7ba5054eb171b151c44874
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 5%

---


# 出力サイズ

これは、グラフの<b>ベースパラメーター</b>の最初のパラメーターであり、<b>出力形式</b> （ビット深度）と共に、Designer内および他のアプリケーションの両方で、[公開されたSubstance 3Dアセット(SBSAR)](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)ファイルとして、グラフの出力に大きな影響を与えるため、よく理解することが重要です。

>[!TIP]
>
> 出力サイズプロパティを効率的に使用するための基盤として、[Substanceグラフの継承](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)について十分に理解しておくことを強くお勧めします。

>[!NOTE]
>
> ![](../../assets/props-output-size-lock.jpg)ロックボタンを使用して、Heightの値を幅の値と&#x200B;*一致*&#x200B;させます。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## 2の累乗

グラフまたはノードによる&#x200B;*テクスチャ*&#x200B;出力の解像度は、出力サイズパラメーターによって決まります。

グラフィック処理ハードウェアが計算を実行する方法によって課せられた制限に縛られた、グラフィック計算のオブジェクトであるテクスチャ。 これらの制限の1つは、テクスチャは、XとYのピクセル数が&#x200B;*2*&#x200B;の累乗である画像を表す必要があることです。

</td>
<td width="33.33%" style="border: 0;" valign="top">

| 2の累乗 | ピクセル |
| --- | --- |
| 7 | 128 |
| 8 | 256 |
| 9 | 512 |
| 10 | 1024 |
| 11 | 2048 |
| 12 | 4096 |
| 13 | 8192 |

</td>
</tr>
</table>

Output sizeプロパティでは、*対数ステップ*&#x200B;を使用して、2の累乗の増加（例： 256、512、1024、...）を簡単にマップします *線形スケール* （例： 8, 9, 10, ...）に変換します。 つまり、XまたはYの出力サイズの値を1ずつ増やしたり減らしたりすることは、現在の解像度を2で乗算または除算することに似ています。

これは、出力サイズの値が[関数](../../function-graphs/function-graphs.md)によって制御されている場合にも適用されます。この場合、関数は対象の解像度ではなく、対象の対数値（相対または絶対）を出力する必要があります。

>[!IMPORTANT]
>
> XとYの両方で解像度を上げたり下げたりすると、ピクセル数が&#x200B;*4*&#x200B;倍または除算され、グラフの&#x200B;*パフォーマンス*&#x200B;および&#x200B;*メモリ使用量*&#x200B;に大きな影響を与えます。\
> したがって、実際に必要な&#x200B;*最低解像度*&#x200B;を使用して、目的の結果を得ることを強くお勧めします。 解像度を管理することは、[パフォーマンス最適化ガイドライン](../../best-practices/performance-optimization/performance-optimization-guidelines.md)の多くの1つです。

>[!NOTE]
>
> [関数グラフ](../../function-graphs/function-graphs.md)では、`$size`および`$sizelog2`の[システム変数](../../function-graphs/variables/system-variables/system-variables.md)が、ノードまたはグラフの現在の解像度に一致するFloat2値を、それぞれ生のピクセル数または2の累乗として返します。\
> 例えば、1024\*512画像の場合、`$size`は`(1024,512)`を返し、`$sizelog2`は`(10,9)`を返します。

## 相対サイズ

Output Sizeプロパティで&#x200B;*Relative to...* [inheritanceメソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)が使用されている場合、その値は、継承された対数値&#x200B;*に対する相対的な修飾子*&#x200B;として表されます。

継承された解像度に関連する修飾子は、対数スケールで–12 ～ +12の範囲で指定します。デフォルトは0です。 つまり、上または下の各手順を実行すると、解像度が2倍または2分の1になります。 右の表は、継承された値が9(512 = 2^9)および11(2048 = 2^11)の場合に、ある次元で相対的な解像度がどのように変化するかを示した例です。

8196を超えると、サイズは&#x200B;*キャップ*&#x200B;になります。 この上限は、[環境設定](../../interface/preferences-window/preferences-window.md)の<b>一般</b>セクションにある<b>調理サイズ制限</b>の設定によって制御されます。 非常に大きな解像度での作業では、比例したパフォーマンスコストと指数関数的なメモリフットプリントが発生することに注意してください。 また、グラフィック処理の制限によって、テクスチャの最大サイズが大きく制限されます。

| -5 | -4 | -3 | -2 | -1 | 0 | +1 | +2 | +3 | +4 | +5 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 16 | 32 | 64 | 128 | 256 | <b>512</b> | 1024 | 2048 | 4096 | 8196 | 8196 |
| 64 | 128 | 256 | 512 | 1024 | <b>2048</b> | 4096 | 8196 | 8196 | 8196 | 8196 |

>[!NOTE]
>
> 解像度が16未満の場合、上限は&#x200B;*なし*&#x200B;ですが、しきい値を下回るパフォーマンスの向上はないため、これより低くすることはお勧めしません。 逆に、<b>Substanceエンジン</b>の具体的な実装が原因で、実際のパフォーマンスは&#x200B;*低下*&#x200B;します。 したがって、Substanceグラフでは、一般的な最小解像度として16 x 16を使用します。

## 継承方法を変更する

ほとんどの場合、出力サイズプロパティの既定の[継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)は、項目に応じて次のようになります。

* グラフ： *親に対する相対*
* ノード： *入力に対する相対* – ノードの[プライマリ入力](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)によって継承された値がこの場合に使用されます
* [ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノード： *絶対* - [ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)ページと[パフォーマンス最適化ガイドライン](../../best-practices/performance-optimization/performance-optimization-guidelines.md)を参照して、その理由を確認してください

ノードまたはグラフの項目をクリックしてプロパティを表示し、[プロパティ](../../interface/properties/properties.md)パネルの<b>基本パラメーター</b>セクションで<b>出力サイズ</b>プロパティを見つけます。 「継承方法」ドロップダウンメニューをクリックして、目的の継承方法を選択します。

![出力サイズの継承メソッド](../../assets/change-mode.gif "出力サイズの継承メソッド"){width="512px"}

## 問題の例

新しい[Adobe Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)をお使いの場合は、よくある問題が発生することがあります。 以下に例と解決策を示します。

+++問題1
**![（エラー）](../../assets/error.svg)問題**

![問題1](../../assets/problem2-bad.png "問題1")の例



**親サイズ**&#x200B;の設定は&#x200B;*グレー表示*&#x200B;で、グラフは望ましくない256\*256解像度で使用されています。

グラフのプロパティで、Output Sizeプロパティの継承メソッドが&#x200B;*Absolute*&#x200B;に設定されました。これにより、任意の値に優先して継承が停止されます。

**![(tick)](../../assets/check.svg)ソリューション**

![問題1の解決例](../../assets/problem2-good.png "問題1の解決例")



グラフの出力サイズの継承方法を&#x200B;*親に対して相対的*&#x200B;に設定します。

+++

+++問題2
**![（エラー）](../../assets/error.svg)問題**

![問題の例2](../../assets/problem1-bad.png "問題の例2")



上の図では、グラフが&#x200B;*親に対して相対的*&#x200B;に設定されているにもかかわらず、グラフの出力で親で設定されている解像度(512\*512)と親で設定されている解像度(1024\*1024)が異なる場合が示されています。

この問題は、[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードから発生しています。 デフォルトでは&#x200B;*絶対*&#x200B;継承メソッドに設定され、[ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)に基づく解像度として512\*512が選択されます。 このノードに接続されているノードは&#x200B;*入力に対する相対*&#x200B;に設定されているため、ビットマップノードから出力サイズを継承します。

**![(tick)](../../assets/check.svg)ソリューション**

![問題2の解決策の例](../../assets/problem1-good.png "問題2の解決策の例")



ビットマップノードの出力サイズの継承メソッドを&#x200B;*親に対して相対的*&#x200B;に設定し、チェーン内の問題を解決します。

+++

+++問題3
**![（エラー）](../../assets/error.svg)問題**

![問題3](../../assets/problem3-bad.png "問題3")の例



上記の例では、チェーンの途中で解像度がかなり高くジャンプし、結果として、親で定義されているよりもはるかに高い出力解像度が得られる問題が発生しています。

この問題は、[変換2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)ノードの相対修飾子3によって発生し、出力が8倍大きくなっています。

**![(tick)](../../assets/check.svg)ソリューション**

![問題3の解決例](../../assets/problem3-good.png "問題3の解決例")



「幅」と「Height」の相対修飾子を0に設定すると、拡大・縮小は行われません。

+++
