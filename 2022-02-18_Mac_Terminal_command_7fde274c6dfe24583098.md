<!--
title:   これだけ知っておけば開発で困らない最強コマンド一覧
tags:    Mac,Terminal,command
id:      7fde274c6dfe24583098
private: false
-->
ここをおさえておけばひとまず開発に困ることはないであろう，というコマンドの一覧です．（※Macでのコマンドです）
**基本的には相対パスによってディレクトリを指定します．** また，Tabキーを押せば補完機能なども使えると思います．

 - 作成
    - mkdirコマンド
    - touchコマンド
 - 移動
    - cdコマンド
    - mvコマンド
 - 確認
    - pwdコマンド
    - lsコマンド
    - catコマンド
 - コピー
    - cpコマンド
 - 削除
    - rm（-r）コマンド
 - おまけ


# 作成
### ディレクトリ作成

```zsh
$ mkdir sample（ディレクトリ名）
```

### ファイル作成

```zsh
// ファイルを作成したいディレクトリ下で
$ touch sample.txt(ファイル名)
```


# 移動
**※ファイルへの移動は不可**
### 指定のディレクトリへの移動

```zsh
// 同じ階層への移動
$ cd sample（ディレクトリ名）
$ cd sample/sample/    ← ディレクトリの中のディレクトリを指定


// 一つ上の階層への移動
$ cd ..
$ cd ../sample（ディレクトリ名）


// 二つ以上の階層への移動
$ cd ../../
$ cd ../../../sample/sample
```

### ディレクトリやファイルそのものを移動させる

```zsh
// "sample.txt"ファイルを，"sample-directory"ディレクトリに移動
$ mv sample.txt sample-directory

// "sample-directory"ディレクトリを，"work-directory"ディレクトリに移動
$ mv sample-directory work-directory
```


# 確認
### カレントディレクトリまでのパス

```zsh
// どこかのディレクトリ上で
$ pwd
（出力例） /Users/user-name/Documents/work/sample
```

### カレントディレクトリの内容を確認

```zsh
// ホーム，またはどこかのディレクトリ上で
$ ls
（出力例） sample  qiita.txt  learnig_python.txt
view.html  main.go  animal  banana.txt
```

### 指定のファイルを閲覧

```zsh
$ cat sample.txt（ファイル名）

（出力例）
aaaa
bbbb
nyan-nyan-nyan
```


# コピー

```zsh
// "banana.txt"ファイルを，"sample.txt"にコピーする
$ cp banana.txt sample.txt

// "banana"ディレクトリを，"sample"ディレクトリにコピーする
$ cp banana sample
```

**※ファイル → ディレクトリ / ディレクトリ → ファイルのコピは不可**


# 削除

```zsh
// "sample.txt"を削除
$rm sample.txt

// ディレクトリの削除には「-r」を付ける
$ rm -r sample-directory
```

# おまけ
### mvコマンドで改名

```zsh
// "banana.txt"を"apple.txt"に改名
// もちろんディレクトリにも使えます
$ mv banana.txt apple.txt
```