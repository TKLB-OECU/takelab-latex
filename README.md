# takelab_latex_env


# 初期設定
## 必要なソフトウェア
- Docker
- Node.js

## インストール
1. DockerとNode.jsがインストールされていることを確認してください。
2. go-taskをインストール
```bash
npm install -g go-task
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
