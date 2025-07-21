## Grid 父容器屬性
- `display`: grid： 啟動Grid。
- `grid-template-columns`：左右。
- `grid-template-rows`：上下。
- `grid-template-areas`：2維區塊。
- `grid-gap` :間距。

## Grid 子項目屬性
- `grid-column-start`、`grid-column-end`：左到右開始結束。
- `grid-row-start`、`grid-row-end`：上到下開始結束。
- `grid-area`：放置區塊。

```
.container {
  display: grid;
  grid-template-columns: 1fr 2fr 1fr;
  grid-template-rows: auto 200px auto;
  grid-template-areas: 
    "header header header"
    "sidebar content content"
    "footer footer footer";
  grid-gap: 10px;
}
.header {
  grid-area: header;
}
.sidebar {
  grid-area: sidebar;
}
.content {
  grid-area: content;
}
.footer {
  grid-area: footer;
}
```



