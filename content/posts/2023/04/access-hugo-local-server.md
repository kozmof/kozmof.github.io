---
title: モバイルで無線LAN内のHugoサーバーにアクセスする
date: 2023-04-16
draft: false
tags: ['hugo']
---

ホストのIPアドレスを取得する。
```sh
hostname -I
```
取得したアドレスを指定してサーバーを起動する。
```sh
hugo server --bind 192.168.xx.xx --baseURL http://192.168.xx.xx
```
モバイル側でホストと同じ無線LANに接続し、取得したアドレスとサーバー起動時のポートをブラウザで指定する。
```
http://192.168.xx.xx:yyyy
```
