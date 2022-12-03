---
title: AeroSandbox をインストールする
date: 2022-12-03
draft: false
tags: ['f1', 'python', 'aerosandbox']
---

F1 のシーズンが終わってしまったので、なにか F1 っぽいものをということで見つけた空力シミュレーションライブラリの `AeroSandbox` を入れてみた。ふつうにインストールすると依存先の `xfoil` で `zip_save` がないというエラーが原因でインストールできなかったので、ワークアラウンドをメモする。

### AeroSandbox

https://github.com/peterdsharpe/AeroSandbox


### 実行環境

```
- Pop!_OS 22.04 LTS (ベースが Ubuntu なので Ubuntu と変わらないはず)
- Python 3.10.6 (venv で環境をつくっているが venv の構築手順は割愛する)
```

### インストール手順

1. `zip_save` がないというエラーは https://github.com/DARcorporation/xfoil-python/pull/18 で対応済みだったので、ワーキングディレクトリで、 `git clone https://github.com/DARcorporation/xfoil-python.git` する

2. `xfoil` のインストールには `gcc` と `gfortran` がいるのでそれぞれインストールする。

```
sudo apt install build-essential
sudo apt install gfortran
```
3. クローンしたディレクトリに移動して `xfoil` を単体でインストールする。

```
cd xfoil-python
pip install .
```

5. `AeroSandbox` をインストールする。

```
pip install aerosandbox[full]
```

### 動作確認

チュートリアルが用意されているので、それで確認する。
```
git clone https://github.com/peterdsharpe/AeroSandbox.git
cd AeroSandbox/tutorial/
jupyter notebook
```
Jupyter Notebook 上で挙動を確認できる。


### その他
PR で OpenVSP に対応したというリクエストが上がっているので、これを使えば OpenVSP のデータが使えるかもしれない。
https://github.com/peterdsharpe/AeroSandbox/pull/60

#### OpenVSP
https://openvsp.org/

