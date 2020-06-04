# text-indent屬性  
段落首字縮排。

## 屬性值
屬性值 (數值) |  說明
-------------|------
大於 0       |  縮排
等於 0       |  預設值
小於 0       |  凸排

單位可以是`px`、`rem`、`%`...等。

## 範例
```html
<!--index.html-->

<p>這一段沒有縮排</p>
<p id="indentA">這一段縮排10px</p>
<p id="indentB">這一段縮排10%</p>
<p id="indentC">這一段縮排-30px</p>
<p id="indentD">這一段縮排-1rem</p>
```
```css
/* main.css */

p#indentA{ text-indent: 10px; }
p#indentB{ text-indent: 10%; }
p#indentC{ text-indent: -30px; }
p#indentD{ text-indent: -1rem; }
```
結果如下圖，第三行被截斷是因為**負值的效果等於凸排**。
![Result](https://github.com/PeggyHsiao/CSS-Notes/blob/master/text-indent/result.JPG)