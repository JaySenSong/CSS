## 父元素屬性
- `display`: flex：啟用 Flexbox。

- `flex-flow`: 設置子元素`排列方向`及`換行`選項
```
  # flex-direction:row | row-reverse | column | column-reverse;
  # flex-wrap:nowrap | wrap | wrap-reverse;
  # default
  flex-flow: row nowrap
```

- `justify-content`：左右齊方式：
```
# justify-content:flex-start | flex-end | center | space-between | space-around | space-evenly;
```

- `align-items`：上下齊方式：
```
# align-items:stretch | flex-start | flex-end | center | baseline;
```

- `align-items`：上下齊方式：
```
# align-items:stretch | flex-start | flex-end | center | baseline;
```

## 子元素屬性
- `order` :  排序按照小到大
```
order:0;
```

- `flex` : flex (flex-grow、flex-shrink、flex-basis)，設定會覆蓋 width
  - `flex-grow`：補足剩餘空間，默認為 0（不增長）。
  - `flex-shrink`：空間不足時的縮小比例，默認為 1（允許縮小）。
  - `flex-basis`：同width優先級更高，默認為 auto。

```
# default, 所有子flex皆有此設定，導致寬度不會超出區塊
flex(0, 1, auto)
```

