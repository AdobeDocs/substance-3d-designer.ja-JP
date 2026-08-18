---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/technical-issues/baking-issues.html"
breadcrumb-title: ''
description: Substance 3D Designerでのテクスチャのベイク処理に関する技術的な問題のトラブルシューティング手順を説明します。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Baking issues
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: ベイク処理の問題
user-guide-description: ''
user-guide-title: ''
source-git-commit: 6c55ac0f1f6da5bc5683a34a4eca174f978eac64
workflow-type: tm+mt
source-wordcount: '216'
ht-degree: 0%

---


# ベイク処理の問題

このページでは、Substance 3D Designerでの[テクスチャのベイク](../../bakers/bakers.md)に関する技術的な問題を一覧表示し、それぞれのトラブルシューティング手順を紹介します。

## このページ内

「名前で一致」が機能しない

## 「名前で一致」が機能しない

<table>
<tr style="border: 0;">
<td style="border: 0;" valign="top">

<b>![（エラー）](../../assets/error.svg)問題</b>

「一致」オプションが「メッシュ名による」に設定されている場合、一致が適用されないか、すべてのシーンオブジェクトに一貫して適用されません。

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

Designer 14.1以前のバージョンでは、低ポリゴンおよび高ポリゴンのオブジェクトは、*親*&#x200B;オブジェクトの名前を使用して一致させられました。ほとんどの場合、親のトランスフォームです。

Designer 15.0以降、*ジオメトリ*&#x200B;オブジェクトの名前は直接使用されます。

</td>
<td style="border: 0;" valign="top">

![シーンツリーのジオメトリオブジェクトとその親](../../assets/sceneTree_objectsName.png "シーンツリーのジオメトリオブジェクトとその親"){zoomable="yes"}

</td>
</tr>
</table>

期待どおりの結果を得るには、次の2つの方法があります。

* ジオメトリオブジェクトの名前を調整して、一致する名前を適用します。
* プロジェクト設定で[&#39;名前フィルターモード&#39;オプション](../../interface/preferences-window/project-settings/project-settings.md)を適用して、Designerの以前のバージョンに戻します。
  1. 編集/環境設定/プロジェクトを選択します
  1. リスト内の最後のプロジェクトファイルを選択
  1. プロジェクトファイルのリストの下で、「ベイカー」タブを選択します。
  1. 「名前フィルタリングモード」を「親名（レガシー）」に設定
