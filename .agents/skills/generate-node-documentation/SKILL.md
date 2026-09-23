---
name: generate-node-documentation
description: |
  help/compositing-nodes/nodes-reference-for-com/node-library/で使用されている標準グラフと一致するようにSubstance 3D Designerのノード参照ページを作成する方法。 このスキルは、そのノードライブラリツリーの下のノードページ（ノードの説明、入力、出力、パラメーター、または例）や、同等のfunction-node / atomic-nodeリファレンスページを作成または編集する場合に使用します。 フォルダー/目次規則、最少前付、アイコン/説明テーブル、アンカー付き入力/出力/パラメータテーブル、およびサンプルギャラリーを取り上げます。 Adobe Experience Leagueマークダウンの一般的なルール（コールアウト、リンク、UICONTROL/DNL、イメージ）では、write-experience-league-markdownスキルを使用します。このスキルでは、ノードページ構造のみを対象とします。 正規の例： help/compositing-graphs/nodes-reference-for-com/node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md
source-git-commit: ed17c57a1aa9669a602d4523bdef20cd7d82db75
workflow-type: tm+mt
source-wordcount: '976'
ht-degree: 3%
---

# ノードのドキュメントの生成

このリポジトリ内のすべてのリーフノード参照ページは、一貫した1つの構造に従います。 この
skillはその構造の仕様です。 標準的で十分に機能している例を以下に示します。
`.../node-library/texture-generators/patterns/shape-splatter-v2/shape-splatter-v2.md` —
疑わしい場合は、それを開いて鏡に映します。

このスキルは、ノードページ&#x200B;*構造*のみを対象としています。 ベースExperience Leagueマークダウン用
(メモ/アラートブロック、絶対リンクと相対リンク、UICONTROL/DNL、イメージクエリパラメーター、
lint gotchas) `write-experience-league-markdown`のスキルに従ってください。

## ノードページが存在する場所（フォルダー/目次規則）

* 一致するカテゴリ/サブカテゴリパスの下のノードごとに1つのフォルダー。例：
  `.../node-library/<category>/<subcategory>/<node-name>/<node-name>.md`.
* フォルダー名はkebab-caseノードタイトルで、**one** `.md`ファイルが含まれています
同じ名前だった
* ページのすべての埋め込みメディア（アイコン、画像、GIFなど）は、**兄弟に存在します
  `.md`の横の`<node-name>.resources/`フォルダー&#x200B;**は、次のURLで参照されています：
  相対パス（例： `<node-name>.resources/<file>.png`）。 ノードページをポイントしない
  共有`help/assets/`フォルダー – 従来のパターンが段階的に廃止されています；新規および
  編集されたページは独自の`.resources`フォルダーを使用します。
* 各ページには、`help/guide/TOC.md`に対応するエントリがあります。 エレメントを追加または移動する場合
`TOC.md`とフォルダーレイアウトを一緒に更新します（AGENTS.mdのフォルダー/目次を参照）
規約)。

## 前付

ノードページは&#x200B;**minimal**&#x200B;ブロックを使用します – `title`とブレッドクラム形式のみ
`description`. (これは、11フィールドのレガシーブロックAGENTS.mdドキュメントとは異なります。
通常のコンテンツページ)

```yaml
---
title: "Shape splatter v2"
description: "Designer > Substance compositing graphs > Nodes reference for Substance compositing graphs > Node library > Generator > Pattern > Shape splatter v2"
---
```

## ボディ構造

上から下、前付の下のすべてのアイテム：

### &#x200B;1. H1タイトル

単一の`# <Node title>` - 1ページにつき1つのH1。

### &#x200B;2. アイコン/説明テーブル

1つのHTMLテーブル、1つの行、2つのセル。 左のセル(`33.33%`)にはアイコンが保持され、次に
`In:`個のブレッドクラム。右のセル(`100.00%`)には`## Description`と散文が含まれています。

```html
<table>
<tr style="border: 0;">
<td width="33.33%" style="border: 0;" valign="top">

![<Node title> icon](<node-name>.resources/<node-name>.png "<Node title>")

<b>In:</b> <Category> &gt; <Subcategory>

</td>
<td width="100.00%" style="border: 0;" valign="top">

## Description

<Description prose.>

</td>
</tr>
</table>
```

説明セルのプロス規則：
* `<br><br>`で段落を区切る（セル内の生の空白行は信頼できません）。
* インライン強調は`<b>…</b>` / `<i>…</i>`です。
* リードイン補助では、文の先頭に`<i>Note:</i>` / `<i>Tip:</i>`を使用します。
* `In:`行の`>`に`&gt;`を使用します（これはHTML内にあります）。 カテゴリを選択/
サブカテゴリ名は、ノード自体から取得します。作成しないでください。
* 複数のバージョンを持つノードの場合（例：カラー/グレースケール/値または番号バリアント）
セル 1/セル 2)と同様に、他の段落を参照する最後のdescription段落を追加します
1行の改行で区切られた相対リンクを持つバージョン。 例： &grave;See also: [&#128279;](../input-grayscale/input-grayscale.md)Input
grayscale, [Input value](../input-value/input-value.md)&grave;。

### &#x200B;3. オプションのコールアウト

`>[!INFO]`、`>[!TIP]`、`>[!NOTE]`などは、アイコン/説明テーブルの&#x200B;**後**&#x200B;に移動します（移動しません）
（セル内）。 `write-experience-league-markdown`スキルごとの構文です。

### &#x200B;4. 入力

ノードに入力ピンがある場合にのみ含めます。 見出しの前にアンカーを付けます。

```markdown
<a name="inputs"></a>

## Inputs

|  |  |
|:---|:---|
| <b>Background height</b> <i>Grayscale</i> | The base height map in which shapes are scattered.<br><br>The contribution is controlled by the <b>Background input opacity</b> parameter. |
```

* 2つの列、空の見出し行、`|:---|:---|` アラインメント。
* 入力ごとに1行：左のセル`<b>Name</b> <i>Type</i>`、説明の右のセル。
* 型マーカーはHTMLの斜体です – `<i>Type</i>` – マークダウン`*Type*`ではありません。

### &#x200B;5. 出力

入力と同じシェイプで、`<a name="outputs"></a>` + `## Outputs`です。 次の場合にのみ含める：
ノードは個別の出力をドキュメント化します（多くのノードは単一の暗黙的な出力を持ち、これを省略します）
section — 1つは作成しないでください)。

