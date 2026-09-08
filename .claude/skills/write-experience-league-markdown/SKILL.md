---
name: write-experience-league-markdown
description: ""
Source: https://experienceleague.adobe.com/en/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: 824d0741467f908abf5aa8fd658cebe5b5c70b61
workflow-type: tm+mt
source-wordcount: '628'
ht-degree: 5%

---


# Experience Leagueマークダウンの書き込み

Experience Leagueがカスタムパイプラインを介してGitHubフレーバーのMarkdownをレンダリング
それには独自の拡張と描画の工夫がある。 標準のGFMはほとんど動作しますが、
以下の項目はExperience Leagueによって異なります。間違った内容を取得してください
ライブサイトでリンク/リンクチェックCIに失敗するか、またはレンダリングが正しく行われない。

## 見出し

* `#` ～ `#####` （レベル1 ～ 5） ページの`title`の前付
事実上レベル0です。本文の最初の「マークダウン」の見出しは、
単一の`# Level 1`見出しがページタイトルに一致しています（または近い位置にあります）。
* レベルを勝手にスキップしないでください。ミニ目次は見出しから生成されます。

## テキストの書式設定

* `**bold**`, `*italic*`, `***bold and italic***`.
* バックスラッシュを使用したエスケープリテラル特殊文字（`\*`、`\_`など）。
* 見出し/タイトルの&#x200B;**アンパサンド**&#x200B;は、(`and`)として書き出すか、エンコードする必要があります
  `&amp;` – タイトル内のRAW `&`は解析を中断できます。
* **山かっこ**&#x200B;を実際のHTMLではなくリテラルテキストとして使用する場合は、エンコードする必要があります：
  `<placeholder>` → `&lt;placeholder&gt;`。
* ワードプロセッサーからペーストされた&#x200B;**引用符の自動調節**&#x200B;は、エンコードする必要があります。エンコードしたままにすることはできません。
リテラルの中括弧：左ダブル`&#8220;`、右ダブル`&#8221;`、
アポストロフィ/右シングル`&#8217;`。

## リスト

* 番号付きリスト：すべてのアイテムを`1.` （または`1)`）で開始 – GitHub/Experience
入力されたリテラル数字に関係なく、リーグの自動番号。
* 箇条書きリスト： `*`、`-`、または`+`を使用しますが、**箇条書き記号の混在はできません
同じリスト/文書**&#x200B;内。
* `TOC.md`リストの入れ子には常に`+`が使用されます – 既存のファイルに従ってください
箇条書きスタイルは、別のスタイルを導入するのではなく、

## リンク

* 内部相互参照は、リンクへの&#x200B;**相対**&#x200B;マークダウンリンクである必要があります
ターゲット`.md`ファイル： `[Overview](../../overview.md)`。
* 外部参照は&#x200B;**絶対** URLである必要があります。
* 別のページの見出し/スパンにアンカーします：例： `#anchor-id`を追加します。
  `[Mesh](../../glossary/glossary.md#mesh)`.
* ページ内アンカーは、見出し（自動スラッグ）または
用語の直前の明示的な`<span id="anchor-id"></span>` —
このリポジトリ全体で使用されるパターンについては、`help/glossary/glossary.md`を参照してください。
* `TOC.md`セクションアンカーは、見出し/一覧の後に`{#section-id}`構文を使用します
ラベル（例： `Getting started{#getting-started}`）。

## 画像

* `![Alt text](path/to/image.png "Optional hover title")`.
* オプションのサイジング/最適化クエリパラメーターをサポート：
  `![Adobe logo](assets/logo.png?width=750&format=png&optimize=medium)`.
* **代替テキストにはアンダースコア**&#x200B;を含めることはできません。正しくレンダリングされません。
代わりにハイフンまたはスペースを使用してください。
* ページ固有の画像は`<page-name>.resources/`に表示されます。共有/アプリアイコン
`help/assets/`に住んでいます（CLAUDE.mdを参照）。

## 表

* パイプ区切り、ハイフンのヘッダー区切り行：

  ```markdown
  | Header | Another header | Yet another header |
  |--- |--- |--- |
  | row 1 | column 2 | column 3 |
  | row 2 | row 2 column 2 | row 2 column 3 |
  ```

* 表の前に空白行を挿入しないと、表として表示されません。
* 表には、複数の段落または複雑なブロックのコンテンツを
セル – このリポジトリでは、表のセル内に画像/リストが必要です(例：
`overview.md`の比較テーブル)、インラインHTMLに戻ります
(`<div>`, `<b>`, `<ul>`/`<li>`) （各`data-preserve-html="true"`）
タグを付けて、パイプラインがストリッピングしないようにします。 むしろ既存のパターンに従ってください
必要に応じて新しいインラインHTMLを発明するよりも

## コード

* インラインコード：1つのバックティック。
* フェンスで囲まれたブロック：3つのバックチック（オプションの構文用言語あり）
強調表示（` `&#x200B;``python `、` ``&#x200B;`javascript `など）

## メモ/警告ブロック

カスタムのブロック引用符構文、ブロックごとに1つのタイプ、間の空白のブロック引用符行
タグと本文：

```markdown
>[!NOTE]
>
>This is a standard NOTE block.

>[!TIP]
>
>This is a standard TIP.

>[!IMPORTANT]
>
>This is an IMPORTANT note.
```

サポートされている型： `NOTE`、`TIP`、`IMPORTANT`、`CAUTION`、`WARNING`、
`ADMINISTRATION`, `AVAILABILITY`, `PREREQUISITES`, `ERROR`, `INFO`, `SUCCESS`.

## ビデオの埋め込み

```markdown
>[!VIDEO](https://video.tv.adobe.com/v/29770/?quality=12)
```

## UICONTROLタグ

UI要素名（ボタンラベル、メニュー項目、フィールド名）をインラインで折り返し、
ローカリゼーションパイプラインは、移動された文字列をチェックすることを認識しており、次の文字列を検出します
英語のラベルがない場合は、英語のラベルに戻ります。

```markdown
Click [!UICONTROL Save] to apply changes.
Go to [!UICONTROL Tools] > [!UICONTROL Settings].
```

説明テキスト（メニュー）で参照されるすべてのリテラルUIラベルに使用します。
項目、ボタン名、ダイアログタイトル、パネル名など)。

## DNLタグ（「ローカライズしない」）

製品名、サードパーティの機能名、または必要な語句をラップします
絶対に機械移動しないでください：

```markdown
Use [!DNL Adobe Analytics] to track metrics.
The [!DNL Target] implementation requires configuration.
```

このリポジトリでは、`[!DNL Substance 3D Designer]`などの製品名に使用します。
ページごとの最初/目立つメンションの`[!DNL Substance 3D Sampler]`など、
既存のページと一貫性がある。

## インラインHTML

RAWHTMLが許可されています（このリポジトリの`markdownlint_custom.json`ではMD033が無効になります）
特にこのような理由で)が、確実に保存されるには、
タグに`data-preserve-html="true"`が含まれる場合のパイプライン。 インラインHTMLを予約
場合によっては、プレーンマークダウンは表現できません(テーブルセル内の画像/リスト、
`<span id="...">`個のアンカーがあります)。マークダウンの一般的な代用ではありません。

## 前付

が使用する正確なブロックについては、CLAUDE.mdの「ページの前付」の節を参照してください。
このリポジトリの通常のコンテンツページと、リポジトリレベルの`metadata.md`
継承フィールド。