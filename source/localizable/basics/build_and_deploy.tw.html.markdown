---
title: 建置與發佈
---

# 輸出你的靜態網站

## 使用 "middleman build" 建置網站

當你終於準備好要產生你的靜態網頁、或是要架設你的靜態網誌時，你會需要建置你的網站。在命令列下，切到你的專案資料夾後，請執行 `middleman build` 指令：

``` bash
$ cd my_project
$ bundle exec middleman build
```

這樣就會把每個放在 `source` 裡面的檔案，都建立一個對應的靜態檔案並輸出到 `build` 資料夾。Middleman 會編譯你的樣板檔案、複製一份本來就是靜態的檔案、接著會執行所有在建置階段被啟用的功能（例如壓縮功能）。同時在 `build` 如果留有之前產生的、但是這次已經用不到的檔案，也會被自動清掉。

## 發佈你的網站

在建置完你的網站後，所有你上線需要的東西就已經都在你的 `build` 目錄內了。發佈靜態網站的方法有接近無限多種，所以我們在這裡推薦你可以逛逛我們的[擴充功能目錄][1]。裡面有更多發佈 `middleman` 網站的方法。如果你是一套適合發佈 `middleman` 網站的發佈工具作者，[請來這裡][2]發 Pull-request 給我們。

[`middleman-deploy`][3] 是一套非常方便的發佈工具，它可以透過 rsync、ftp、sftp 或是 git 的方式幫你發佈你的網站：

```bash
$ middleman build [--clean]
$ middleman deploy [--build-before]
```

[1]: https://directory.middlemanapp.com/#/extensions/deployment
[2]: https://github.com/middleman/middleman-directory
[3]: https://github.com/middleman-contrib/middleman-deploy