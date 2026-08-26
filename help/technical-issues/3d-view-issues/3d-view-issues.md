---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/3d-view-issues.html"
breadcrumb-title: ''
description: レンダリング、表示、パフォーマンスの問題など、Substance 3D Designerの3Dビューに関する問題のトラブルシューティング
helpx_creative_field: ""
helpx_description: Designer > Technical issues > 3D View issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 3Dビューの問題
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '1643'
ht-degree: 0%

---


# 3Dビューの問題

このページでは、Substance 3D Designerの[3Dビュー](../../interface/3d-view/3d-view.md)に関連する技術的な問題の一覧を表示し、それぞれのトラブルシューティング手順を紹介します。

## 低パフォーマンス：ディスクリートGPUは使用されていません

**![（エラー）](../../assets/error.svg)問題**

Substance 3D Designerは、システムの&#x200B;*discrete* GPU (<b>dGPU</b>)を使用せず、*統合* GPU (<b>iGPU</b>)を使用します。 これにより、グラフや[3Dビュー](../../interface/3d-view/3d-view.md)をレンダリングする際のパフォーマンスが低下します。

**![（ティック）](../../assets/check.svg)推奨ステップ**

グラフィックスを切り替え可能なシステムでは、GPUの製造元によって&#x200B;*dGPU*&#x200B;を強制的に実行できます。これは、専用ソフトウェアの&#x200B;*特定のアプリケーション*&#x200B;に使用されます。

例えば、<b>Nvidia dGPU</b>を使用するユーザーは、次の操作を実行できます。

1. Substance 3D Designerを閉じる
2. <b>NVIDIAコントロールパネル</b>を開きます
3. <b>3D設定の管理</b>画面（<b>3D設定</b>セクション）に移動
4. [<b>プログラムの設定</b>]タブで&#39;Substance 3D Designer&#39;エントリを探します
5. <b>優先GPU</b>コンボボックスで<b>高性能NVIDIAプロセッサー</b>を選択
6. Substance 3D Designerを開始

>[!WARNING]
>
> 統合GPU (iGPU)は&#x200B;*サポートされていません*。 詳しくは、[必要システム構成](../../getting-started/system-requirements/system-requirements.md)ページをご覧ください。

## 3Dオブジェクトはフラットです

**![（エラー）](../../assets/error.svg)問題**

あるセッションで詳細なボリュームを特徴とする3Dオブジェクトは、次のセッションではフラットになりますが、グラフは変更されておらず、Heightマップには同じデータが含まれています。

**![（ティック）](../../assets/check.svg)推奨ステップ**

Heightマップに基づく3Dオブジェクトの変形効果は、**テッセレーションディスプレイスメント**&#x200B;と呼ばれる手法を用いて行われる。 この方法には2つの手順があります。

1. **テッセレーション**:オブジェクトジオメトリは&#x200B;*頂点に再分割*&#x200B;され、より細かいボリュームの詳細をサポートするために&#x200B;*密度の高い*&#x200B;ジオメトリになります
2. **ディスプレイスメント**：頂点は、*法線ベクトル*&#x200B;に沿って&#x200B;*移動* （つまり、変位）しています。 法線ベクトルは、ポリゴンが向いている方向に従い、大きさ（長さ）は1です

ディスプレイスメント&#x200B;*direction*&#x200B;は既知です：法線ベクトルの方向です。\
頂点を移動するディスプレイスメント&#x200B;*距離*&#x200B;は、次のように計算されます： `Distance = Height scale * Height map`。 グラフのHeightマップは&#x200B;*変更されていない*&#x200B;ため、**Heightスケール**&#x200B;のままです。

既定のHeightスケール値は&#x200B;**1.0**&#x200B;です。これは、3Dビューに表示されるメッシュと、それに適用されるHeightマップによっては、*目立たない*&#x200B;ディスプレイスメント効果になる場合があります。

この値は、次の方法で変更できます。

