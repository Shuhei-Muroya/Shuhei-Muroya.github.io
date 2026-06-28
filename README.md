# 研究者ホームページ

シンプルな HTML/CSS で作った研究者向けの個人ホームページです。GitHub Pages で無料公開できます。

## ファイル構成

```
homepage/
├── index.html   … ページ本体（内容を編集する）
├── style.css    … デザイン（色・レイアウト）
├── images/      … 顔写真などの画像を置く
│   └── profile.jpg   （任意。置くと丸い写真が表示されます）
└── README.md    … このファイル
```

## 1. ローカルで確認する

`index.html` をダブルクリックしてブラウザで開くだけで表示を確認できます。

## 2. 内容を編集する

`index.html` を開き、次の箇所を自分の情報に書き換えてください。

- `室屋 修平 / Shuhei Muroya` … 名前
- `〇〇大学 …` … 所属・職位
- `your-email@example.com` … メールアドレス（2 箇所）
- Google Scholar / GitHub / ORCID の `href="..."` … 自分の URL
- About / Education / Research / Publications / Talks … 各セクションの本文
- 顔写真：`images/profile.jpg` に画像を置く（なければ「PHOTO」枠が出ます）

## 3. GitHub Pages で公開する

1. GitHub にログインし、新しいリポジトリを作成する
   - 個人サイトにするなら、リポジトリ名を **`ユーザー名.github.io`** にすると
     `https://ユーザー名.github.io` で公開されます。
   - 普通の名前（例 `homepage`）でも `https://ユーザー名.github.io/homepage/` で公開できます。
2. この `homepage` フォルダの中身（`index.html` など）をリポジトリのトップに置く。
   - ターミナルから：
     ```bash
     cd homepage
     git init
     git add .
     git commit -m "Initial homepage"
     git branch -M main
     git remote add origin https://github.com/ユーザー名/リポジトリ名.git
     git push -u origin main
     ```
3. GitHub のリポジトリ画面で **Settings → Pages** を開く。
4. **Source** を `Deploy from a branch`、**Branch** を `main` / `/ (root)` に設定して Save。
5. 1〜2 分待つと公開 URL が表示されます。

## カスタマイズのヒント

- 色を変える：`style.css` の上部 `:root { --accent: ...; }` を編集。
- セクションを増やす：`index.html` の `<section>` ブロックをコピーして使う。
- ダークモードは OS の設定に自動で追従します。
