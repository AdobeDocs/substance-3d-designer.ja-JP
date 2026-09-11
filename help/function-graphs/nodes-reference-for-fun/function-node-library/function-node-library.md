---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/function-graphs/nodes-reference-for-function-graphs/function-node-library.html"
breadcrumb-title: ''
description: 事前定義済みのSubstance機能グラフにインスタンス化としてアクセスして、ワークフローを高速化し、機能を強化します。
helpx_creative_field: ""
helpx_description: Designer > Function graphs > Nodes reference for function graphs > Function node library
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 関数ノードライブラリ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 68fa6e85c7fe7318a4dafd491f9dc9e945a458e2
workflow-type: tm+mt
source-wordcount: '689'
ht-degree: 6%

---


# 関数ノードライブラリ

Designerでは、[アトミックノード](../../../function-graphs/nodes-reference-for-fun/atomic-function-nodes/atomic-function-nodes.md)に加えて、インスタンス化として事前定義済みのSubstance機能グラフも提供しています。 ワークフローを高速化するツールが数多く用意されており、ベクトルやカラーの操作、値のリマップ、より高度な代数の実行などのより多くの機能を利用できます。

これらのツールは、いくつかのカテゴリに分類されています。

<a name="sdf-functions"></a>

## SDF 関数

これらのノードでは、専用の&#x200B;**SDF 関数**&#x200B;パラメーターを使用して、[Shape splatter v2](../../../compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md)および[3dビューア](../../../compositing-graphs/nodes-reference-for-com/node-library/filters/effects/3d-viewer/3d-viewer.md)ノードで3Dシェイプを作成するために使用できるSDF 関数を作成できます。

>[!INFO]
> 
> SDF 関数に関する概念やワークフローについて詳しくは、専用ページ（[SDF 関数の操作](function-nodes-sdf-functions/working-with-sdf-functions.md)）を参照してください

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

### プリミティブ

[キャップ付き円錐](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capped-cone/3d-sdf-capped-cone.md)

[キャップ付き円錐（2点）](././function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capped-cone-2-points/3d-sdf-capped-cone-2-points.md)

[キャップ付きトーラス](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capped-torus/3d-sdf-capped-torus.md)

[カプセル](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-capsule/3d-sdf-capsule.md)

[円錐](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cone/3d-sdf-cone.md)

[立方体](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cube/3d-sdf-cube.md)

[円柱](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cylinder/3d-sdf-cylinder.md)

[円柱（2点）](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-cylinder-2-points/3d-sdf-cylinder-2-points.md)

[楕円体](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-ellipsoid/3d-sdf-ellipsoid.md)

[細長い円柱](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-elongated-cylinder/3d-sdf-elongated-cylinder.md)

[グランドプレーン](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-ground-plane/3d-sdf-ground-plane.md)

[らせん](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-helix/3d-sdf-helix.md)

[六角柱](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-hexagonal-prism/3d-sdf-hexagonal-prism.md)

[無限平面](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-infinite-plane/3d-sdf-infinite-plane.md)

[平面](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-plane/3d-sdf-plane.md)

[ピラミッド](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-pyramid/3d-sdf-pyramid.md)

[ピラミッド正方形](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-pyramid-square/3d-sdf-pyramid-square.md)

[ロック](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-rock/3d-sdf-rock.md)

[球面](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-sphere/3d-sdf-sphere.md)

[トーラス](./function-nodes-sdf-functions/sdf-functions-primitives/3d-sdf-torus/3d-sdf-torus.md)

</td>
<td style="border: 0;" valign="top">

### 演算子

[積集合](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-intersection/3d-sdf-op-intersection.md)

[交差のスムーズ](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-intersection-smooth/3d-sdf-op-intersection-smooth.md)

[交差サーフェス](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-intersection-surface/3d-sdf-op-intersection-surface.md)

[モーフ](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-morph/3d-sdf-op-morph.md)

[ミラーを繰り返す](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-repeat-mirror/3d-sdf-op-repeat-mirror.md)

[丸め](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-rounding/3d-sdf-op-rounding.md)

[シェル](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-shell/3d-sdf-op-shell.md)

[減算](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-subtraction/3d-sdf-op-subtraction.md)

[減算スムーズ](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-subtraction-smooth/3d-sdf-op-subtraction-smooth.md)

[対称](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-symmetry/3d-sdf-op-symmetry.md)

[和集合](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-union/3d-sdf-op-union.md)

[ユニオン面取り](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-union-chamfer/3d-sdf-op-union-chamfer.md)

[ユニオンスムーズ](function-nodes-sdf-functions/sdf-functions-operators/3d-sdf-op-union-smooth/3d-sdf-op-union-smooth.md)

</td>
<td style="border: 0;" valign="top">

### 変形

[曲げ](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-bend/3d-sdf-transform-bend.md)

[細長い](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-elongate/3d-sdf-transform-elongate.md)

[反転](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-flip/3d-sdf-transform-flip.md)

[オフセット](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-offset/3d-sdf-transform-offset.md)

[オフセットP](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-offset-p/3d-sdf-transform-offset-p.md)

[回転](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-rotate/3d-sdf-transform-rotate.md)

[P軸回転](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-rotate-p/3d-sdf-transform-rotate-p.md)

[スケール](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-scale/3d-sdf-transform-scale.md)

[ねじり](function-nodes-sdf-functions/sdf-functions-transforms/3d-sdf-transform-twist/3d-sdf-transform-twist.md)

</td>
<td style="border: 0;" valign="top">

### マテリアル

[カラーを設定](function-nodes-sdf-functions/sdf-functions-material/set-color/set-color.md)

[マテリアルIDを設定](function-nodes-sdf-functions/sdf-functions-material/set-id/set-id.md)

