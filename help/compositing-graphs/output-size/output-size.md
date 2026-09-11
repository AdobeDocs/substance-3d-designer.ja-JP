---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/substance-compositing-graphs/output-size.html"
breadcrumb-title: ''
description: Substance合成グラフの出力サイズを設定し、テクスチャの解像度と画質を制御します。
helpx_creative_field: ""
helpx_description: Designer > Substance graphs > Output size
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 出力サイズ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 46563ec789547cc1add76655dbad02f5099927a6
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 5%

---


# 出力サイズ

グラフの<b>基本パラメーター</b>の最初のパラメーターであり、<b>出力形式</b> （ビット深度）と共に、Designer内および他のアプリケーションの両方で[公開されたSubstance 3Dアセット(SBSAR)](../publishing-asset-files/publishing-substance-3d-asset-files-sbsar.md)ファイルとして、グラフの出力に大きな影響を与えるため、このパラメーターを適切に理解することが重要です。

>[!TIP]
>
> 出力サイズプロパティを効率的に使用するための基盤として、[グラフの継承](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)について十分に理解しておくことを強くお勧めします。

>[!NOTE]
>
> ![](output-size.resources/props-output-size-lock.jpg)ロックボタンを使用して、Heightの値を幅の値と&#x200B;*一致*&#x200B;させます。

<table>
<tr style="border: 0;">
<td width="100.00%" style="border: 0;" valign="top">

## 2の累乗

出力サイズパラメーターは、グラフまたはノードによる&#x200B;*テクスチャ*&#x200B;出力の解像度を指定します。

グラフィックス処理ハードウェアが計算を行う方法によって課される何らかの制限に縛られたグラフィックス・コンピューティングのオブジェクトであるテクスチャ。 これらの制限事項の1つは、XとYのピクセル数が&#x200B;*2*&#x200B;の累乗であるイメージを表す必要があるテクスチャです。

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
> [関数グラフ](../../function-graphs/function-graphs.md)では、`$size`および`$sizelog2`の[システム変数](../../function-graphs/variables/system-variables/system-variables.md)が、ノードまたはグラフの現在の解像度に一致する浮動小数2値を、それぞれrawピクセル数または2の累乗として返します。\
> 例えば、1024\*512画像の場合、`$size`は`(1024,512)`を返し、`$sizelog2`は`(10,9)`を返します。

## 相対サイズ

Output Sizeプロパティで&#x200B;*Relative to...* [継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)が使用されている場合、その値は、継承された対数値&#x200B;*に対する修飾子*&#x200B;として表されます。

継承された解像度に関連する修飾子は、対数スケールで–12 ～ +12の範囲で指定します。デフォルトは0です。 つまり、上または下の各手順を実行すると、解像度が2倍または2分の1になります。 右の表は、継承された値が9(512 = 2^9)および11(2048 = 2^11)の場合に、ある次元で相対的な解像度がどのように変化するかを示した例です。

8196を超えると、サイズは&#x200B;*キャップ*&#x200B;になります。 この上限は、[環境設定](../../interface/preferences-window/preferences-window.md)の<b>一般</b>セクションにある<b>調理サイズ制限</b>の設定によって制御されます。 非常に大きな解像度での作業では、比例したパフォーマンスコストと指数関数的なメモリフットプリントが発生することに注意してください。 また、グラフィック処理の制限によって、テクスチャの最大サイズも大きく制限されます。

| -5 | -4 | -3 | -2 | -1 | 0 | +1 | +2 | +3 | +4 | +5 |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 16 | 32 | 64 | 128 | 256 | <b>512</b> | 1024 | 2048 | 4096 | 8196 | 8196 |
| 64 | 128 | 256 | 512 | 1024 | <b>2048</b> | 4096 | 8196 | 8196 | 8196 | 8196 |

>[!NOTE]
>
> 解像度が16未満の場合、上限は&#x200B;*なし*&#x200B;ですが、しきい値を下回るパフォーマンスの向上はないため、これより低くすることはお勧めしません。 逆に、<b>エンジン</b>の具体的な実装が原因で、実際のパフォーマンスは&#x200B;*低下*&#x200B;します。 したがって、グラフでの一般的な最小解像度として16 x 16を使用します。