| 3Dビュー内 | グラフビュー内 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 左側のツールバーの&#x200B;**ディスプレイスメントポップアップ**&#x200B;を使用します。<br>詳細については、[専用ページ](../../interface/3d-view/displacement/displacement.md)を参照してください。 | [Output](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)ノードを作成し、そのプロパティで`heightScale`の使用法を設定します。<br>この出力に値を指定します。例えば、[定数浮動小数点ノード](../../compositing-graphs/nodes-reference-for-com/node-library/values/constant.md#floats)を使用して、値を指定してから、*3Dビューでグラフを再適用*&#x200B;します。 |

>[!TIP]
>
> この手法を使用すると、グラフごとに&#x200B;*カスタムのHeightスケール値*&#x200B;を設定し、グラフのマテリアルに合わせて調整できます。

## 3Dビューが完全に黒くなる

**![（エラー）](../../assets/error.svg)問題**

バージョン15.0.0以降では、3Dビューのビューポートは平坦な黒になります。 テキストオーバーレイ（サンプルやレンダリング時間など）が表示されていても、3Dシーンが表示されない。

**![（ティック）](../../assets/check.svg)推奨ステップ**

バージョン15.1以降

新しい3Dレンダラーは、バージョン15.1でアップグレードされ、最新のGPUドライバーが必要です。 システムのGPUドライバーを最新バージョンに更新してください。

ドライバーは次の場所で確認できます： [NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [インテル](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

バージョン15.0以降

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md)では、最新のテクノロジーを使用しているため古いGPUではサポートされていない新しい社内の[3Dレンダラー](../../interface/3d-view/3d-renderers/3d-renderers.md)を導入しました。

サポートされているGPUには、Designerの[必要システム構成](../../getting-started/system-requirements/system-requirements.md)に従って、NVIDIA RTX 20シリーズ(Turing)以降が含まれています。

プロジェクト設定の[新しいオプション](../../interface/preferences-window/project-settings/project-settings.md)を使用すると、既定でOpenGLレンダラーを引き続き使用できます。

1. 編集/環境設定/プロジェクトを選択します
2. リスト内の最後のプロジェクトファイルを選択
3. プロジェクトファイルのリストで、[3Dビュー]タブを選択します
4. 「デフォルトのレンダラー」オプションを「OpenGL（非推奨）」に設定します
5. 「OK」をクリックして変更を検証します

これで、すべての新しい3DビューでデフォルトでOpenGLレンダラーが使用され、これまでと同様に作業を続けることができます。

>[!NOTE]
>
> 同じ問題とトラブルシューティング手順が、ほとんどのAMDおよびIntel GPUに適用されます。これらのGPUは現在、新しい3Dレンダラーでは&#x200B;*サポートされていません*。

>[!IMPORTANT]
>
> OpenGLレンダラーは&#x200B;*非推奨*&#x200B;であり、将来的にDesignerから削除される可能性があります。 ワークフローの中断を防ぎ、継続的なサポートを確保するために、システムのGPUをアップグレードすることをお勧めします。

## 「レンダラーがサポートされていません」というメッセージが表示される

**![（エラー）](../../assets/error.svg)問題**

バージョン15.0.0以降では、新しい3Dレンダラー（ラスタライザー、GPUパストレーサー）を使用すると、ビューポートの右下隅に「レンダラーはサポートされていません」というメッセージが表示されます。 3Dシーンは表示されません。

**![（ティック）](../../assets/check.svg)推奨ステップ**

Designer [15.0.0](../../release-notes/version-15-0/version-15-0.md)では、最新のテクノロジーを使用しているため古いGPUではサポートされていない新しい社内の[3Dレンダラー](../../interface/3d-view/3d-renderers/3d-renderers.md)を導入しました。

サポートされているGPUには、Designerの[必要システム構成](../../getting-started/system-requirements/system-requirements.md)に従って、NVIDIA RTX 20シリーズ(Turing)以降が含まれています。

[プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)で「デフォルトのレンダラー」オプションが「デフォルト（定義済みのレンダラー）」に設定されている場合、デフォルト設定では、3Dビューは自動的にOpenGLレンダラーにフォールバックします。

このオプションは、次の手順に従って検索および調整できます。

1. 編集/環境設定/プロジェクトを選択します
2. リスト内の最後のプロジェクトファイルを選択
3. プロジェクトファイルのリストで、[3Dビュー]タブを選択します
4. タブ内の設定に「デフォルトのレンダラー」オプションが一覧表示されます

>[!NOTE]
>
> 現在、<b>NVIDIA GTXシリーズ</b>のGPUのみが検出され、サポートされていません。
> 
> ただし、ほとんどのAMDおよびIntel GPUもサポートされておらず、メッセージが表示されずに黒でレンダリングされます。 これらのGPUに関するガイダンスについては、上記の「3Dビューが完全に黒い」項目を参照してください。

>[!IMPORTANT]
>
> OpenGLレンダラーは&#x200B;*非推奨*&#x200B;であり、将来的にDesignerから削除される可能性があります。 ワークフローの中断を防ぎ、継続的なサポートを確保するために、システムのGPUをアップグレードすることをお勧めします。

## 3Dオブジェクトは完全に滑らかに見えます

**![（エラー）](../../assets/error.svg)問題**

**Height** [出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)に送信されたデータを処理すると、オブジェクトにはボリュームがあるように見えますが、シェーディングでHeight情報が無視されたかのように、*全体的に滑らかに*&#x200B;見えます。

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![（ティック）](../../assets/check.svg)推奨ステップ**

Heightデータが&#x200B;*法線*&#x200B;に変換され、**法線** [出力](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/output/output.md)に接続されていることを確認してください。

**テッセレーションディスプレイスメント**&#x200B;手法を使用する場合 – 上記の「3Dオブジェクトが平坦である」を参照 – オブジェクトはHeightデータに従って&#x200B;*変形*&#x200B;する場合がありますが、Heightデータを考慮して&#x200B;*法線*&#x200B;も変更されるまで、そのサーフェスは光に対して&#x200B;*異なる反応を示さない*&#x200B;ことになります。

解決策は非常に簡単です。Height出力につながるストリームの最後のノードを[Normal](../../compositing-graphs/nodes-reference-for-com/atomic-nodes/normal/normal.md)ノードに接続します。 作業中のマテリアルに応じてそのノードの&#x200B;**強度**&#x200B;パラメーターを調整し、標準ノードを&#x200B;**標準**&#x200B;出力に接続します。

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/3dview-height-without-normals.gif){width="256px"}

