---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/substance-compositing-graphs/nodes-reference-for-substance-compositing-graphs/node-library/material-filters/scan-processing/material-clone-patch.html"
breadcrumb-title: ''
description: マテリアルコピーパッチノードを使用して、スキャンしたマテリアルのアーティファクトを修復するためのテクスチャ領域をクローンおよびパッチします。
helpx_creative_field: ""
helpx_description: Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Material Filters > Scan Processing > Material Clone Patch
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: マテリアルクローンパッチ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '334'
ht-degree: 1%

---


# マテリアルクローンパッチ

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

![](../../../../../../assets/clone-patch-material.png){width="128px"}

## マテリアルクローンパッチ

**イン：** *マテリアルフィルター/スキャン処理*

**複合**

</td>
<td style="border: 0;" valign="top">

## 説明

[コピーパッチ](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)のマルチチャンネル、完全なマテリアルバージョンです。 マテリアルのすべてのチャンネルに対してクローンパッチを実行します。 [詳細については、元のバージョンを参照してください。](../../../../../../compositing-graphs/nodes-reference-for-com/node-library/material-filters/scan-processing/clone-patch/clone-patch.md)

これは、マテリアルのすべてのチャンネルからディテールを削除する場合に非常に便利です。 複数のチャンネルのデバッグ画像を出力して、スマートパッチ領域がどのように見えるかを確認します。

## パラメーター

### 入力

* **マスク**: *グレースケール入力*\
  ノードのエフェクトのマスクに使用するマスクスロット。 「マスク」パラメーターで切り替えることができます。

### パラメーター

* **チャネル**
  * この領域でマテリアルチャンネルのオンとオフを切り替えます。たとえば、メタリック/ラフネスの代わりにSpecular/光沢マップを使用する場合などです。
* **シェイプ**: *正方形、ディスク*&#x200B;スタンプのシェイプを設定します。 ベースとしてのみ使用されます。
* **エッジ**
  * **しきい値（複数チャンネルの場合）**: *0.0 ～ 1.0*&#x200B;ブレンドした領域の到達距離を設定します。 これは、ターゲット領域のシェイプに沿って段階的に大きくなるので、背景を均一にすると効果が非常に少なくなります*。*チャンネル間でこの値を変更しすぎると、視覚的な食い違いが生じる可能性があるので、注意してください。
  * **ぼかし**: *0.0 ～ 2.0*&#x200B;より緩やかな変化が必要な場合に備えて、スタンプ領域のエッジをぼかします。
  * **Smoothness**: *0.0 ～ 2.0*&#x200B;印鑑の形状のエッジを丸めて、アウトラインの流れを滑らかにします。
  * **グリッド解像度**: *1 - 11*&#x200B;ブレンド分析の品質解像度を設定します。 値が大きいほど、ブレンドの精度は高くなります。
* **変換**
  * **ソースマトリックス**: *（変換マトリックス）*ソースを変換します（スケールと回転）。 カンバス上では実行できません。これらのパラメーターのみを変更してください。
  * **ソースオフセット**: *-0.5 - 0.5*&#x200B;ソースの場所を変換します。 カンバス上では実行できません。これらのパラメーターのみを変更してください。 *このパラメーターは、変更するメインのパラメーターである可能性があります。*
  * **ターゲット行列**: *（変換行列）*ターゲットの位置を変換します（スケールと回転）。 カンバス上のギズモを使用しても実行できます。
  * **ターゲットオフセット**: *-0.5 - 0.5*&#x200B;ターゲットの場所を変換します。 カンバス上のギズモを使用しても実行できます。

## サンプル画像

|  |
| --- |
| このページに添付された画像はありません。 |

</td>
</tr>
</table>
