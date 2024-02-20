#  卒業論文・修士論文 テンプレート @Takelab


## Updated
2024-02-14: Released v1.95 - edited by Yuta Nakamura (中村 勇太)

2024-02-02: Released v1.94 - edited by Wakana HASHIMOTO (橋本 和奏)

2020-02-01: Released v1.9x - edited by Yutaka TAKESUE (竹末 裕)

2018-02-01: Released v1.9x - edited by Yoshiki MASHIMA (間嶋 義喜)

2016-02-01: Released v1.9x - edited by Takuya OKADA (岡田 拓也)

2010-02-28: Released v1.93 - edited by Tatsuya YAMAMOTO 


## Usage

### 表紙のタイトル，著者等について
タイトル，著者等の情報は構成ファイル(main.tex)のプリアンプルにて，
```latex
        \title{},\id{},\author{},\professer{},\date{}
```
の各項目に書き込むだけでよいため，styleファイル (**sty/dep-title.sty**) に直接書き込む必要はない．

### 卒業論文・修士論文との切り替え
styleファイル (**sty/dep-title.sty**) のコメントアウト部分で制御する．


# 初期設定
## 必要なソフトウェア
- git
- Docker
- Node.js

## リポジトリのフォーク
```bash
git clone --bare https://github.com/TKLB-OECU/takelab-paper-latex
cd takelab-paper-latex.git
# ここでgithub上のprivateリポジトリを作成しておく
git push --mirror git@github.com:自分のgithubnのユーザー名/作成したリポジトリ名
cd ../
rm -rf takelab-paper-latex.git
```

## インストール
1. DockerとNode.jsがインストールされていることを確認してください。
2. go-taskをインストール
```bash
npm install -g @go-task\cli
```
3. ターミナルで以下のコマンドを実行
```bash
task init
```


# How to use
## 文章チェックの実行
```bash
task lint
```

## draw.ioの書き出し
```bash
task drawio
```

## LaTeXのコンパイル
```bash
task latex
```

## Dockerコンテナの再起動
```bash
task dc_restart
```

# Textlint について
## 必須（絶対に使用するべき）
- textlint-plugin-latex2e

LaTeXの文書に対してtextlintを行うためのプラグイン

- textlint-rule-preset-ja-spacing

スペースの使い方に関するルール

- textlint-rule-preset-ja-technical-writing

技術文章向けのルール。
複数のルールが含まれている、詳細は[こちら](https://github.com/textlint-ja/textlint-rule-preset-ja-technical-writing?tab=readme-ov-file#%E3%83%AB%E3%83%BC%E3%83%AB%E4%B8%80%E8%A6%A7)

- textlint-ja/textlint-rule-no-synonyms

表記揺れをチェックする。
例えば「インターネット」と「ネット」など、
専門的な用語については精度低め。

- sudachi-synonyms-dictionary

表記揺れをチェックするための辞書

- textlint-rule-no-mixed-zenkaku-and-hankaku-alphabet

全角文字と半角文字が混在しているかチェックする。


## 任意


- textlint-rule-spellcheck-tech-word

技術系の単語のスペルミスをチェックする。
