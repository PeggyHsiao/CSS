# position屬性  
指定某元素在網頁中的位置，其屬性值包含static、relative、absolute、fixed。
- **position: static**：預設值。依照瀏覽器預設位置排版。無法使用top、left、right、bottom、z-index。
- **position: relative**：沒有特別設定top、left、right、bottom，就會同static一樣按照瀏覽器預設配置。  
- **position: absolute**：根據上層容器中設定其絕對位置，如果沒有上層容器就會參照`<body>`。  
- **position: fixed**：將元素固定於視窗的絕對位置，不會受到position其他屬性值影響。
