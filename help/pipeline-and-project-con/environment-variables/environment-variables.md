---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/pipeline-and-project-configuration/environment-variables.html"
breadcrumb-title: ''
description: Substance 3D Designerで環境変数を使用して、パスやシステム設定を構成する方法について説明します。
helpx_creative_field: ""
helpx_description: Designer > Pipeline and Project Configuration > Environment variables
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 環境変数
user-guide-description: ''
user-guide-title: ''
source-git-commit: 5b9c9d12e2ccd76f75ec2a74815f9c68c43c06a2
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 3%

---


# 環境変数

このページには、アプリケーションのデフォルトの動作を上書きするために使用できる環境変数が一覧表示されます。

| 変数 | 説明 |
| --- | --- |
| **SBS\_DESIGNER\_PYTHON\_PATH** | Designerが[Pythonプラグイン](../../scripting/plugin-basics/plugin-basics.md)を読み込むパス。 |
| **SUBSTANCE\_DESIGNER\_ライセンス** | Designerで使用する必要があるライセンスファイル(*license.key*)の場所です。   Designer [ライセンス認証ウィザード](../../getting-started/activation-and-licenses/activation-and-licenses.md)で設定されたパスを上書きします。  **注意：**&#x200B;古いバージョンでは、代替の変数名を使用する必要がある場合があります：<ul data-preserve-html="true"><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_6_LICENSE</strong></li><li data-preserve-html="true"><strong>SUBSTANCE_DESIGNER_5_ライセンス</strong></li></ul> |
| <b>OCIO</b> | OpenColorIO [カラーマネジメント](../../color-management/color-management.md)を使用する際に使用するOCIO設定ファイルへのパスです。   [プロジェクト設定](../../interface/preferences-window/project-settings/project-settings.md)のDesignerのカラーマネジメント設定で設定されたパスをオーバーライドします。 |
| **ALLEGO\_LICENSE\_IDLE\_DELAY** | マルチユーザー構成の場合、ライセンスシートをリリースするまでの遅延時間デフォルトは7200秒（2時間）です。 |
