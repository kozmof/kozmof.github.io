---
title: ブログをつくった
date: 2022-07-25
draft: false
tags: ['hugo']
---

とくに記録的な文章を書いてなかった 2、3 年の間に世の中が変わりまくっていて、後から振り返られる文章を書く習慣がなかったことが悔やまれるので、今からでも記憶の断片化をどうにかしようということでブログをつくった。

## 構成

GitHub Pages + GitHub Actions + Hugoでpush後はデプロイまで全任せすることにした。

執筆はiPhone経由の場合はWorking Copyを使う。 この文章もiPhoneで書いている。

## 作業記録

- エディタ上でプレビューできる画像のパスとビルド後に参照可能なパスが変わるため、投稿用ディレクトリ内にあるファイルの`/static/static/img`をビルド前に`/img`に書き換える処理をGitHub Actionsに追加した。他にいい方法があるかもしれない。
- ActionをSHA-1 checksum指定にした。
- 使っているthemeがsubmoduleを再帰的に取得する必要があるものだったのでgh-pages.ymlで`submodules: recursive`を指定した。

### やりたいこと

- 日本語の文章用のlinterを入れるかつくるかする
- 更新日時の表示
- push時の日時を使う
 