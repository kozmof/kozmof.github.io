---
title: ブログをつくった
date: 2022-07-25
draft: false
tags: ['hugo']
---

とくに記録的な文章を書いてなかった 2、3 年の間に世の中が変わりまくっていて、後から振り返られる文章を書く習慣がなかったことが悔やまれるので、今からでも記憶の断片化をどうにかしようということでブログをつくった。

## 構成

GitHub Pages + GitHub Actions + Hugo で push 後はデプロイまで全任せすることにした。

執筆は iPhone 経由の場合は Working Copy を使う。 この文章も iPhone で書いている。

## 作業記録

- エディタ上でプレビューできる画像のパスとビルド後に参照可能なパスが変わるため、投稿用ディレクトリ内にあるファイルの `/static/static/img` をビルド前に `/img` に書き換える処理を GitHub Actions に追加した。他にいい方法があるかもしれない。
- Action を SHA-1 checksum 指定にした。
- 使っている theme が submodule を再起的に取得する必要があるものだったので gh-pages.yml で `submodules: recursive` を指定した。

## やりたいこと

- 日本語の文章用の linter を入れるかつくるかする
- 更新日時の表示
- push 時の日時を使う
 