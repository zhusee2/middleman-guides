---
title: 樣板語言
---

# 樣板語言

Middleman 讓你可以使用多種樣板語言來簡化你的 HTML 開發過程。從單純允許你在頁面中使用 Ruby 變數或迴圈的樣板語言、到讓你可以用完全不同的格式來編寫、並編譯為 HTML 的樣板語言都有。Middleman 預設支援 ERb、Haml、Sass、Scss 及 CoffeeScript 引擎，但是也有許多其他的樣板引擎可供安裝。只需要引入它們的 Tilt 相容 gem 套件即可。詳情請參閱[引擎清單][1]。

## 樣板語言基礎

預設的樣板語言是 ERb。ERb 看起來就跟 HTML 差不多，但是你可以在裡面加入變數、呼叫方法、使用迴圈及 if 判斷式。本篇以下的段落都會使用 ERb 作為範例。

在 Middleman 中，所有的樣板檔案都會在副檔名中指名它的樣板語言。例如以 ERb 寫成的首頁，檔名就會是 `index.html.erb`。其中 `index.html` 是該網頁的完整檔名，`.erb` 則是標記它為 ERb 樣板檔案。

一開始，這個網頁可能只會包含標準的 HTML：

``` html
<h1>歡迎光臨</h1>
```

如果我們想要華麗一點，我們可以加入一組迴圈：

``` html
<h1>歡迎光臨</h1>
<ul>
  <% 5.times do |num| %>
    <li>報數 <%= num %></li>
  <% end %>
</ul>
```

[1]: (/tw/basics/template_engine_options/)
