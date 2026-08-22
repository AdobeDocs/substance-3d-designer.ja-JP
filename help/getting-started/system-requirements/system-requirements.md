---
helpx_url: "https://helpx.adobe.com/jp/substance-3d-designer/getting-started/system-requirements.html"
breadcrumb-title: ''
description: Substance 3D Designerの必要システム構成を確認して、コンピューターが必要な仕様を満たしていることを確認してください。
helpx_creative_field: ""
helpx_description: Designer > Getting started > System requirements
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 必要システム構成
user-guide-description: ''
user-guide-title: ''
source-git-commit: ec787363bab8318804a71d6cf7c5484fc67a987e
workflow-type: tm+mt
source-wordcount: '830'
ht-degree: 0%

---


# サポート対象システム

以下に、アプリケーションでサポートされているハードウェアとシステムのリストを示します。

## Windows

|  | 最小 | おすすめ | 最適 |
| --- | --- | --- | --- |
| <b>OS</b> | Windows 11 64ビット版23H2 | Windows 11 64ビット版24H1 | Windows 11 64ビット版24H2 |
| <b>CPU</b> | Intel Core i5 AMD Ryzen 5 | Intel Core i7 AMD Ryzen 7 | Intel Core i9 AMD Ryzen 9 |
| <b>GPU</b> | NVIDIA GeForce RTX 2060 Super NVIDIA Quadro RTX 4000 AMD Radeon RX 5700 XT AMD Radeon Pro W5700 | NVIDIA GeForce RTX 3080 NVIDIA Quadro RTX A4000 AMD Radeon RX 6800 XT AMD Radeon Pro W7700 | NVIDIA GeForce RTX 4090 NVIDIA Quadro RTX 5000 Ada Generation AMD Radeon RX 7900 XTX AMD Radeon Pro W7800 |
| <b>VRAM</b> | 8 GB | 16 GB | 24 GB |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>ストレージ</b> | 30 GBの空き容量のあるSSD | 50 GBの空き容量のあるSSD | 70 GBの空き容量のあるSSD |

### macos

|  | 最小 | おすすめ | 最適 |
| --- | --- | --- | --- |
| <b>OS</b> | macOS14ソノマ | macOS 26タホ | macOS 26タホ |
| <b>CPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>GPU</b> | Apple M1 | Apple M2 Pro | Apple M4 Pro |
| <b>RAM</b> | 16 GB | 32 GB | 64 GB |
| <b>ストレージ</b> | 30 GBの空き容量のあるSSD | 50 GBの空き容量のあるSSD | 70 GBの空き容量のあるSSD |

### Linux

| Enterprise | スチーム |
| --- | --- |
| RHEL 8 </br>RHEL 9 | Ubuntu 22.04 |

## 一般的な推奨事項

* 快適な状態で作業するには、1メガピクセルを超え、1280ピクセルを超える解像度のモニターをお勧めします。
* 多くのSubstanceアプリは、RHEL8/9との互換性をOpenSSL 1.1.1に依存しています。 新しいバージョンのOpenSSLを使用するシステムでは、手動で提供する必要があります。
* *MacOS 10.15</b> (Catalina)で実行するために、<b>2019.x</b>以降の*&#x200B;バージョンのみが公証されました。<b>
* <b>リモートデスクトップ</b>接続は、OpenGL 3.3コンテキストが利用可能な場合に可能です。 OpenGL 1.4コンテキストのみを提供するため、Nvidia GeForceでは<b>Nvidia Quadro</b>で動作しますが、*では動作しません*。 これが問題である場合は、<b>VNC</b>/<b>Teamviewer</b>などの代替ソリューションを使用することをお勧めします。
* <b>Steam</b>のバージョンを使用している場合は、Designer用<b>Steamオーバーレイ</b>を&#x200B;*無効*&#x200B;にする必要があります。アクティブ時にパフォーマンスの問題が発生する可能性があります。

## サポートされているGPU

以下に、このアプリケーションと互換性のあるGPUのリストを示します。