パックされたマルチチャンネル出力の場合、`<br>`でチャンネルを分割し、インデントします
`&nbsp;`を持つサブポイント(
参照):

```markdown
| <b>Splatter UVW</b> | <b>R</b> - U component of the shapes' UVs.<br><b>G</b> - V component of the shapes' UVs.<br><b>B</b> - The shapes' height. (W)<br><b>A</b> - Packed data:<br>&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;- <i>Integer part:</i> The shapes' unique identifier. |
```

### &#x200B;6. パラメーター

`<a name="parameters"></a>` + `## Parameters`の同じテーブル図形です。 全体を省略する
ノードにパラメータがない場合（空のテーブルまたは「パラメータなし」を生成しない）
行)。

* **グループ化されたパラメーター**：右側のセルが空白のスパンラベル行を
グループの行：

  ```markdown
  | <b>Positioning</b> |  |
  | <b>Project Input</b> <i>UV Position, World Space Position</i> | Choose whether the projection position is set in 2D/UV or in 3D/World space. |
  ```

* **列挙/マルチオプション値**：説明セル内のオプションを
  `<br>`で区切られたダッシュの一覧：

  ```markdown
  | <b>Position distribution mode</b> <i>Integer</i> | The method of distributing the shapes:<br><br>- <b>2D grid:</b> A simple uniform grid.<br>- <b>Poisson disc:</b> Randomly offsets grid cells to prevent overlaps.<br>- <b>Uniform:</b> An even distribution of a set number of shapes. |
  ```

### &#x200B;7. 例

サンプルの画像/GIFがある場合にのみ含めます。 フチなし、固定レイアウトのHTMLを使用する
ギャラリーテーブル。1つの画像につき1つの`<td>`。3つの画像の後に新しい`<tr>`に折り返します。 メディアパス
ページの`.resources`フォルダーをポイントします。 HTML `<img>`要素を使用する間隔
例えば`class="modal-image"`を使用すると、公開された画像が標準で開きます
画像ビューア。 ノードと例を識別する意味のある`alt`テキストを指定してください
数値。 このギャラリーでは、マークダウン画像の構文を使用しないでください。

```html
## Examples

<table style="table-layout:fixed">
    <tr style="border: 0;">
        <td style="border: 0;">
            <img src="<node-name>.resources/<file>.gif" class="modal-image" alt="<Node title> - Example 1" />
        </td>
        <td style="border: 0;">
            <img src="<node-name>.resources/<file2>.jpg" class="modal-image" alt="<Node title> - Example 2" />
        </td>
    </tr>
</table>
```

テーブルの`style="table-layout:fixed"`と `style="border: 0;"`
属性を正確に示しています。境界線、余白、背景スタイルを追加しないでください。
最後の行の一部が塗りつぶされている場合、その行の後続セルは空白のままにする
(`<td style="border: 0;"></td>`)で、折り返しではありません。 既存の画像を使用
順序とファイル名 ページにキャプションがある場合は、キャプションを`alt`テキストとして保存してください
表示されているキャプションのマークアップを追加する必要があります。 ページにセクションがない場合は、セクション全体を省略します。
メディアの例

## 正規型の値

ノード独自の型表現を再利用します。一般的な値： `Grayscale`、`Color`、`Integer`、
`Float`, `Float2`, `Float3`, `Float4`, `Integer2`, `Boolean`, `Grayscale Input`,
`Color Input`, `(Color value)`, `(Grayscale value)`. 文字を考案したり「標準化」したりしないでください
ノードは実際には使用しません。

## 表セルの罫線

* テーブルセル内に未加工の改行がありません – `<br>` （および`<br><br>`）で行を結合します
段落)。
* セル内の強調は`<b>`/`<i>`で、型マーカーは常に`<i>Type</i>`です。
* `&nbsp;`シーケンスの入れ子になったサブポイントをインデントします。

## ルール/注意事項

* **ノードが持たない入力、出力、またはパラメーターを作成しないでください**。以下を省略してください。
代わりにセクションを使用します。 既存の技術コンテンツを書き換えたり、要約したり、削除したりしないでください。ただしその機能は
形式を変更します。
* **他の`.md`ページに対する相対リンク**&#x200B;を維持します。外部リンクは絶対リンクです。
* 古いページをこの形式に編集するときに&#x200B;**レガシークレジットを削除**：難易度タグ
(`**Simple**` / `**Intermediate**` / `**Complex**`)、冗長 `## <Title>`
アイコンセル内の小見出し、「画像が添付されていません」のようなスタブ文
このページ。」および以前の移行で残された空のナビゲーション/ラッパーテーブル。
* **1ページにつき1つのH1**。セクションでは`##`を使用し、入力/出力/パラメーターのアンカーを使用します
(`inputs` / `outputs` / `parameters`)は、見出しの前に付ける必要があるため、ページを横断できます
  `#inputs`個のリンクが解決されます。
* ページの追加、名前の変更、移動を行う場合は、**`TOC.md`の同期を維持**&#x200B;します。
