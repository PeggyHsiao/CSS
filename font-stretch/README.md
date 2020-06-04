# font-stretch
可以改變文字的寬度，只限定使用於**具有可自訂文字寬瘦屬性**的字型。(例如：`LeagueMonoVariable.ttf`...)  

## 屬性值
屬性值           | 說明    
----------------|----------------
ultra-condensed | 最瘦 50%
extra-condensed | 瘦	62.5％
condensed       | 瘦 75%
semi-condensed  | 瘦 87.5%
normal          | 中等 100%
semi-expanded   | 寬 112.5%
expanded        | 寬 125%
extra-expanded  | 寬 150%
ultra-expanded  | 寬 200%
百分比 (%)       | 依照字型自有的縮放範圍自訂

`LeagueMonoVariable.ttf`的縮放範圍為50%-200%。所以在百分比定義的時候如果小於50%會被視為最小值(50%)，反之如果超過200%則會視為最大值(200%)。  

不過有些字型只有區分為「正常」和「窄」，無論屬性值填入什麼結果都是`normal`或`condensed`，就算輸入`font-stretch: expanded`結果還是呈現`normal`的樣式。簡單來說，它會去判斷是否為`condensed`，如果不是一律視為`normal`。

## 範例
>使用 LeagueMonoVariable.ttf 字型來說明
```html
<!--index.html-->

<div class="container">
    <p class="ultra-condensed">Hello World</p>
    <p class="extra-condensed">Hello World</p>
    <p class="condensed">Hello World</p>
    <p class="semi-condensed">Hello World</p>

    <p class="normal">Hello World</p>

    <p class="semi-expanded">Hello World</p>
    <p class="expanded">Hello World</p>
    <p class="extra-expanded">Hello World</p>
    <p class="ultra-expanded">Hello World</p>
</div>
```
利用`@font-face`加入要使用的字型，另外`chrome`需要額外定義`font-stretch`的範圍。這裡我們就配合`LeagueMonoVariable.ttf`的縮放範圍將其設為50%-200%。
```css
/* main.css */

@font-face {
    src: url('LeagueMonoVariable.ttf');
    font-family: 'LeagueMonoVariable';
    font-stretch: 50% 200%;  /* Required by Chrome */
  }
  
  .container {
    font-family:'LeagueMonoVariable';
    font-size: 2rem;
  }

  .ultra-condensed { font-stretch: ultra-condensed; }
  .extra-condensed { font-stretch: extra-condensed; }
  .condensed { font-stretch: condensed; }
  .semi-condensed { font-stretch: semi-condensed }

  .normal { font-stretch: normal; }
  
  .semi-expanded { font-stretch: semi-expanded }
  .expanded { font-stretch: expanded; }
  .extra-expanded { font-stretch: extra-expanded; }
  .ultra-expanded { font-stretch: ultra-expanded; }
```
這時候打開瀏覽器會看到這樣的結果。
<img src='https://github.com/PeggyHsiao/CSS-Notes/blob/master/font-stretch/result.JPG' style='align:left'/>  


如果不想侷限屬性值規定的縮放大小，也可以自訂百分比。
```html
<!--index.html-->

<div class="container">
    <p class="custom-narrow">Hello World</p>
    <p class="custom-wider">Hello World</p>
</div>
```
```css
/* main.css */

.custom-narrow { font-stretch: 60%; }
.custom-wider { font-stretch: 130%; }
```