* NVIDIA GeForce GTX 1060以降
* NVIDIA Quadro P2200以降
* AMD Radeon RX 580以降
* AMD Radeon Pro 5300 M

>[!TIP]
>
> **TDR （Windowsのみ）**
> 
> GPUで大量の計算を実行する際（複雑なグラフのレンダリング、3Dビューでのレンダリング、3Dビューからのシーンの書き出しなど）に全体的な安定性を最大限に高めるには、<b>タイムアウトの検出と回復(TDR)</b>の値がドキュメントの[このページ](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-drivers-crash-with-long-computations-tdr-crash)の推奨事項と一致していることを確認することを強くお勧めします。

## サポートされていない設定

<b>ウィンドウ</b>

* 仮想マシンはサポートされていません。
* Windows Serverはサポートされていません。

<b>macOS</b>

* IntelベースのmacOSシステムはサポートされていません。
* 公式のApple設定のみがサポートされています。
* eGPUは現在サポートされておらず、安定性の問題がある可能性があります。

<b>Linux</b>

* Linux上のMesaドライバはサポートされていません。

<b>任意のプラットフォーム</b>

* 内蔵GPUは、x86-64(Intel、AMD)CPUではサポートされていません。
* Designerをサードパーティ製ソフトウェアと組み合わせて使用し、Designerによるグラフィックドライバーの呼び出しを傍受する機能はサポートされていません。 当該ソフトウェアには、以下が含まれます。
  * カラーグレーディングを適用するリシェーダなどの後処理インジェクタ、カメラエフェクト、...
  * カスタムクロスヘア、GPUパフォーマンス指標、ビデオストリーミング用スキンなどのオンスクリーンオーバーレイ

## GPUドライバーの最小バージョン

アプリケーションを問題なく実行するために必要なGPUドライバーの最小バージョンを以下に示します。 このリストは、新しいバージョンのリリースに伴って変更される場合があります。

新しいドライバーをダウンロードするには、[GPUに古いドライバーがあります](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/technical-support/technical-issues/gpu-issues/gpu-has-outdated-drivers)を参照してください。

| OS | NVIDIA | AMD | Intel |
| --- | --- | --- | --- |
| <b>ウィンドウ</b> | GeForce 451.48 Quadro 451.48 | Radeon 19.7.1 Radeon Pro / FirePro 18.Q4 | 15.33 |
| <b>Linux</b> | 535.129.03 | Radeon 23.20 Pro 23.Q3 | 非対応 |

>[!NOTE]
>
> **Mac OS**&#x200B;では、GPUドライバーはオペレーティングシステム自体から提供されます。 最新のドライバーにアクセスするには、OSを最新バージョンにアップデートしてください。

## 焼き用GPU レイトレーシング

OptixまたはDXR経由でGPU レイトレーシングを有効にするには、上記の推奨ドライバをインストールする必要があります。

<b>DXR</b>には次の最小構成が必要です：

* <b>Windows 10</b>バージョン1809。詳細については、[このページ](https://experienceleague.adobe.com/ja/docs/substance-3d/bakers/features/gpu-raytracing)を参照してください
* <b>Pascalアーキテクチャ搭載GPU</b> (Nvidia GeForce 10XX)

>[!TIP]
>
> GPU レイトレーシングは、NVIDIA GeForce RTXまたはNVIDIA Quadro RTX GPUなどの専用レイトレーシングハードウェアで最適に実行されます。

## タブレットの使用

<b>Windows</b>のタブレットユーザーは、最も信頼性の高いエクスペリエンスを実現するために、次のページで説明されている設定を適用する必要があります： [ペンとタブレットの構成](https://experienceleague.adobe.com/ja/docs/substance-3d-painter/using/technical-support/configuring-pens-and-tablets)。

## 言語

ソフトウェアインターフェイスは次の言語で使用できます。

* ドイツ語（ドイツ）
* 英語（米国）
* Español （スペイン語）
* フランス語（フランス）
* イタリア語（イタリア）
* ポルトガル語（ブラジル）
* 日本語（日本）
* 한국어(한국)
* 简体中文（中国)
