---
title: Frontmatter
---

# Frontmatter

Frontmatter 可以讓你在樣板的最開頭，使用 YAML 或 JSON 格式來指定頁面專屬的變數。

## YAML Frontmatter

用一個簡單的 ERb 樣板舉例，假設你要為這個頁面指定一些 frontmatter 變數來變更它的版型：

``` html
---
layout: "custom"
title: "我的標題"
my_list:
  - one
  - two
  - three
---

<h1>清單</h1>
<ol>
  <% current_page.data.my_list.each do |f| %>
  <li><%= f %></li>
  <% end %>
</ol>
```

Frontmatter 必須被放在樣板的最開頭，並且要使用三連槓 `---` 來將其跟剩下的內容分開。在這個段落裡面，你可以新增之後可以在樣板中透過 `current_page.data` 雜湊物件取用的資料。例如：`title: "我的標題"` 可以用 `current_page.data.title` 取用。`layout` 設定會直接被傳給 Middleman，並用來更改這個網頁要套用的版型。你也可以用 frontmatter 來設定 `ignore`、`directory_index` 或是其他的頁面屬性。

## JSON Frontmatter

你也可以用 JSON 來設定你的 frontmatter。你必須用 `;;;` 來標記 frontmatter 段落，看起來會像這樣：

``` json
;;;
"layout": "custom",
"my_list": [
  "one",
  "two",
  "three"
]
;;;
```

然後你就可以像 YAML frontmatter 一樣，在頁面中使用它了。
