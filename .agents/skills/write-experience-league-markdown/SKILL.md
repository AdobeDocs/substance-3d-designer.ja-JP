---
name: write-experience-league-markdown
description: |
  Adobe Experience Leagueで公開されたMarkdownコンテンツを記述するための構文規則、カスタム拡張、およびgotchas。 このスキルは、このリポジトリ（またはその他のExperience Leagueコンテンツリポジトリ）のhelp/の下に見出し、リンク、画像、表、メモ/アラートブロック、UICONTROL/DNLタグ、ビデオ埋め込み、アンカー、既知のレンダリングの落とし穴などのページを作成または編集する場合に使用します。 出典： https://experienceleague.adobe.com/ja/docs/contributor/contributor-guide/writing-essentials/markdown
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '1263'
ht-degree: 4%
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
用語の直前の明示的な`<span id="anchor-id"></span>` (HTML) / `{: #anchor-id}` （マークダウン） —
このリポジトリ全体で使用されるパターンについては、`help/glossary/glossary.md`を参照してください。
* `TOC.md`セクションアンカーは、見出し/一覧の後に`{#section-id}`構文を使用します
ラベル（例： `Getting started{#getting-started}`）。

## 画像

可能な限りMarkdownイメージ構文を使用してください。

```markdown
![Alt text](path/to/image.png "Optional hover text")
```

* `![...]`テキストにはアクセス可能な代替テキストが必要です。 簡潔にして
アンダースコアは使用しないでください。代わりにスペースまたはハイフンを使用してください。
* イメージパスは、Markdownファイルに対する相対パス、またはルートに対する相対パスで指定できます
`/help/assets/shared-image.png`として。 ページ固有の画像は
兄弟`<page-name>.resources/`フォルダー(例：
  `<page-name>.resources/image.png`). `help/assets/`は従来の共有フォルダーです。
  ページ固有の新しい画像をそこに追加しないでください。
* オプションのイメージクエリパラメーターを使用して、CDN処理を制御できます。
  `?width=750&format=png&optimize=medium`. これらのパラメーターを画像に保持する
  プロパティブロックの前のURL。
* 閉じる`)`の直後に画像のプロパティを追加する：
  `![Alt text](image.png "Hover text"){width="300" align="center"}`.
  `width`は表示エリアのピクセル値またはパーセンテージです。画像スケール
均等に サポートされているアラインメント値は`center`および`right`です。
  `valign`はサポートされていません。
* `modal="regular"`または`zoomable="yes"`を使用して、画像をクリックしてズームします：
  `![Alt text](image.png){width="100" zoomable="yes"}`. 結合しない
  画像リンクを使用してクリックしてズームします。ハイパーリンクが優先されます。
* 画像を別のページにリンクするには、画像をMarkdownリンクでラップします。
  `[![Alt text](image.png)](../target/target.md)`.
* 大きな画像の場合は、実際には、最低でも640ピクセルのソース幅を指定してください。
必要な場合を除き、約2000ピクセル以下のピクセルを使用し、画像ファイルを
可能であれば5 MB パイプラインでは、最大100 MBのファイルを受け入れますが、ファイルは
検証に失敗した場合は20 MBです。通常、アーティクルに含める最大サイズは
100枚の画像（一部の古いガイダンスでは200と表示されています。より厳格な制限を適用してください）。

HTMLは、マークダウンが
特殊な表またはカスタムのインラインプレゼンテーション サポートされているHTML画像フォーム
は：

```html
<img src="image.png" alt="Alt text" />
```

* 常に意味のある`alt`属性を指定し、relativeまたは
マークダウンイメージと一致するルート相対`src`。
* 保存されたインラインHTML内のHTML画像については、
  `data-preserve-html="true"`を含むタグに追加します（必要な場合）
  周囲のマークアップ。 以下に例を示します。

  ```html
  <div data-preserve-html="true" align="center">
    <img src="my-page.resources/preview.gif" alt="Preview" />
  </div>
  ```

* HTML画像に対してクリックしてズームを有効にするには、
  `<img>`タグの`class="modal-image"`。
* サポートされていないHTML属性を使用したり、`valign`に依存したりしないでください。マークダウンを推奨します
幅とアラインメントのプロパティ。

## 表

通常の表形式のコンテンツには、ネイティブのマークダウンテーブルを使用します。

