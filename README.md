* `%HOME%\AppData\Roaming\pandoc` 以下に `templates`フォルダを作ってそこに入れる（`DATA-DIR` は `pandoc --version` より）
* `eu1lmr.fd` を読み込むところで時間がかかる => `fc-cache -fv` 実行
* YAML fromt matterは，
```
title: "日本語のタイトル"
author: "日本人名"
date: "`r format(Sys.time(), '%Y-%m-%d')`"
documentclass: bxjsarticle
output: 
  pdf_document:
    latex_engine: xelatex
    template: default_ja.tex
classoption: a4paper,xelatex,ja=standard
geometry: no
```
* なぜか，`keep_tex: true` が効かない