## 查詢條件
- 'max-width': 設置最大寬度（針對小屏幕設備）
- 'min-width': 設置最小寬度（針對大屏幕設備）
- 'orientation': 設置屏幕的方向（橫向或縱向）

## 設計中的斷點
- 超大螢幕: 1200px 以上
- 桌面電腦: 992px - 1200px
- 平板電腦: 768px - 992px
- 手機: 480px - 768px

## 背景圖片處理
- `background-size: cover;`背景圖片會覆蓋整個區域，保持圖片的比例，可能會裁剪
- `background-size: contain;`:背景圖片會保持比例，顯示整張圖片，並可能會有空白區域

```
.container {
  background-image: url('background-image.jpg');
  background-size: cover;
  background-position: center;
  background-repeat: no-repeat;
}
```

## 圖片處理
  - html 跟 css 差異
    ```
    HTML <img> 標籤：可互動（例如點擊圖片來開啟鏈接或進行其它操作）。
    CSS background-image：不需互動（例如背景圖像、按鈕背景、卡片背景等）。
    ```
  - 更換
    ```
    # srcset 指定寬度，使用w
    # sizes 指定中斷，，使用px
    <img src="small.jpg" 
        loading="lazy"
        srcset="small.jpg 400w, middle.jpg 600w, large.jpg 800w" 
        sizes="(max-width: 400px) 400px, (max-width: 600px) 600px, 800px">
    ```
    
  - 自適應
    ```
    img {
      max-width: 100%;
      height: auto;
    }
    ```
    
  - Flex 自動縮放
    ```
    .image-gallery {
      display: flex;
      flex-wrap: wrap;
      gap: 20px;
    }

    .image-gallery img {
      max-width: 100%;
      height: auto;
      flex: 1 1 calc(33.33% - 20px); /* 每行顯示3張圖片 */
    }

    @media (max-width: 768px) {
      .image-gallery img {
        flex: 1 1 calc(50% - 20px); /* 在小屏設備上每行顯示2張圖片 */
      }
    }

    @media (max-width: 480px) {
      .image-gallery img {
        flex: 1 1 100%; /* 在超小屏設備上每行顯示1張圖片 */
      }
    }
    ```  


