---
title: 変更履歴リンクを追加した
date: 2023-04-16
draft: false
tags: ['hugo']
---

右上に「変更履歴」リンクを追加した。現在は[Archie](https://github.com/athul/archie)というテーマを使用しているので(CSSは一部[custom.css](https://github.com/kozmof/kozmof.github.io/blob/main/assets/css/custom.css)で変更している)、これをフォークして`head.html`に下記を追加した。
```html
{{- $githubHistory := $.Site.Params.historyBaseURL }}
{{ with .Page.File }}
    {{- $currentRelPath := .Path -}}
    <a class="change-history" alia-label="See change histories of this page" href="{{ print $githubHistory $currentRelPath }}">変更履歴</a>
{{ else }}
    <a class="change-history" alia-label="See change histories of this page" href="{{ print $githubHistory }}">変更履歴</a>
{{ end }}
```
各投稿ページではGitHubのそれぞれの変更履歴に飛び、トップページやタグ一覧では全体の変更履歴に飛ぶようになっている。
`historyBaseURL`は`config.toml`で下記のように定義できる。
```toml
[params]
historyBaseURL = "https://github.com/kozmof/kozmof.github.io/commits/main/content/"
```
