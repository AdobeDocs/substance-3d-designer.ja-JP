---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/glslfx-shaders.html"
breadcrumb-title: ''
description: Substance 3D Designer 3DビューでGLSLFXシェーダを使用して、マテリアルレンダリングとプレビュー効果をカスタマイズします。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > GLSLFX Shaders
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: GLSLFXシェーダ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '3098'
ht-degree: 1%

---


# GLSLFXシェーダ

GLSLFXファイルは、アプリケーションとglslシェーダファイルの間のブリッジを作成します。\
これにより、コードを変更することなく、任意のglslシェーダを使用できます。

## ファイル形式

GLSLFXファイル形式はXMLファイルです。 コメントはサポートされています。

### ヘッダーおよびルートノード

XMLルートノード要素の名前は<b>glslfx</b>です。

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->

</glslfx>
```


### Body

#### テクニック

テクニックを説明するXMLエレメント。 技術は、電流FXの変化である。 GLSLFXには複数のテクニックを含めることができますが、少なくとも1つのテクニックを定義する必要があります。

ジオメトリは、アプリケーションで定義されたいずれかの手法を使用してレンダリングされます。

+++XML要素定義
<b>名前：</b>のテクニック

<b>属性：</b>

* name：手法に名前を付けるために使用される文字列

+++

XML要素には複数の子を含めることができます。 手法で定義されたエレメントは、グローバルに定義されたエレメントをオーバーライドします。

例えば、一部のユニフォームの値をオーバーライドし、このテクニックのFXバリエーションを取得するために使用されます。

#### レンダーパス

レンダーパスを記述するXML要素。 レンダーパスは、ジオメトリのレンダリングを表します。

テクニックには、順番に実行される複数のレンダーパスを含めることができます。 レンダーパスを含まないテクニックは、「オンスクリーン」レンダーパスを含むテクニックと同等です。

レンダーパスで定義されたエレメントは、親のテクニックで定義されたエレメントをオーバーライドします。

+++XML要素定義
<b>名前：</b>パス

<b>属性：</b>

* 出力

* オフスクリーン：レンダリングはユーザー定義のレンダリングターゲットに対して実行されます

* 画面：レンダリングはデフォルトのレンダーターゲットに行われます

+++

#### シェーダー

タイプごとにGLSLシェーダファイルを設定します。

XML要素定義：

+++XML要素定義
<b>名前：</b>シェーダー

<b>属性：</b>

* タイプ： GLSLシェーダタイプ；

* filename: glslシェーダーファイルのパス。 GLSLFXファイルに対する絶対または相対パスで指定できます。

* primitiveType:プリミティブをレンダリングするメソッドです。


| &#39;type&#39;値 | 説明 |
| --- | --- |
| 頂 | 頂点シェーダ |
| 幾何学 | ジオメトリシェーダ |
| tess\_control | テッセレーションコントロールシェーダ |
| tess\_eval | テッセレーション評価シェーダ |
| フラグメント | フラグメントシェーダ |



| &#39;primitiveType&#39;値 | 説明 |
| --- | --- |
| ポイント | ポイントとしてレンダリング |
| lineloop | 線ループとしてレンダリング |
| patch[1..N] | [1..N]頂点を持つパッチとしてレンダリングする |


+++

#### プロパティ

OpenGLステートの一部を設定できるようにします。

+++XML要素定義
<b>Name:</b>プロパティ

<b>属性：</b>

* name：設定するプロパティの名前。 この名前は、OpenGL関数またはglEnum名に基づいています。
  * 構文を列挙します：小文字で&#39;GL\_&#39;接頭辞を付けません。 例： glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;
  * 関数の構文： &#39;gl&#39;接頭辞なし、小文字なし、すべての単語を&#39;\_&#39;文字で区切る。 例： glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* 構文を列挙します：小文字で&#39;GL\_&#39;接頭辞を付けません。 例： glEnable(GL\_BLEND\_ENABLE) => &quot;&quot;, glDisable(GL\_CULL\_FACE) => &quot;&quot;

* 関数の構文： &#39;gl&#39;接頭辞なし、小文字なし、すべての単語を&#39;\_&#39;文字で区切る。 例： glBlendFunc(GL\_SRC\_ALPHA, GL\_ONE\_MINUS\_SRC\_ALPHA) => &quot;&quot;

* value:プロパティの値です。


| 「名前」値 | 「値」値 | 説明 |
| --- | --- | --- |
| blend\_enabled | ブール値 | 描画モードを有効/無効にする |
|  | true |  |
|  | 擬似 |  |
| blend\_func | 文字列、文字列 | ソースと出力先のブレンド機能の設定 |
|  | ゼロ | OpenGL列挙GL\_ZERO |
|  | 1 | （OpenGL列挙GL\_ONE用） |
|  | src\_color | OpenGL列挙GL\_SRC\_COLOR用 |
|  | one\_minus\_src\_color | OpenGL enumの場合： GL\_ONE\_MINUS\_SRC\_COLOR |
|  | dst\_color | OpenGL列挙GL\_DST\_COLORの場合 |
|  | one\_minus\_dst\_color | OpenGL enumの場合： GL\_ONE\_MINUS\_DST\_COLOR |
|  | src\_alpha | OpenGL列挙GL\_SRC\_ALPHA |
|  | one\_minus\_src\_alpha | OpenGL enumの場合： GL\_ONE\_MINUS\_SRC\_ALPHA |
|  | dst\_α | OpenGL列挙GL\_DST\_ALPHA |
|  | one\_minus\_dst\_alpha | OpenGL enumの場合： GL\_ONE\_MINUS\_DST\_ALPHA |
|  | constant\_color | OpenGL列挙GL\_CONSTANT\_COLOR用 |
|  | one\_minus\_constant\_color | OpenGL enumの場合： GL\_ONE\_MINUS\_CONSTANT\_COLOR |
|  | constant\_alpha | OpenGL列挙GL\_CONSTANT\_ALPHA |
|  | one\_minus\_constant\_alpha | OpenGL enumの場合： GL\_ONE\_MINUS\_CONSTANT\_ALPHA |
|  | src\_alpha\_saturate | OpenGL enumの場合： GL\_SRC\_ALPHA\_SATURATE |
|  | src1\_color | OpenGL列挙GL\_SRC1\_COLOR用 |
|  | one\_minus\_src1\_color | OpenGL enumの場合： GL\_ONE\_MINUS\_SRC1\_COLOR |
|  | src1\_alpha | OpenGL列挙GL\_SRC1\_ALPHA |
|  | one\_minus\_src1\_alpha | OpenGL enumの場合： GL\_ONE\_MINUS\_SRC1\_ALPHA |
| curl\_面\_enabled | ブール値 | 面カリングを有効/無効にする |
|  | true |  |
|  | 擬似 |  |
| curl\_face\_mode | 文字列 | 面のカリングモードの設定 |
|  | 前面 | OpenGL列挙GL\_FRONT用 |
|  | 裏 | OpenGL列挙GL\_BACKの場合 |
|  | front\_and\_back | OpenGL enumの場合： GL\_FRONT\_AND\_BACK |
| 深度\_func | 文字列 | 深度比較機能の設定 |
|  | しない | （OpenGL列挙GL\_NEVER） |
|  | 少なく | OpenGL列挙GL\_LESSの場合 |
|  | しとめ | OpenGL列挙GL\_LEQUAL |
|  | 等しい | OpenGL列挙GL\_EQUALの場合 |
|  | notequal | OpenGL列挙GL\_NOTEQUAL |
|  | gequal | OpenGL列挙GL\_GEQUAL |
|  | より大 | OpenGL列挙GL\_GREATER |
|  | 常に | OpenGL列挙GL\_ALWAYSの場合 |


+++

#### 制服

グローバルまたは親のテクニックで定義された一部のユニフォームをオーバーライドできるようにします。 これにより、このテクニックまたはレンダーパスのシェーダーの動作を変更できます。

定義について詳しくは、以下の<b>制服</b>のセクションを参照してください。

+++例


+++

## レンダーターゲット

「オフスクリーン」レンダーパスの場合、レンダーターゲットをレンダーパスで定義する必要があります。

+++XML要素定義
<b>名前：</b>の出力

<b>属性：</b>

* attachment: OpenGLの名前から着想を得たOpenGLのアタッチメントポイント。\
  GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
  GL\_深度\_ATTACHMENT => &#39;深度&#39;

attachment: OpenGLの名前から着想を得たOpenGLのアタッチメントポイント。\
GL\_COLOR\_ATTACHMENT[0..3] => &#39;color[0..3]&#39;\
GL\_深度\_ATTACHMENT => &#39;深度&#39;

* 名前：レンダーターゲットの名前です。\
  後のレンダーパスでこのレンダーターゲットをサンプラーとしてバインドするために使用できます。

名前：レンダーターゲットの名前です。\
後のレンダーパスでこのレンダーターゲットをサンプラーとしてバインドするために使用できます。

* 形式：レンダーターゲットの内部形式です。

形式：レンダーターゲットの内部形式です。

* clear: clear値を定義するオプション属性です。\
  存在する場合、レンダーターゲットはレンダーパスの開始時にこの値までクリアされます。\
  見つからない場合、レンダーターゲットは以前のコンテンツを保持します。

+++

>[!NOTE]
>
> 画面上のレンダーパスではカラーレンダーターゲットの使用は禁止されていますが、深度のレンダーターゲットは任意のレンダーパスで共用できます（ただし、シーンで複数のマテリアルをミックスすると、レンダリングが壊れる可能性があります）。

<b>形式について</b>

深度形式の場合、すべての深度のみ（ステンシルなし）のOpenGL形式がサポートされます。

* GL\_深度\_COMPONENT16 => &#39;深度26&#39;
* GL\_深度\_COMPONENT24 => &#39;深度34&#39;
* GL\_深度\_COMPONENT32 => &#39;深度42&#39;
* GL\_深度\_COMPONENT32F => &#39;深度42f&#39;

カラー形式の場合、名前はOpenGLの列挙名に基づいており、小文字の「GL\_」接頭辞は付きません。\
3つのチャンネル形式(RGB)はサポートされていません。代わりにRGBA形式を使用してください。\
サポートされているチャンネルごとのビット深度:

* 正規化された符号なし整数: 8、16
* 浮動小数点： 16、32

これらのルールの例外は、サポートされているGL\_R11F\_G11F\_B10F形式です。

* GL\_RGBA8 => &#39;rgba8&#39;
* GL\_RGBA16F => &#39;rgba16f&#39;
* GL\_SRGB8\_ALPHA8 => &#39;srgb8\_alpha8&#39;
* GL\_R11F\_G11F\_B10F => &#39;r11f\_g11f\_b10f&#39;
* GL\_RG16 => &quot;rg16&quot;

### サンプラ

グローバルに定義されている一部のサンプラーをオーバーライドできます。テクニックで定義することはできません。 これにより、このレンダーパスのサンプラーの使用法を定義したり、前のレンダーパスのレンダーターゲットから読み取ることができます。

定義の詳細については、<b>サンプラー</b>セクションを参照してください。

+++例


+++

## 入力頂点の形式

これにより、シェーダーで定義される各属性のセマンティックを定義できます。

<b>XML要素定義：</b>

名前： &#39;vertexformat&#39;

属性 :

* &#39;name&#39;：頂点シェーダで定義されたアトリビュートの名前です。
* &#39;semantic&#39;：属性のセマンティック。

| 「意味的」値 | 説明 |
| --- | --- |
| 位置 | 頂点の位置(float3) |
| 法線 | 頂点法線(float3) |
| textcoord[0..N] | テクスチャ座標バッファーN (float2) |
| 正接[0..N] | 正接バッファーN(float4) |
| 従法線[0..N] | 従法線バッファーN(float4) |

例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- INPUT VERTEX FORMAT -->

     <vertexformat name="iVS_Position" semantic="position"/>

     <vertexformat name="iVS_Normal" semantic="normal"/>

     <vertexformat name="iVS_UV" semantic="texcoord0"/>

     <vertexformat name="iVS_Tangent" semantic="tangent0"/>

     <vertexformat name="iVS_Binormal" semantic="binormal0"/>

</glslfx>
```


