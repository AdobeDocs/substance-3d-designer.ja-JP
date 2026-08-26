---
source-git-commit: ec58342925d3e608b0180b67a1e20ffaeb1f306a
workflow-type: tm+mt
source-wordcount: '527'
ht-degree: 0%

---
# CLAUDE.md

このファイルは、このリポジトリーでコードを操作する際のガイダンスとしてClaude Code (claude.ai/code)を提供します。

&#x200B;# Substance 3D Designerドキュメント

このリポジトリーには、Substance 3D Designerに関するドキュメントが含まれています。 アプリケーションコード、ビルドステップ、またはテストスイートがありません。リポジトリ&#x200B;*は*&#x200B;のコンテンツで、マークダウンで記述され、[Adobe Experience League](https://experienceleague.adobe.com/docs/substance3d-designer.html?lang=en)に公開されています。

&#x200B;# リポジトリ構造

* `help/` – すべてのドキュメントコンテンツ。目次をミラーリングするように構成されています。
* `help/guide/TOC.md` – 目次。 すべてのエントリは、ページのマークダウンファイルへの相対リンクです（`/help/...`をルートとする）。 `TOC.md`にはページツリーメタデータ（`user-guide-title`、`breadcrumb-title`、`nudge`、`{#section-id}`などのセクションアンカー）も含まれています。
* `help/assets/` – 共有された、ページ固有ではない画像（ページ間で再利用されるアプリアイコンなど）。
* `help/glossary/glossary.md` – 単一の大きな用語集ページで、`#term`フラグメントによるクロスリンクに使用されるアンカースパン(`<span id="term"></span>`)でアルファベット順に整理されています。
* `metadata.md` – リポジトリレベルの前付（クラウド/ソリューション/製品ID、`git-repo`など） これは`TOC.md`ごとに継承されます。 リポジトリ全体のメタデータの変更にのみ編集します。ページ固有のメタデータは、ページ自体の前付に属します。
* `redirects.csv`、`linkcheckexclude.json`、`markdownlint_custom.json`、`pipeline.opts` – 公開パイプライン構成（リダイレクト、リンク確認例外、lintルールのオーバーライド、パイプラインオプション）。
* `fix-image-names.py` — `help/assets`画像の名前をかっこで囲んだサフィックス（`foo(1).png` → `foo_1.png`など）に変更し、すべてのMarkdown参照を一致するように書き換える1回限りのユーティリティです。 通常のワークフローには含まれません。このようなファイル名が再び表示された場合にのみ手動で実行してください。

## フォルダー/目次の命名規則

`help/guide/TOC.md`の各エントリについて：
* 目次と同じ入れ子に続く、`help/`の下に対応するフォルダーがあります。
* このフォルダーには、1つのマークダウンファイルが含まれています。このファイルは、ページタイトルのケバブバージョンとして名前が付けられています。
* ページに専用のメディア（画像、GIF、ビデオ）がある場合、そのページは`<md-file-name>.resources`という名前の兄弟サブフォルダーに格納されます。

ページを追加または移動する場合、`TOC.md`とフォルダーレイアウトを同時に更新します。同期を維持する必要があります。

## ページの前付

通常のコンテンツページは、次のような前付ブロックを使用します。

```yaml
---
helpx_url: "https://helpx.adobe.com/substance-3d-designer/<section>/<page>.html"
breadcrumb-title: ""
description: <one/two sentence SEO description>
helpx_creative_field: ""
helpx_description: Designer > <Section> > <Page>
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: <Page title>
user-guide-description: ""
user-guide-title: ""
---
```

`description`を正確かつ簡潔に保ちます。SEO/検索スニペットに使用されます。

&#x200B;# コンテンツオーサリングルール

* 英語は真理の源だ。他のすべての言語はそこから翻訳される。
* 他のドキュメントページへのリンクはすべて&#x200B;**相対**&#x200B;リンクにする必要があります。外部リソースへのリンクはすべて&#x200B;**絶対**&#x200B;リンクにする必要があります。
* コンテンツは、GitHubフレーバーのマークダウンで、Experience Leagueのカスタム拡張機能/gotchasを使用して書かれています。[こちら](https://experienceleague.adobe.com/ja/docs/contributor/contributor-guide/writing-essentials/markdown)で文書化されています。 詳細については、`write-experience-league-markdown`スキルを使用してください（存在する場合）。
* 送信されたすべての変更は、CIで自動化されたリンクチェックとリンク検証を通じて処理されます（以下を参照）。ルールが適用される、またはリンクを修正する必要があると仮定する前に、`markdownlint_custom.json`と`linkcheckexclude.json`を確認してください。

&#x200B;# 検証/CI

* `.github/workflows/validate-articles.yml`はPR上で実行され、`main`にプッシュされます（`retest`のPRコメントを介して）。共有された`Adobe-Enterprise-Docs/workflows`再利用可能なワークフローを呼び出して、マークダウンをリンクし、リンクを検証します。 このリポジトリにはローカルに対応するスクリプトはありません。CIは合格/不合格の真のソースです。
* `.github/workflows/mirror.yml`は、プッシュ時に公開リポジトリに`main`をミラーリングします。これはインフラストラクチャであり、コンテンツの変更が反映される必要はありません。
* `markdownlint_custom.json`は、共有されている`markdownlint.json`ルールセットを拡張し、Experience LeagueのカスタムMarkdown拡張機能（インラインHTML、非標準の強調など）と競合するいくつかのルール(MD005、MD007、MD018、MD032、MD033、MD034、MD037、MD040)を無効にします。 これらの無効なルールを満たすためにコンテンツを「修正」しないでください。
* `linkcheckexclude.json`は、リンクチェッカーがスキップするリンクパターン（現在`example.com`/`example-end.com`）をホワイトリストに登録します。

&#x200B;# 作業中の規則

* これはリリースノート重視のドキュメントです。リリースノートは`help/release-notes/`下にあり、バージョンごとに1つのフォルダー（例： `version-16-0`）に加えて、`all-changes`および`old-versions`のアグリゲーションページに格納されます。 新しいリリースを追加する場合は、既存のバージョンフォルダーにテンプレートとして従います。