```markdown
| Header | Another header | Yet another header |
|--- |--- |--- |
| row 1 | column 2 | column 3 |
| row 2 | row 2 column 2 | row 2 column 3 |
```

* テーブルの前に空行を入れなさい。 マークダウンテーブルには、少なくとも1つ必要です
ヘッダー行と1つのボディ行。1行またはヘッダーなしの場合はHTML表を使用します。
テーブルです。
* 各ヘッダーセパレータセルには最低3つのハイフンを使用し、同じハイフンは使用しない
各行のパイプ文字の数。 `\|`としてリテラルパイプをエスケープするか、
  `&vert;`.
* 必要に応じて、区切り行にアラインメントマーカーを使用します。
  左、中央、右のアラインメントの`|---|:---:|---:|`。
* 段落の区切りのマークダウン表セルでインラインHTMLがサポートされています。
基本的なリスト。 `<p>`を段落ごとに使用し、`<br>`を改行に使用します。
  `<ul>`/`<ol>` （リストのアイテム数： `<li>`）。 追加
  `data-preserve-html="true"`は、必要なときにHTMLエレメントをインライン化します
  リポジトリのマークアップを囲んでいます。

  ```markdown
  | Header | Details |
  |---|---|
  | Text | First paragraph.<p>Second paragraph.<br>New line.<ul><li>Item</li></ul> |
  ```

* 幅と高さが非常に広いテーブルは避けてください。移動が困難です。
長いコードは強制実行される可能性があるため、表にインラインコードを含める場合は注意が必要です
不釣り合いな列幅
* マークダウン表の表レイアウトを選択するには、
空白行で区切られた表：

  ```markdown
  {style="table-layout:fixed"}
  ```

  長いテキストまたはコードに柔軟性が必要な場合は`table-layout:auto` （既定）を使用する
  列幅： 含んでいるテーブルなど、バランスの取れた列には`fixed`を使用します
  同じサイズの画像

マークダウンが必要な構造を表現できない場合に、HTMLテーブルを使用します。例えば、
ヘッダーの省略、スパンを持つセルの結合、列の均等配置、または整列
セル内の内容：

```html
<table style="table-layout:fixed">
  <tr>
    <th>Property</th>
    <th>Value</th>
  </tr>
  <tr>
    <td align="center">Example</td>
    <td>Details</td>
  </tr>
</table>
```

* サポートされているテーブル要素は`<table>`、`<tbody>`、`<thead>`、`<tfoot>`です。
  `<tr>`、`<th>`、`<td>`、`<col>`および`<colgroup>`、およびサポートされている
`<p>`、`<br>`、`<b>`、`<i>`、`<ul>`、`<ol>`などのインライン要素
  `<li>`.
* HTMLテーブル内ではマークダウン構文を使用しないでください。 例えば次のようになります：マークダウン
メモ、画像、リンクは文字通りレンダリングされる場合があります。代わりにHTML構文を使用してください。
  `UICONTROL`および`DNL`のローカリゼーションタグは例外です。
* セルで`align="left"`、`align="center"`、または`align="right"`を使用する
必要です。 HTML表にはネストされた表を含めることはできません。
* 開始タグにHTMLテーブルレイアウトを設定します。
  `<table style="table-layout:auto">`または
  `<table style="table-layout:fixed">`.
* 境界線のない1行のHTMLテーブルの場合は、
  `<tr style="border: 0;">`.

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

Experience Leagueでは、`[!VIDEO]`ブロックにMP4またはYouTubeビデオを直接埋め込むことはできません。 アニメーションプレビューが必要な場合は、代わりにページの兄弟`.resources`フォルダーのGIFを使用し、必要に応じてインラインHTMLの中央に配置します。

```markdown
<div data-preserve-html="true" align="center">
  <img src="my-page.resources/my-preview.gif" alt="My preview" />
</div>
```

ローカルMP4ファイル、リモートMP4ファイル、またはYouTube URLに`[!VIDEO]`を使用しないでください。公開パイプラインでそれらを拒否し、CIが失敗します。

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

で使用される正確なブロックについては、AGENTS.mdの「ページの前付」のセクションを参照してください。
このリポジトリの通常のコンテンツページと、リポジトリレベルの`metadata.md`
継承フィールド。