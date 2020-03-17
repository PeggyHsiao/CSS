# position屬性  
指定某元素在網頁中的位置，其屬性值包含static、relative、absolute、fixed。
- **position: static**：預設值。依照瀏覽器預設位置排版。無法使用top、left、right、bottom、z-index。
- **position: fixed**：將元素固定於視窗的絕對位置，不會受到捲動網頁、position其他屬性值影響。
- **position: relative**：依照top、left、right、bottom調整原本應顯示位置其相對位置，沒有特別設定同static。  
- **position: absolute**：根據最靠近的父元素設定其絕對位置，如果沒有就會參照`<body>`來定位。  