[マテリアルを設定](function-nodes-sdf-functions/sdf-functions-material/set-material/set-material.md)

[メタネスの設定](function-nodes-sdf-functions/sdf-functions-material/set-metalness/set-metalness.md)

[ラフネスを設定](function-nodes-sdf-functions/sdf-functions-material/set-roughness/set-roughness.md)

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<a name="comparison"></a>

## 比較

等価演算ブール値

等価浮動小数2

等価浮動小数3

等価浮動小数4

ブール値に等しくない

float2と等しくない

float3と等しくない

float4と等しくない

</td>
<td style="border: 0;" valign="top">

<a name="conversion"></a>

## 変換

[-1, 1] ～ [0, 1]

[0, 1] ～ [0, 1, 0]

[0, 1]から[-1, 1]

[0, 1] ～ [1, 0]

[a, b] ～ [0, 1]

float1へのブーリアン

度からラジアン

度から度へ

Height平衡

のこぎり波

三角波

度に変換

</td>
<td style="border: 0;" valign="top">

<a name="constant"></a>

## 定数

2 Pi

円周率

<a name="parity"></a>

## パリティ

偶数

奇数

出産回数テスト

</td>
</tr>
</table>

<a name="maths"></a>

## 数学

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

acos

asin

平均実数

平均実数2

平均実数3

平均実数4

クランプ

クロス積

クロス積vec2

距離float2

距離float3

</td>
<td style="border: 0;" valign="top">

スカラー除算float2

スカラー除算float3

スカラー除算float4

Fmod

Frac

長さfloat2

長さfloat3

float3を結合

float4を結合

vec2をノーマライズ

vec3を正規化

vec4をノーマライズ

</td>
<td style="border: 0;" valign="top">

1引く

直交vec2

リフレクト

丸いフロート1

彩度

float2を飽和

署名

滑らかさ

ステップ

浮動小数点数を切り捨てる

</td>
</tr>
</table>

<a name="color"></a>

## カラー

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

ACEScgからリニアsRGB

法線の方向

HCLからRGB

HSIからRGB

HSLオフセット

RGBにHSL

HSVからRGB

リニアsRGBからACEScg

リニアからsRGB(輝度)

リニアからsRGB

ランダムカラー

ランダムな輝度

</td>
<td style="border: 0;" valign="top">

RGBクロマ2極

六方晶RGB染色質

RGB色相2極

RGBの色相（六角形）

明度平均

明度バイヘクコーン

明度六円錐

RGB明度ルミナンスRec.601

RGB 明度ルミナンスRec.709

RGB飽和度HSI

RGB彩度HSL

RGB飽和度HSV

</td>
<td style="border: 0;" valign="top">

HCLへのRGB

HSIへのRGB

HSLのRGB

HSVRGB

sRGBからリニア(輝度)

sRGBからリニア

体温からRGBへ

ACE tonemapper

Agxトネマッパー（約）

ヘイルトネマッパー

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<a name="transformation"></a>

## 変形

デカルトを極座標に

方向オフセット

行列の反転

行列乗算

極座標から直交座標

vec2を回転

Vec2 （ラジアン）を回転

回転マトリックス

スケール行列

タイル行列

</td>
<td width="66.67%" style="border: 0;" valign="top">

<a name="random"></a>

## ランダム

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

ランダム離散[a, b]

グローバル・ランダム

[ハッシュ11](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[ハッシュ14](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[ハッシュ21](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[ハッシュ22](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[ハッシュ24](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[ハッシュ31](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

[ハッシュ32](../../../function-graphs/nodes-reference-for-fun/function-node-library/function-nodes-random/hash-functions/hash-functions.md)

</td>
<td style="border: 0;" valign="top">

正規分布

ランダムな一様&lbrack;-1, 1&lbrack;

ランダムに一様&lbrack;a, b&lbrack;

Random uniform float2 &lbrack;a, b&lbrack;

Random uniform float3 &lbrack;a, b&lbrack;

Random uniform float4 &lbrack;a, b&lbrack;

</td>
</tr>
</table>

</td>
</tr>
</table>

<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

<a name="easings"></a>

## イージング

イーズイン円

イーズイン（立方体）

イーズインエキスポ

イーズインアウト回路

イーズインアウト（立方体）

イーズインアウトexpo

イーズインアウト（四角）

イーズインアウト（四角）

イーズインアウトクォート

イーズインアウト（正弦）

イーズイン（四角）

イーズインクォート

イーズイン（濃淡）

イーズイン（正弦）

イーズアウト円

イーズアウト（立方体）

イーズアウトexpo

イーズアウト（四角）

イーズアウト（四角）

イーズアウトクイント

イーズアウト（正弦）

</td>
<td width="66.67%" style="border: 0;" valign="top">

<a name="various"></a>

## 各種

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

カーブ

非正方形の拡張UV スケール

非正方形の出力サイズ

粗さ

float 2入力を切り替える

float2 2入力を切り替え

float2 4入力の切り替え

float2 8入力の切り替え

float3 2入力を切り替え

float3 4入力の切り替え

float3 8入力の切り替え

float3 8入力の切り替え

float4 2入力の切り替え

float4 4入力の切り替え

float4 8入力の切り替え

</td>
<td style="border: 0;" valign="top">

整数 2入力の切り替え

整数 4入力の切り替え

スイッチ整数8入力

スイッチ整数2 2入力

スイッチ整数2 4入力

スイッチ整数2 8入力

スイッチ整数3 2入力

スイッチ整数3 4入力

スイッチ整数3 8入力

スイッチ整数4 2入力

スイッチ整数4 4入力

スイッチ整数4 8入力

</td>
</tr>
</table>

</td>
</tr>
</table>
