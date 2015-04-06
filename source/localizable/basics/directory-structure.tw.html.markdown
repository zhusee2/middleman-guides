---
title: 目錄結構
---

# 目錄結構

一個預設的 Middleman 專案，包含如下列的目錄結構：

``` ruby
mymiddlemansite/
+-- .gitignore
+-- Gemfile
+-- Gemfile.lock
+-- config.rb
+-- source
    +-- images
    ¦   +-- background.png
    ¦   +-- middleman.png
    +-- index.html.erb
    +-- javascripts
    ¦   +-- all.js
    +-- layouts
    ¦   +-- layout.erb
    +-- stylesheets
        +-- all.css
        +-- normalize.css
```

## 主要目錄

Middleman 利用 `source`、`build`、`data` 以及 `lib` 目錄作為特定用途。這些目錄應該要放在 Middleman 主目錄的下面同一層。

### Source 目錄

`source` 裡面放著你網站專案中等著被編譯的原始碼，包含了樣板檔、JavaScript、CSS 及圖片。

### Build 目錄

`build` 就是你的靜態網站在經過編譯後，會被輸出到的地方。

### Data 目錄

你可以在 `data` 資料夾中建立 `.yml`、`.yaml` 或 `.json` 檔案來存放一些本地的靜態資料，之後這些資訊就可以在你的樣板中被使用。`data` 資料夾必須被放在你專案的根目錄，也就是必須跟你的 `source` 資料夾同一層。詳情請參閱[靜態資料檔案](/tw/advanced/data_files/)文件。

### Lib 目錄

`lib` 讓你可以在裡面放入包含 [Helper 方法](/tw/basics/helper_methods/)的外部 Ruby 模組，幫助你建立你的 App。如果你有在用 Rails，應該會對這個結構比較熟悉。