## サンプラ

これにより、各サンプラーの使用方法を定義できます。\
これは、アプリケーションが、指定されたサンプラーに設定するテクスチャを認識するために使用します。

<b>XML要素定義：</b>

名前： &#39;sampler&#39;

属性 :

* &#39;name&#39;: シェーダーファイル内のsampler変数の名前です。
* &#39;usage&#39;:サンプラーの使用方法。 これは、グラフの出力ノードで指定された使用方法と一致します。

| &#39;usage&#39;値 | 説明 |
| --- | --- |
| 拡散 | Diffuse地図 |
| 不透明 | 不透明度マップ |
| 発光 | Emissive地図 |
| 環境閉塞 | Ambient occlusion地図 |
| 周囲 | アンビエントマップ |
| マスク | マスクマップ |
| 詳細正常 | 詳細法線マップ |
| 法線 | 法線マップ |
| マイクロ | バンプマップ |
| 高さ | Height地図 |
| ディスプレイスメント | ディスプレイスメント地図 |
| specularlevel | Specular level地図 |
| specularcolor | Specularカラーマップ |
| 反射 | Specular地図 |
| 光沢 | 光沢マップ |
| ラフネス | ラフネス地図 |
| 異方性ピレベル | 異方性レベルの地図 |
| 異方性ピアングル | 異方性の角度マップ |
| transmissive | 透過地図 |
| 反射 | 反射マップ |
| 屈折 | 屈折マップ |
| 環境 | 環境マップ（立方体マップ） |
| パノラマ | パノラマの地図（緯度・経度の地図） |
| bluenoisemask | 256 x 256のディザリングテクスチャ |

