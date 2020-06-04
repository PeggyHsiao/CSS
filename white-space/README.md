# white-space
根據不同屬性值決定如何處理文字中的空白字元。

## 屬性值
屬性值          | 說明
---------------|--------
normal (預設值) | 連續空白會合併為一個，**換行符號也視為空白**。會隨著外圍元素的寬度自動換行。
nowrap         | 空白處理和`normal`一樣，但是不會隨著外圍元素的寬度自動換行。
pre            | 所有空白都會被保留也允許換行符號，不會隨著外圍元素的寬度自動換行。
pre-wrap       | 所有空白都會被保留也允許換行符號，會隨著外圍元素的寬度自動換行。
pre-line       | 和`normal`一樣，但允許換行符號。

## 範例
```html
<!--index.html-->

<div id="normal">
    <p>Lorem   ipsum dolor sit amet consectetur adipisicing elit. 
    dignissimos ut hic fugiat atque voluptas expedita enim libero!</p>
</div>

<div id="nowrap">
    <p>Lorem   ipsum dolor sit amet consectetur adipisicing elit. 
    dignissimos ut hic fugiat atque voluptas expedita enim libero!</p>
</div>

<div id="pre">
    <p>Lorem   ipsum dolor sit amet consectetur adipisicing elit. 
    dignissimos ut hic fugiat atque voluptas expedita enim libero!</p>
</div>

<div id="pre-wrap">
    <p>Lorem   ipsum dolor sit amet consectetur adipisicing elit. 
    dignissimos ut hic fugiat atque voluptas expedita enim libero!</p>
</div>

<div id="pre-line">
    <p>Lorem   ipsum dolor sit amet consectetur adipisicing elit. 
    dignissimos ut hic fugiat atque voluptas expedita enim libero!</p>
</div>
```
```css
/* main.css */

div { 
    border: 1px solid rgba(0,0,0,.1);
    width: 300px; 
}

div#nowrap > p{ white-space: nowrap; }

div#pre > p{ white-space: pre; }

div#pre-wrap > p{ white-space: pre-wrap; }

div#pre-line > p{ white-space: pre-line; }
```
結果顯示如下：  

![Result](https://github.com/PeggyHsiao/CSS-Notes/blob/master/white-space/result.JPG)
