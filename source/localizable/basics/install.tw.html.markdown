---
title: 安裝
---

# 安裝

Middleman 是經由 RubyGems 套件管理系統發佈的。因此你必須先安裝好 Ruby 語言的執行階段 (runtime) 與 RubyGems，才能開始使用 Middleman。

Mac OS X 已經在系統上預載好了 Ruby 跟 RubyGems。但是在 Middleman 安裝時，會需要編譯一些必要的組件──在 OS X 上你會需要 Xcode 來做編譯。你可以在 [Mac App
Store](http://itunes.apple.com/tw/app/xcode/id497799835?ls=1&mt=12&l=zh) 上安裝 Xcode。或者如果你有免費的 Apple 開發者帳號，也可以直接從他們的[下載網頁](https://developer.apple.com/downloads/index.action)取得並安裝「Command Line Tools for Xcode」即可。

在 Ruby 跟 RubyGems 都安裝好之後，請在命令行執行下列指令：

```bash
$ gem install middleman
```

這樣就可以安裝 Middleman 與其依存套件、以及供你操作 Middleman 的命令行工具。安裝程式會幫你的命令行環境新增一個指令，提供你三個好用的功能：

```bash
$ middleman init
$ middleman server
$ middleman build
```

在下一篇《[建立新網站](/tw/basics/start_new_site)》中，我們會講解這些指令的使用方式。