</td>
</tr>
</table>

## レンダリングがぼやけている/ピクセル化されている

**![（エラー）](../../assets/error.svg)問題**

システムが&#x200B;*画面の拡大/縮小*&#x200B;を使用している場合、レンダリングされたイメージがぼやけたり、ピクセル化されたように見えます。

<table style="margin-left: 0; margin-right: 0;">
<tr style="border: 0;">
<td style="border: 0; width: 60%; vertical-align: top">

**![（ティック）](../../assets/check.svg)推奨ステップ**

初期設定では、Designerは&#x200B;*拡大/縮小*&#x200B;の表示解像度を使用して[3Dビュー](../../interface/3d-view/3d-view.md)のレンダリング解像度を定義します。 これを変更して、鮮明なレンダリングに&#x200B;*ネイティブ*&#x200B;のディスプレイ解像度を使用できます。

**編集**&#x200B;メニューを開き、**環境設定…**&#x200B;オプションを選択します。 [環境設定](../../interface/preferences-window/preferences-window.md)ウィンドウで、**3Dビュー**&#x200B;セクションを開き、**ビューポートの拡大・縮小**&#x200B;パラメーターを&#x200B;*なし*&#x200B;に設定します。

</td>
<td style="border: 0; width: 40%; vertical-align: top">

![](../../assets/demo-viewport-scaling-option.png){width="256px"}

</td>
</tr>
</table>

## &#39;Tessellation factor&#39;プロパティが見つかりません

