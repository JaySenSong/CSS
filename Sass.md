### 變數
```
$primary-color: #3498db;
$font-size-base: 16px;

body {
  color: $primary-color;
  font-size: $font-size-base *2;  #可做運算
}
```
### 嵌套
```
.nav {
  background: #333;
  .nav-item {
    color: #fff;
    &:hover {
      color: #3498db;
    }
  }
}
```

### 混入
- `@mixin` : 定義
- `@include` : 調用
```
@mixin button-style($color, $padding: 10px) {
  background-color: $color;
  padding: $padding;
  border: none;
  border-radius: 5px;
  color: white;
}

.primary-button {
  @include button-style(#3498db); // 使用默認的 padding
}
```
 
### 繼承
- @extend
```
base-button {
  padding: 10px;
  border-radius: 5px;
  font-size: 16px;
  color: white;
}

.primary-button {
  @extend .base-button;
  background-color: #3498db;
}
```