## 継承方式の変更

ほとんどの場合、出力サイズプロパティの既定の[継承メソッド](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)は、項目に応じて次のようになります。

* グラフ: *親に相対的*
* ノード： *入力に対する相対* – ノードの[プライマリ入力](../../compositing-graphs/inheritance-compositing/inheritance-in-substance-compositing-graphs.md)によって継承された値がこの場合に使用されます
* [ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノード： *絶対* - [ビットマップリソース](../../resources/bitmap-resource/bitmap-resource.md)ページと[パフォーマンス最適化ガイドライン](../../best-practices/performance-optimization/performance-optimization-guidelines.md)を参照して、その理由を確認してください

ノードまたはグラフのプロパティをクリックして表示し、[プロパティ](../../interface/properties/properties.md)パネルの<b>基本パラメーター</b>セクションで<b>出力サイズ</b>プロパティを見つけます。 継承法ドロップダウンメニューをクリックし、目的の継承法を選択します。

![出力サイズの継承方法](output-size.resources/change-mode.gif "出力サイズの継承方法"){width="512px"}

## 問題の例

新しい[Adobe Substance 3D Designer](https://www.adobe.com/jp/products/substance3d-designer.html)をお使いの場合は、よくある問題が発生することがあります。 以下に例と解決策を示します。

+++問題1
**![（エラー）](output-size.resources/error.svg)問題**

![問題1](output-size.resources/problem2-bad.png "問題1")の例



**親サイズ**&#x200B;の設定は&#x200B;*グレー表示*&#x200B;で、グラフは望ましくない256\*256解像度で使用しています。

グラフのプロパティで、Output Sizeプロパティの継承メソッドが&#x200B;*Absolute*&#x200B;に設定されました。これにより、任意の値を優先して継承が停止されます。

**![(tick)](output-size.resources/check.svg)ソリューション**

![問題1の解決例](output-size.resources/problem2-good.png "問題1の解決例")



グラフの出力サイズの継承方式を&#x200B;*親に相対的*&#x200B;に設定します。

+++

+++問題2
**![（エラー）](output-size.resources/error.svg)問題**

![問題の例2](output-size.resources/problem1-bad.png "問題の例2")



上の図は、グラフーが&#x200B;*親に相対的*&#x200B;に設定されていても、グラフーの出力の解像度(512\*512)が親(1024\*1024)の設定と異なる場合を示しています。

この問題は、[ビットマップ](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/bitmap/bitmap.md)ノードから発生しています。 デフォルトでは&#x200B;*Absolute*&#x200B;継承方式に設定され、[Bitmapリソース](../../resources/bitmap-resource/bitmap-resource.md)に基づく解像度として512\*512が選択されています。 このノードに接続されているノードは&#x200B;*入力に対する相対*&#x200B;に設定されているため、ビットマップノードから出力サイズを継承します。

**![(tick)](output-size.resources/check.svg)ソリューション**

![問題2の解決策の例](output-size.resources/problem1-good.png "問題2の解決策の例")



ビットマップノードの出力サイズの継承方式を&#x200B;*親に相対的*&#x200B;に設定し、チェーン内の問題を解決します。

+++

+++問題3
**![（エラー）](output-size.resources/error.svg)問題**

![問題3](output-size.resources/problem3-bad.png "問題3")の例



上記の例では、チェーンの途中で解像度がかなり高くジャンプし、結果として、親で定義されているよりもはるかに高い出力解像度が得られる問題が発生しています。

この問題は、[変形 2D](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/transformation-2d/transformation-2d.md)ノードの相対修飾子3が原因で、出力が8倍大きくなっています。

**![(tick)](output-size.resources/check.svg)ソリューション**

![問題3の解決例](output-size.resources/problem3-good.png "問題3の解決例")



「幅」と「Height」の相対修飾子を0に設定すると、拡大・縮小は行われません。

+++
