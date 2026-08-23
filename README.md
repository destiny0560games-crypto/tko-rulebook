# TKO鯖 10勝プラベ部 公式ルールブック

GitHub Pages で公開している静的サイトです。中身は `index.html` 1枚で完結しています。

**公開URL** → https://destiny0560games-crypto.github.io/tko-rulebook/

| ファイル | 内容 |
|---|---|
| `index.html` | ルールブック本体（CSS・JS・図版すべて内蔵） |
| `ogp.png` | Discord等にリンクを貼ったときに表示されるサムネイル |

アプリ本体（`my-sheet-app`）とは完全に切り離してあります。このリポジトリを見ても
アプリのURLは分かりませんし、ここを更新してもアプリは再デプロイされません。

---

## 公開手順（初回のみ）

### 1. リポジトリを作る

- Owner: `destiny0560games-crypto`
- Repository name: `tko-rulebook`
- Visibility: **Public**（無料アカウントでは Private だと Pages が使えないため）
- Add README / .gitignore / license: **すべてなし**

### 2. ファイルを置く（どちらか片方でOK）

#### 方法A: ブラウザだけで完結（おすすめ・git不要）

1. 作成直後のリポジトリ画面にある **uploading an existing file** のリンクを押す
   （既にファイルがある場合は **Add file → Upload files**）
2. このフォルダの `index.html` `ogp.png` `README.md` を**まとめてドラッグ＆ドロップ**
3. 下部の **Commit changes** を押す

ファイル3つだけなので、これが一番早くて確実です。

#### 方法B: コマンドラインで

このフォルダで PowerShell を開いて実行します。

```
git init
git add .
git commit -m "ルールブック V8.2 を公開"
git branch -M main
git remote add origin https://github.com/destiny0560games-crypto/tko-rulebook.git
git push -u origin main
```

### 3. Pages を有効にする

リポジトリの **Settings**（上部タブ）→ 左メニューの **Pages** を開き、

- Build and deployment / Source: **Deploy from a branch**
- Branch: **main** と **/ (root)** を選んで **Save**

保存すると画面上部に公開URLが表示されます。**初回は反映まで1〜3分**かかります。
すぐ開くと404が出ますが、少し待てば表示されます。

### 4. 確認

スマホから https://destiny0560games-crypto.github.io/tko-rulebook/ を開いて、
表示が崩れていないか確認してください。あわせてDiscordにURLを貼って、
サムネイル付きで展開されるかも見ておくと安心です。

---

## 更新のしかた

### ブラウザから

リポジトリで `index.html` を開き、右上の鉛筆アイコン（Edit this file）で直接編集 →
**Commit changes**。ファイルごと差し替える場合は **Add file → Upload files** で
同じ名前のファイルを上げれば上書きされます。

### コマンドラインから

```
git add .
git commit -m "ルールブック更新"
git push
```

どちらも1分ほどで反映されます。反映されないときはブラウザのキャッシュを疑ってください
（スマホなら一度タブを閉じて開き直すのが確実です）。

---

## 注意点

- **リポジトリ名を変えるとURLが変わります。** その場合は `index.html` 内の
  `og:url` と `og:image`（16〜17行目付近）も新しいURLに直してください。
  ここを直さないとDiscordのサムネイルが表示されなくなります。
- **Publicリポジトリなので中身は誰でも閲覧できます。** 公開予定のルールブックしか
  入っていないので問題ありませんが、パスワードや管理用の情報は絶対に置かないでください。

## 補足

- **スマホ対応済み**：iPhone / Android どちらのブラウザでもそのまま読めます。
  HTMLファイルを直接送るとiPhoneで開けないことがありますが、URLなら問題ありません。
- **PDFにしたい場合**：ブラウザで開いて印刷 → PDFとして保存。
  印刷時は上部バーと目次、背景装飾が自動的に外れるようにしてあります。
- **ダークモード対応**：閲覧者の端末設定に追従して配色が切り替わります。
- **外部通信**：Webフォント（Google Fonts）のみ読み込みます。
  それ以外の通信はなく、閲覧者の情報を収集する仕組みは入っていません。