* 複数の用途がサポートされています。
  * 例：

```
   <!-- SAMPLERS -->

    <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <!-- ... -->
```


&#39;isHidden&#39;:サンプラーをGUIに表示するかどうかを示すブーリアン

* 例：

```
     <!-- SAMPLERS -->

    <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <!-- ... -->
```


ラッピングモード：

<table data-preserve-html="true"><tbody><tr><th>名前</th><th>値</th></tr><tr><td rowspan="4">テクスチャ_ラップ_s、テクスチャ_ラップ_t、テクスチャ_ラップ_r<br/><br/><br/></td><td>clamp_to_edge</td></tr><tr><td>clamp_to_border</td></tr><tr><td colspan="1">mirrored_repeat</td></tr><tr><td colspan="1">繰り返し<br/><br/></td></tr></tbody></table>

テクスチャフィルター

<table data-preserve-html="true"><tbody><tr><th>名前</th><th>値</th></tr><tr><td rowspan="6">テクスチャ_min_filter, テクスチャ_mag_filter<br/><br/><br/></td><td>nearest</td></tr><tr><td>線形</td></tr><tr><td colspan="1">nearest_ミップマップ_nearest</td></tr><tr><td colspan="1">linear_ミップマップ_nearest</td></tr><tr><td colspan="1">nearest_ミップマップ_linear</td></tr><tr><td colspan="1">linear_ミップマップ_リニア</td></tr></tbody></table>