**![（エラー）](../../assets/error.svg)問題**

Designerをバージョン15.0.0にアップグレードした後、以前のマテリアルプロパティに「テッセレーション係数」パラメーターが見つかりません。

**![（ティック）](../../assets/check.svg)推奨ステップ**

新しいレンダラー（ラスタライザとGPU パストレーサー）を使用する場合、「テッセレーション係数」がこれらのレンダラーのプロパティにあります。 3Dビューで、<b>レンダラー/設定の編集</b>に移動します。 プロパティは、プロパティドックに表示されます。

>[!NOTE]
>
> テッセレーションの範囲は、レンダラーによって異なります。
> 
> * ラスタライザ/GPU パストレーサー:シーン全体にグローバルに適用される固有の値です。
> * OpenGL:マテリアルごとに1つの値。
> * Iray:メッシュごとに1つの値です。

## 3Dオブジェクトの見た目が正しくない：照明に合わせてシェーディングが調整されない

**![（エラー）](../../assets/error.svg)問題**

オブジェクトのシェーディングは、法線、接線、および従法線ベクトルに依存します。 通常のマップではほとんどの場合[0, 1]の範囲が使用されますが、それらの座標では[-1, 1]の範囲が使用されます。 一方の値をもう一方の値に適応させるには、<b>バイアスとスケール</b>を適用する必要があります。value\*scale+biasです。

例えば、スケール2とバイアス–1はx値[0, 1]から[-1, 1]にx値を適応させ、x\*2-1に変換します。

Designerでは、3Dメッシュで指定されていない限り、法線のスケールとバイアスは適用されません。 その情報が欠落している場合、[そのマテリアルのいずれかを上書き](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)すると、コンソールで警告が発生します：

```
[SceneGraph]No 'scale' or 'bias' defined on the UsdUVTexture shader '/root/material/<materialName>' (the rendering may be incorrect)
```


**![（ティック）](../../assets/check.svg)推奨ステップ**

少し前にUSD形式に書き出したシーンの場合：最新バージョンのUSDを使用してシーンを再書き出しします。これには必要なデータが含まれます。 法線のスケールとバイアスに関連するプロパティがある場合は、それに注意してください。これは、シーンのエクスポートに使用するソフトウェアによって異なります。

[マテリアルをオーバーライド](../../working-with-3d-scenes/overriding-scene-mat/overriding-scene-materials.md)すると、Designerはメッシュを処理し、その法線、接線、および従法線に関連する欠落データを計算します。 Designerのデフォルトのスケールとバイアスがメッシュに必要な値と一致した場合、メッシュはオーバーライドされると正しく表示されます。

## 3Dビューの起動時にクラッシュする

**![（エラー）](../../assets/error.svg)問題**

3Dビューの起動時、プロジェクトの作成時、プロジェクトの読み込み時、または3Dビューを手動で開始するときに、Designerがクラッシュする。

**![（ティック）](../../assets/check.svg)推奨ステップ**

まず、ご使用のシステムがDesignerの[必要システム構成](../../getting-started/system-requirements/system-requirements.md)を満たしていることを確認してください。

次に、グラフィックドライバーを更新します。 次のリンクを参照して、GPUの最新ドライバーを確認できます。[NVIDIA](https://www.nvidia.com/Download/index.aspx?lang=en-us)  | [AMD](https://www.amd.com/en/support)  | [インテル](https://downloadcenter.intel.com/product/80939/Graphics-Drivers)

お使いのシステムに、統合GPU (iGPU)とディスクリートGPU (dGPU)の両方が搭載されている場合は、*両方のドライバーを更新*&#x200B;してください。

次に、3Dグラフィックプロセスでデータを挿入またはオーバーレイするソフトウェアを無効にします。 例を次に示します。

* ReShadeなどの後処理インジェクタ
* カスタムクロスヘアやGPUパフォーマンス指標などのオーバーレイ
* 3Dグラフィックスをリアルタイムで記録、ストリーミング、または共有するための画面キャプチャソフトウェア
