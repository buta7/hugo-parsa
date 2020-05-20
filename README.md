# README

foresty(https://foresty.io)との連携らしいがよくわからない

## セットアップ

サイト作成

```shell
hugo new site hugo-parsa
```

レポジトリ初期化

```shell
cd hugo-parsa
git init
echo '*.bak' >> .gitignore
echo '*~' >> .gitignore
echo '*.orig' >> .gitignore
echo 'public' >> .gitignore
```

テーマ設定

```shell
cd themes 
git submodule add https://github.com/themefisher/parsa-hugo.git
```

サイト設定

```shell
cd hugo-parsa
cp -pr ./themes/parsa-hugo/exampleSite/{config.toml,static,content} .
```

config.toml

```toml
baseURL = "https://higebobo.github.io/hugo-parsa/"
languageCode = "ja"
title = "Hugo Parsa"
theme = "parsa-hugo"
publishDir = "docs"
```

> github pagesやnetlifyで使う場合はbaseURLのプロトコルはhttpsにすること

Githubレポジトリ作成後

```shell
git remote add origin git@github.com:higebobo/hugo-parsa.git
hugo
git add -A
git commit -m 'init'
git push -u origin master
```

Github>Settings>Gighub Pages>Source>master branch/docs folder

## 既存のレポジトリからクローンする場合

```shell
git clone git@github.com:higebobo/hugo-parsa.git higebobo-parsa
cd higebobo-parsa
git submodule update --init --recursive
```

## Link

* [Parsa Hugo Personal Blog Theme \| Hugo Themes](https://themes.gohugo.io/parsa-hugo-personal-blog-theme/)
