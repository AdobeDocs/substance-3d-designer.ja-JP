---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/technical-issues/crash-when-rendering-graphs.html"
breadcrumb-title: ''
description: Substance 3D Designerでグラフをレンダリングする際にクラッシュする場合のトラブルシューティングを行い、その問題を回避するための解決策を見つけます。
helpx_creative_field: ""
helpx_description: Designer > Technical issues > Crash when rendering graphs
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: グラフのレンダリング時にクラッシュ
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 3%

---


# グラフのレンダリング時にクラッシュ

このページでは、Substance 3D Designerでのグラフのレンダリングプロセス中に発生するクラッシュの一覧を示し、それぞれのトラブルシューティング手順について説明します。

## TDR（Windowsのみ）

<b>[![（エラー）](../../assets/error.svg)](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)問題</b>

システムの<b>TDR (Timeout Detection &amp; Recovery)</b>タイマーは&#x200B;*短すぎます*。グラフィックスドライバーが&#x200B;*再起動*&#x200B;される前に、Substance 3D Designerで現在の計算を完了できません。

Substance 3D Designerによって実行される計算は非常に負荷が高くなる可能性があり、グラフィックスドライバーはしばらくの間、オペレーティングシステムに&#x200B;*反応しない*&#x200B;程度まで使用されます。\
安定性とセキュリティを確保するために、オペレーティングシステム&#x200B;*はグラフィックスドライバーを再起動*&#x200B;し、コンピューターの計算量を減らしてSubstance 3D Designer *がクラッシュ*&#x200B;します。

<b>![(tick)](../../assets/check.svg)おすすめの手順</b>

このようなクラッシュを防ぐには、TDRタイマーの値を&#x200B;*増加*&#x200B;する必要があります。 これは、Substance 3D Designerにも該当する、Substance 3D Painterのドキュメントの[このページ](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)の手順に従って行うことができます。
