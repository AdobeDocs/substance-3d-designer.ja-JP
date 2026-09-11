---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/interface/3d-view/switching-your-shaders-to-opengl-core-profile.html"
breadcrumb-title: ''
description: Substance 3D Designer 3DビューでシェーダをOpenGL Core Profileに切り替えて、互換性とパフォーマンスを向上させる方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Interface > 3D View > Switching your shaders to OpenGL Core Profile
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: シェーダをOpenGLコアプロファイルに切り替える
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 0%

---


# シェーダをOpenGLコアプロファイルに切り替える

バージョン2018.2.0以降、3D ビューポートはOpenGLコアプロファイルを使用します。\
この際、GLSLバージョン120からGLSLバージョン330へのアプリケーションに用意されているシェーダをいくつか更新しました。

独自のシェーダを更新して、使用可能な新しいGLSL関数を活用するか、GLSLコードをより新しくすることができます。 macOSでは、古いシェーダが機能しなくなる可能性があることに注意してください。\
新機能の概要を確認するために、OpenGLの公式ドキュメントを参照することを強くお勧めします。 たとえば、[OpenGLシェーディング言語の仕様3.30](https://www.khronos.org/registry/OpenGL/specs/gl/GLSLangSpec.3.30.pdf)を見ることができます。\
それ以外の場合は、GLSL 3.30でGLSL 1.20シェーダを変換するのに役立つクイックガイドを参照してください。

## バージョン番号の更新

まず、以前の`#version`ディレクティブを`#version 330`で置き換えます（まだ持っていない場合はファイルの先頭に追加します）。

### 「attribute」と「varying」を「in」または「out」で置き換えます

現在、`attribute`および`varying`変数は、シェーダーステージに応じて`in`または`out`として明示的に宣言されています。

頂点 シェーダーでは、頂点の`attribute`が`in`として宣言され、フラグメントシェーダーに渡される`varying`が`out`として宣言されています。\
以下に例を示します。

```
## version 120



attribute vec3 vertexPosition;

attribute vec3 vertexNormal;

attribute vec2 vertexUV;



varying vec3 fragmentNormal;

varying vec2 fragmentUV;
```


次のようになります。

```
## version 330



in vec3 vertexPosition;

in vec3 vertexNormal;

in vec2 vertexUV;



out vec3 fragmentNormal;

out vec2 fragmentUV;
```


フラグメントシェーダーでも同様に、変化が生じます。 また、gl\_FracColor （これはビルドインではなくなりました）を置き換えるout変数を宣言しなければなりません。

```
## version 120



varying vec3 fragmentNormal;

varying vec2 fragmentUV;



void main() {

...

gl_FragColor = vec4(myColor.rgb, 1.0);

}
```


次のようになります。

```
## version 330



in vec3 fragmentNormal;

in vec2 fragmentUV;



out vec4 outColor; //you could choose any name you want here



void main() {

...

outColor = vec4(myColor.rgb, 1.0);

}
```


### 新しいテクスチャ参照関数の使用

新しいバージョンのシェーディング言語では、テクスチャ検索APIが簡素化され、強化されています。

`texture1D()`、`texture2D()`、`texture3D()`および`textureCube()`関数はすべて`texture()`のオーバーロードになります。\
同様に、`texture2DLod()`は`textureLod()`になり、`texture2DGrad()`は`textureGrad()`になります。

また、`textureSize()` （ピクセルのサンプラーのサイズを照会）、`textureOffset()` （ターゲット位置の近隣のサンプルを抽出）、`textureFetch()` （ピクセルのサンプル位置を提供）などの便利な関数にもアクセスできるようになりました。