例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- SAMPLERS -->

     <sampler name="baseColorMap" usage="basecolor,diffuse"/>

     <sampler name="heightMap" usage="height"/>

     <sampler name="normalMap" usage="normal"/>

     <sampler name="detailNormalMap" usage="detailNormal"/>

     <sampler name="environmentMap" usage="environment"/>

     <sampler name="bluenoiseMask" usage="bluenoisemask" ishidden="true"/>

     <sampler name="sssDiffuseMap" usage="sssDiffuse"/>

</glslfx>
```


## 制服

これにより、各シェーダー制服に関する補足情報を入力できます。

<b>XML要素定義：</b>

名前： &#39;uniform&#39;

属性 :

&#39;name&#39;: シェーダーファイル内のユニフォームの名前です。

| 「意味的」値 | 説明 |
| --- | --- |
| ワールド | ワールド行列(float16) |
| worldinversetranspose | ワールド逆転位行列(float16) |
| worldviewprojection | ワールドビュー投影行列(float16) |
| viewinverse | ワールド逆行列(float16) |
| worldview | ワールド表示行列(float16) |
| modelview | モデルビュー行列(float16) |
| 投影 | 射影行列(float16) |
| 周囲 | シーンの周囲光カラー(float3) |
| lightposition[0..N] | シーンのN番目のライトの位置(float3) |
| lightcolor[0..N] | シーンのN番目のライトのカラー(float3) |
| lightintensity[0..N] | シーンのN番目のライトの強度（浮動小数点） |
| globaltime | 現在の時間（秒単位） |
| 解決策 | ビューポート解像度(int2) |
| マウス | マウスの位置(int2) |
| samplespostablesize | 環境照明(int)の計算に使用するサンプルの数 |
| irradianceshcoefs | 球面高調波ベクトルの配列(float3[10]) |
| panoramipmapheight | パノラママップのミップマップレベル数（浮動小数点） |
| パノラマ変換 | 角度パノラママップの回転角度(float) |
| パノラマ性 | パノラママップの強度（浮動小数点） |
| computebinormalinfragmentshader | バイナリはフラグメントごとに計算されますか？ （頂点でない場合は頂点ごと） (bool) |
| isdirectxnormal | DirectXですか？ (bool) |
| uvwscale | u、v、wのスケール値(float3) |
| renderuvtile | 1つのUVタイルのみをレンダリングしますか？ (bool) |
| uvtilecoords | レンダリングするUVタイル座標(int2) |

「セマンティック」：制服のセマンティック。 （すべての行列はfloat16です）。

例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

     <!-- BODY -->

     <!-- ... -->



     <!-- MATRICES -->

     <uniform name="worldMatrix" semantic="world"/>

     <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

     <uniform name="worldViewMatrix" semantic="worldview"/>

     <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

     <uniform name="viewInverseMatrix" semantic="viewinverse"/>

     <uniform name="modelViewMatrix" semantic="modelview"/>

     <uniform name="projectionMatrix" semantic="projection"/>

</glslfx>
```


例：

```
<?xml version="1.0" encoding="UTF-8"?>

<glslfx version="1.0.0" author="allegorithmic.com">

    <!-- BODY -->

    <!-- ... -->



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>

</glslfx>
```


### その他のパラメーター

その他の追加情報は、各制服に次の目的で追加できます。

* デフォルト値の定義
* クランプ値
* アプリケーションでの制服の表示方法を制御します。
* ラベルを設定
* アプリケーションで値の編集に使用するウィジェット情報を設定します。
* ウィジェット名、最小、最大、増分/減分ステップ
* グループウィジェットのグループユニフォーム

制服は各テクニックに対して上書きできるため、各テクニックに対して特定のGUI設定を表示できます。

<b>XML要素定義：</b>

名前： &#39;uniform&#39;

属性 :

* &#39;name&#39;: シェーダーファイル内のユニフォームの名前です。
* &#39;default&#39;：均一の既定値
* &#39;min&#39;：有効範囲の最小値
* &#39;max&#39;：有効範囲の最大値
* &#39;guiName&#39;:アプリケーションのGUI内のユニフォームの名前
* &#39;guiGroup&#39;:アプリケーションのGUIにユニフォームを配置するグループの名前
* &#39;guiWidget&#39;:アプリケーションのGUIで一様な値を編集するために使用されるウィジェットの名前

| &#39;guiWidget&#39;値 | 説明 |
| --- | --- |
| スライダー | floatNのスライダーウィジェット |
| 角度 | フロートの角度ウィジェット |
| カラー | float3、float4カラーのカラーウィジェット |
| checkbox | boolのCheckBoxウィジェット |

* &#39;guiMin&#39;:ウィジェットの最小値
* &#39;guiMax&#39;:ウィジェットの最大値

