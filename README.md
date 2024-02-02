#  卒業論文・修士論文 テンプレート @Takelab


## Updated
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