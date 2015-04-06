---
title: 開發階段
---

# 開發階段

## Middleman 伺服器

Middleman 從一開始就把你的開發用檔案及上線用檔案分開。因此你可以在開發階段使用許多在上線階段不需要、或不想要的工具（例如
[Haml](http://haml-lang.com)、[Sass](http://sass-lang.com)、[CoffeeScript](http://coffeescript.org/)⋯⋯等等）。我們把這兩個環境分別稱為「開發階段」及「靜態網站」。

你在使用 Middleman 時，大部分的時間都會是在開發階段當中。

你可以在命令列下，在你的專案資料夾中啟動一個預覽用的網頁伺服器：

``` bash
$ cd my_project
$ bundle exec middleman server
```

這樣就會在本機啟動一個伺服器，網址為：`http://localhost:4567/`

你可以在 `source` 資料夾中建立或修改檔案，然後在這個預覽用的網頁伺服器中看看結果。

只要在命令列下按 `CTRL-C`，就可以結束這個預覽伺服器。

### 單用 middleman 指令

如果你單純使用 `middleman` 指令，而沒有在後面加任何命令，這樣也等同於啟動預覽伺服器。

``` bash
$ bundle exec middleman
```

這個跟執行 `middleman server` 的結果完全一致。

## LiveReload

Middleman 內建一個可以在你檔案修改時，自動重新整理瀏覽器的擴充功能。只要打開 `config.rb` 並加入：

``` ruby
activate :livereload
```

你的瀏覽器現在就會自動跟著被編輯的檔案重新整理了。

[HTML5 Boilerplate]: http://html5boilerplate.com
[SMACSS]: http://smacss.com
