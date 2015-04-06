---
title: 建立新網站
---

# 建立新網站

首先我們需要先建立一個專案資料夾，讓 Middleman 在裡面運作。你可以使用現有的資料夾、或是透過 `middleman init` 指令讓 Middleman 幫你建立一個新的資料夾。

只要指定好你要做成新網站的資料夾，Middleman 就會幫你在裡面建立一個專案骨架（或是幫你開新資料夾）。

``` bash
$ middleman init my_new_project
```

### 專案骨架

每個新的專案，都會幫你建立好一組基本的網站開發骨架。它會以標準的結構，自動幫你建好你會在所有專案中用到的資料夾及檔案。

一個全新的專案會包含一個 `source` 資料夾、以及一個 `config.rb` 檔案。`source` 資料夾是你會在裡面建置網站的地方。專案骨架預設會包含放 JavaScript、CSS 及圖片用的資料夾，但是你也可以依你喜好自行修改對應。

而 `config.rb` 檔案則包含了 Middleman 的設定值、還有如何開啟如「編譯時壓縮」或「網誌模式」這類複雜功能的註解說明文件。

#### Gemfile

Middleman 也使用 Bundler 需要的 `Gemfile` 來表列及控制你的 gem 套件與依存關係。當你建立一個新專案時，Middleman 會自動產生一個 `Gemfile`，同時裡面會列出與你使用中相同版本的 Middleman。這會將這個專案中的 Middleman 鎖定在指定的版本範圍（例如 3.0.x 系列）。

你也可以修改你的 `Gemfile`，透過 `:git` 選項指定從 Github 使用最新版的 Middleman。所有你在專案中使用到的 Plugin 或是額外的程式庫，都應該要列在你的 `Gemfile` 裡面。這樣 Middleman 在啟動時自動 `require` 他們全部。

#### config.ru

`config.ru` 檔案描述了這個網站應該如何被一台啟用 Rack 的伺服器載入。有些使用者可能會想要把他們的 Middleman 網站，以開發模式架設在 Rack 基礎的伺服器上（例如 Heroku）。這個設定檔可以給他們一些方便。但是別忘了，Middleman 設計的目的是用來建立「靜態」網站的。

如果想要在你的專案中包含預先編寫好的 `config.ru` 檔案，只要在建立的指令後面加上 `--rack`
標籤：

``` bash
$ middleman init my_new_project --rack
```

如果你已經建立好了一個專案，但是想要加入 `config.ru` 檔案來搭配 Pow 或其它開發伺服器來使用，你可以自己建立並加入下列內容：

```
require 'rubygems'
require 'middleman/rack'
run Middleman.server
```