## 例： Tessellation/Parallax

### 視差頂点シェーダーファイル

場所： .\tessellation\_parallax\parallax\vs.glsl

コンテンツ：

> #version 120

属性vec4 iVS\_Position;\
属性vec4 iVS\_Normal;\
アトリビュートvec2 iVS\_UV;\
属性vec4 iVS\_Tangent;\
属性vec4 iVS\_Binormal;

vec3 iFS\_Normalの変更；\
可変vec2 iFS\_UV;\
vec3 iFS\_Tangent;\
vec3 iFS\_Binormal;\
vec3 iFS\_PointWSの変更；

均一mat4 worldMatrix;\
均一mat4 worldViewProjMatrix;

void main()\
{\
gl\_Position = worldViewProjMatrix \&#42; iVS\_Position;\
iFS\_Normal = iVS\_Normal.xyz;\
iFS\_UV = iVS\_UV;\
iFS\_Tangent = iVS\_Tangent.xyz;\
iFS\_従法線 = iVS\_従法線.xyz;\
iFS\_PointWS = (worldMatrix \&#42; iVS\_Position).xyz;\
}

### テッセレーション頂点シェーダファイル

場所： .\tessellation\_parallax\tessellation\vs.glsl

コンテンツ：

>> 

#version 120

属性vec4 iVS\_Position;\
属性vec4 iVS\_Normal;\
アトリビュートvec2 iVS\_UV;\
属性vec4 iVS\_Tangent;\
属性vec4 iVS\_Binormal;

vec4 oVS\_Normalの変更；\
vec2 oVS\_UVの変更；\
vec4 oVS\_正接の変更；\
vec4 oVS\_従法線の変更；

void main()\
{\
gl\_Position = iVS\_Position;\
oVS\_Normal = iVS\_Normal;\
oVS\_UV = iVS\_UV;\
oVS\_正接 = iVS\_正接;\
oVS\_従法線 = iVS\_従法線;\
}

### テセレーション制御シェーダーファイル

場所： .\tessellation\_parallax\tessellation\tcs.glsl

コンテンツ：

>> 

#version 400コア\
#extension GL\_ARB\_tessellation\_shader ：有効にする

layout(vertices = 3) out;

in vec4 oVS\_Normal[];\
in vec2 oVS\_UV[];\
in vec4 oVS\_Tangent[];\
in vec4 oVS\_Binormal[];

out vec4 oTCS\_Normal[];\
out vec2 oTCS\_UV[];\
out vec4 oTCS\_Tangent[];\
out vec4 oTCS\_Binormal[];

均一フローティングテッセレーション係数；

void main()\
{\
gl\_TessLevelOuter[0] = tessellationFactor;\
gl\_TessLevelOuter[1] = tessellationFactor;\
gl\_TessLevelOuter[2] = tessellationFactor;\
gl\_TessLevelInner[0] = tessellationFactor;\
gl\_out[gl\_InvocationID].gl\_Position = gl\_in[gl\_InvocationID].gl\_Position;

oTCS\_Normal[gl\_InvocationID] = oVS\_Normal[gl\_InvocationID];\
oTCS\_UV[gl\_InvocationID] = oVS\_UV[gl\_InvocationID];\
oTCS\_Tangent[gl\_InvocationID] = oVS\_Tangent[gl\_InvocationID];\
oTCS\_Binormal[gl\_InvocationID] = oVS\_Binormal[gl\_InvocationID];\
}

### テッセレーション評価シェーダファイル

場所： .\tessellation\_parallax\tessellation\tcs.glsl

コンテンツ：

>> 

#version 400コア

layout(triangles, equal\_spacing, ccw) in;

in vec4 oTCS\_Normal[];\
in vec2 oTCS\_UV[];\
in vec4 oTCS\_Tangent[];\
vec4 oTCS\_従法線[];

均一mat4 worldMatrix;\
均一mat4 worldViewProjMatrix;

uniform sampler2D heightMap;

均等浮動小数タイリング= 1.0f;\
uniform float heightMapScale = 1.0f;

out vec3 iFS\_Normal;\
vec2 iFS\_UV出力；\
vec3 iFS\_正接を出力します。\
vec3 iFS\_Binormal;\
vec3 iFS\_PointWSを出力しました。

vec3 interpolate3D(vec3 v0, vec3 v1, vec3 v2, vec3 uvw)\
{\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
}

vec2 interpolate2D(vec2 v0, vec2 v1, vec2 v2, vec3 uvw)\
{\
return uvw.x \&#42; v0 + uvw.y \&#42; v1 + uvw.z \&#42; v2;\
}

void main()\
{\
vec3 uvw = gl\_TessCoord.xyz;

vec3 newPos = interpolate3D(gl\_in[0].gl\_Position.xyz, gl\_in[1].gl\_Position.xyz, gl\_in[2].gl\_Position.xyz, uvw);\
vec3 newNormal = normalize(interpolate3D(oTCS\_Normal[0].xyz, oTCS\_Normal[1].xyz, oTCS\_Normal[2].xyz, uvw));\
vec3 newTangent = normalize(interpolate3D(oTCS\_Tangent[0].xyz, oTCS\_Tangent[1].xyz, oTCS\_Tangent[2].xyz, uvw));\
vec3 newBinormal = normalize(interpolate3D(oTCS\_Binormal[0].xyz, oTCS\_Binormal[1].xyz, oTCS\_Binormal[2].xyz, uvw));\
vec2 newUV = interpolate2D(oTCS\_UV[0], oTCS\_UV[1], oTCS\_UV[2], uvw);

float heightTexSample = texture（heightMap, newUV \&#42;タイリング）.x \&#42; 2.0 - 1.0;\
newPos += newNormal \&#42; heightTexSample \&#42; heightMapScale;

vec4 obj\_pos = vec4(newPos, 1);\
gl\_Position = worldViewProjMatrix \&#42; obj\_pos;

iFS\_UV = newUV \&#42;タイリング；\
iFS\_Tangent = newTangent;\
iFS\_Binormal = newBinormal;\
iFS\_Normal = newNormal;\
iFS\_PointWS = (worldMatrix \&#42; obj\_pos).xyz;\
}

### フラグメントシェーダーファイル

場所： .\tessellation\_parallax\fs.glsl

コンテンツ：

>> 

#version 120

// #define ALG\_NORMAL\_DIRECTX\
#define ALG\_NORMAL\_OPENGL

#ifdef ALG\_NORMAL\_DIRECTX\
// #define FLIP\_NORMAL\_X\
#define FLIP\_NORMAL\_Y\
// #define FLIP\_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_DIRECTX

#ifdef ALG\_NORMAL\_OPENGL\
// #define FLIP\_NORMAL\_X\
#define FLIP\_NORMAL\_Y\
// #define FLIP\_NORMAL\_Z\
#endif //#ifdef ALG\_NORMAL\_OPENGL

vec3 iFS\_Normalの変更；\
可変vec2 iFS\_UV;\
可変vec3 iFS\_正接;\
可変vec3 iFS\_従法線;\
vec3 iFS\_PointWSの変更；

均一vec3 Lamp0Pos = vec3(0.0f,0.0f,70.0f);\
均一vec3 Lamp0Color = vec3(1.0f,1.0f,1.0f);\
均一vec3 Lamp1Pos = vec3(70.0f,0.0f,0.0f);\
uniform vec3 Lamp1Color = vec3(0.198f,0.198f,0.198f);\
uniform bool flipNormal = true;\
uniform float TilingDetail = 3.0f;\
uniform float SpecExpon = 50.0;\
均一フロートKs = 1.0;\
uniform int parallax\_mode = 0;\
uniform float tessellationFactor = 4.0;\
uniform float heightMapScale = 1.0f;\
均一フロート深度\_detail = 0.5f;\
均一フロートKr = 0.5f;\
uniform int KF\_on = 1;\
均一フロートKF = 1.0f;\
uniform vec3 AmbiColor = vec3(0.07f,0.07f,0.07f);\
均一フロートタイリング= 1.0f;\
uniform int enableTilingInFS = 0;

uniform sampler2D heightMap;\
uniform sampler2D normalMap;\
uniform sampler2D detailNormalMap;\
uniform sampler2D emissiveMap;\
uniform sampler2D diffuseMap;\
uniform sampler2D specularMap;\
uniform sampler2D opacityMap;\
uniform samplerCube environmentMap;

均一mat4 worldMatrix;\
均一mat4 worldInverseTransposeMatrix;\
均一mat4 viewInverseMatrix;

vec4 litFct(float NdotL、float NdotH、float specExp)\
{\
float ambient = 1.0;\
float diffuse = max(NdotL, 0.0);\
float Specular = step(0.0, NdotL) \&#42; pow(max(0.0, NdotH), specExp);\
return vec4(ambient, diffuse, Specular, 1.0);\
}

vec3 lerpFct(vec3 v0, vec3 v1, float percent)\
{\
return v0 + (v1-v0) \&#42; percent;\
}

//フォンシェーディング\
void phong\_シェーディング(\
vec3 LightColorでは、\
vec3 normalWSでは、\
vec3 pointToLightDirWSでは、\
vec3 pointToCameraDirWSでは、\
vec3 DiffuseContribを見つけます。\
inout vec3 SpecularContrib)\
{\
vec3 Hn = normalize(pointToCameraDirWS + pointToLightDirWS);\
vec4 litV = litFct(dot(normalWS, pointToLightDirWS), dot(normalWS, Hn), SpecExpon);\
DiffuseContrib = litV.y \&#42; LightColor;\
SpecularContrib = litV.y \&#42; litV.z \&#42; Ks \&#42; LightColor;\
}

vec3 fixNormalSample(vec3 v)\
{\
vec3結果= v - vec3(0.5,0.5,0.5);

#ifdef FLIP\_NORMAL\_X\
result.x = -result.x;\
#endif // ifdef FLIP\_NORMAL\_X\
#ifdef FLIP\_NORMAL\_Y\
result.y = -result.y;\
#endif // ifdef FLIP\_NORMAL\_Y\
#ifdef FLIP\_NORMAL\_Z\
result.z = -result.z;\
#endif // ifdef FLIP\_NORMAL\_Z

結果を返す。\
}

vec3 normalVecOSToWS(vec3 normal)\
{\
return normal;\
}

void main()\
{\
vec3 cameraPosWS = viewInverseMatrix[3].xyz;\
vec3 pointToLight0DirWS = normalize(Lamp0Pos - iFS\_PointWS);\
vec3 pointToLight1DirWS = normalize(Lamp1Pos - iFS\_PointWS);\
vec3 pointToCameraDirWS = normalize(cameraPosWS);\
vec3 normalOS = normalize(iFS\_Normal);\
vec3 tangentOS = normalize(iFS\_正接);\
vec3 binormalOS = normalize(iFS\_従法線);

// ------------------------------------------\
// TBNが直交化されていることを確認します\
binormalOS = normalize(cross(normalOS, tangentOS));\
tangentOS = normalize(cross(binormalOS, normalOS));

vec3 cumulatedNormalOS = normalOS;

// ------------------------------------------\
// UVを更新\
float a = dot(normalOS,-pointToCameraDirWS);\
vec3 s = vec3(dot(pointToCameraDirWS,tangentOS), dot(pointToCameraDirWS,binormalOS), a);\
vec2 uv = enableTilingInFS == 0 ? iFS\_UV : (iFS\_UV \&#42; タイリング);\
浮動小数点Height= テクスチャ 2D(heightMap,uv).x \&#42; 2.0 - 1.0 ;\
float parallax = parallax\_mode == 0 ? (tessellationFactor / 100000.f + heightMapScale / 500.f) : (heightMapScale / 50.f);\
uv += （Height \&#42; s.xy \&#42;視差） ;

// ------------------------------------------\
// normalMapから法線を追加\
vec3 normalTS = テクスチャ2D(normalMap,uv).xyz;\
normalTS = fixNormalSample(normalTS);\
vec3 normalMapOS = normalTS.x\&#42;tangentOS + normalTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalMapOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

// ------------------------------------------\
//詳細ノーマルマップを追加\
vec3 normalDetailTS = テクスチャ 2D(detailNormalMap,uv\&#42;TilingDetail).xyz;\
normalDetailTS = fixNormalSample(normalDetailTS);\
vec3 variableNormalDetailTS = lerpFct(vec3(0.0,0.0,0.5),normalDetailTS,深度\_detail);\
vec3 normalDetailOS = variableNormalDetailTS.x\&#42;tangentOS + variableNormalDetailTS.y\&#42;binormalOS;\
cumulatedNormalOS = cumulatedNormalOS + normalDetailOS;\
cumulatedNormalOS = normalize(cumulatedNormalOS);

if (length(normalTS)&lt;0.0001)\
cumulatedNormalOS = normalOS;

vec3 cumulatedNormalWS = normalVecOSToWS(cumulatedNormalOS);

// ------------------------------------------\
// DiffuseとSpecularを計算

//ライト0の貢献度\
vec3 diffContrib = vec3(0, 0, 0);\
vec3 specContrib = vec3(0, 0, 0);\
phong\_シェーディング(Lamp0Color, cumulatedNormalWS, pointToLight0DirWS, pointToCameraDirWS, diffContrib, specContrib);

//ライト1の貢献度\
vec3 diffContrib2 = vec3(0, 0, 0);\
vec3 specContrib2 = vec3(0, 0, 0);\
phong\_シェーディング(Lamp1Color, cumulatedNormalWS, pointToLight1DirWS, pointToCameraDirWS, diffContrib2, specContrib2);

diffContrib += diffContrib2;\
specContrib += specContrib2;

vec4 diffuseColor = テクスチャ2D(diffuseMap,uv);

vec3 specularColor = テクスチャ2D(specularMap,uv).rgb;\
vec3 R = reflect(pointToCameraDirWS,cumulatedNormalWS);\
vec3 reflColor = Kr \&#42; textureCube(environmentMap,R.xyz).bgr;

float FallofRefl;

if (KF >= 0.0)\
FallofRefl = max((1-dot(pointToCameraDirWS/(KFs),cumulatedNormalWS)),0)\&#42;KF\_on;\
else\
FallofRefl = (1-max((1-dot(pointToCameraDirWS/(-KFs),cumulatedNormalWS)),0)\&#42;KF\_on;

if (KF\_on == 0)\
FallofRefl=1.0;

vec3 Ambiant\_final = diffuseColor.rgb\&#42;AmbiColor;

// ------------------------------------------\
vec3 emissive = テクスチャ2D(emissiveMap,uv).xyz;

vec3 finalcolor = Ambiant\_final\
+ specularColor\&#42;specContrib\
+ diffuseColor.rgb\&#42;diffContrib\
+ (reflColor\&#42;specularColor\&#42;FallofRefl)\
+放射；

//最終的なカラー\
vec4 finalColor4 = vec4(finalcolor, texture2D(opacityMap,uv));

gl\_FragColor = finalColor4;\
}

### GLSLFXファイル

glslfxファイルは、ジオメトリをレンダリングする2つのテクニックを定義します。

* 1つはハードウェアのテッセレーション技術を使う
* もう1つは、ユーザハードウェアがテッセレーションをサポートしていない場合にフォールバックとして使用される視差効果に基づいています。

場所： .\tessellation\_parallax\fs.glsl

コンテンツ：

```
<?xml version="1.0" encoding="UTF-8"?>

<!DOCTYPE sbsbatchnode SYSTEM "glslfx.dtd">

<glslfx version="1.0.0" author="allegorithmic.com">



    <!-- TECHNIQUES -->

    <technique name="Tesselation">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/tessellation/vs.glsl" primitiveType="patch4"/>

        <shader type="tess_control" filename="tessellation_parallax/tessellation/tcs.glsl"/>

        <shader type="tess_eval" filename="tessellation_parallax/tessellation/tes.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="0" max="0" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="0" max="0" />

        <uniform name="tessellationFactor" guiName="Tessellation Factor" default="4" min="1" max="64" guiStep="1" guiWidget="slider"/>

    </technique>



    <technique name="Parallax">

        <!-- PROPERTIES -->

        <property name="blend_enabled" value="true"/>

        <property name="blend_func" value="src_alpha,one_minus_src_alpha"/>

        <property name="cull_face_enabled" value="true"/>

        <property name="cull_face_mode" value="back"/>



        <!-- SHADERS -->

        <shader type="vertex" filename="tessellation_parallax/parallax/vs.glsl"/>

        <shader type="fragment" filename="tessellation_parallax/fs.glsl"/>



        <!-- UNIFORMS -->

        <uniform name="parallax_mode" guiName="Parallax Mode" min="1" max="1" />

        <uniform name="enableTilingInFS" guiName="Tiling Enabled In FS" min="1" max="1" />



    </technique>



    <!-- INPUT VERTEX FORMAT -->

    <vertexformat name="iVS_Position" semantic="position"/>

    <vertexformat name="iVS_Normal" semantic="normal"/>

    <vertexformat name="iVS_UV" semantic="texcoord0"/>

    <vertexformat name="iVS_Tangent" semantic="tangent0"/>

    <vertexformat name="iVS_Binormal" semantic="binormal0"/>



    <!-- SAMPLERS -->

    <sampler name="diffuseMap" usage="diffuse"/>

    <sampler name="heightMap" usage="height"/>

    <sampler name="normalMap" usage="normal"/>

    <sampler name="detailNormalMap" usage="detailNormal"/>

    <sampler name="emissiveMap" usage="emissive"/>

    <sampler name="specularMap" usage="specular"/>

    <sampler name="opacityMap" usage="opacity"/>

    <sampler name="environmentMap" usage="environment"/>



    <!-- MATRICES -->

    <uniform name="worldMatrix" semantic="world"/>

    <uniform name="worldViewProjMatrix" semantic="worldviewprojection"/>

    <uniform name="worldViewMatrix" semantic="worldview"/>

    <uniform name="worldInverseTransposeMatrix" semantic="worldinversetranspose"/>

    <uniform name="viewInverseMatrix" semantic="viewinverse"/>

    <uniform name="modelViewMatrix" semantic="modelview"/>

    <uniform name="projectionMatrix" semantic="projection"/>



    <!-- SCENE PARAMETERS -->

    <uniform name="AmbiColor" semantic="ambient"/>

    <uniform name="Lamp0Pos" semantic="lightposition0"/>

    <uniform name="Lamp0Color" semantic="lightcolor0"/>

    <uniform name="Lamp1Pos" semantic="lightposition1"/>

    <uniform name="Lamp1Color" semantic="lightcolor1"/>



    <!-- UNIFORMS -->

    <uniform name="tiling" guiName="Tiling" default="1" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="heightMapScale" guiGroup="Height" guiName="Scale" default="1" min="0" guiWidget="slider" guiMin="-50" guiMax="50" />

    <uniform name="TilingDetail" guiGroup="Detail Normal" guiName="Tiling" default="3" min="1" guiWidget="slider" guiMax="10"/>

    <uniform name="Depth_detail" guiGroup="Detail Normal" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.05" guiWidget="slider"/>

    <uniform name="SpecExpon" guiGroup="Specular" guiName="Power" default="50" min="1" guiWidget="slider" guiMax="128"/>

    <uniform name="Ks" guiGroup="Specular" guiName="Intensity" default="1" min="0" guiWidget="slider" guiMax="3"/>

    <uniform name="Kr" guiGroup="Reflection" guiName="Intensity" default="0.5" min="0" max="1" guiStep="0.01" guiWidget="slider"/>

    <uniform name="KF_on" guiGroup="Reflection" guiName="Falloff" default="1" min="0" max="1" guiStep="1" guiWidget="slider"/>

    <uniform name="KFs" guiGroup="Reflection" guiName="Falloff Size" default="1" min="-1" max="1" guiStep="0.05" guiWidget="slider"/>



</glslfx>
```
