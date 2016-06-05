# HTML Tags

## Block Elements
```
<div>
<h1> - <h6>
<p>
<form>
```

*   `<header>` 表示一個文章或段落的標題 
*   `<nav>` - 表示容器的導航鏈結
*   `<section>` - 一個段落
*   `<article>` - 代表一個獨立的文章
*   `<aside>` - 代表在內容旁的內容，像是 sidebar
*   `<footer>` - 表示一個文章或段落的 頁腳
*   `<details>` - 額外的資訊
*   `<summary>` - `<details>` 的標題

## Inline Elements
```
<span>
<a>
<img>
```

## Global Attribute
*   title 用來表示額外的資訊，通常 browser 會實作當滑鼠移到該元素的時候，顯示提示

## Comment
```html
<!-- and  -->
```
    
### Conditional Comments
下面表示只有 IE8 才能看到內容, 其它都會視為 comment
```html
<!--[if IE 8]>
    .... something ....
<![endif]-->
```

## Heading
html headings 有 h1 ~ h6
不要為了將字變大變粗而使用heading！heading 是很重要的，它可以供搜尋引擎來組識你的 Web page 結構

## P
*   attributes: 
    *   title - 當滑鼠移到該段落會顯示文字

## Image & Map
### Image
*   attributes: 
    *   src - 圖檔名稱
    *   alt - 一定要加，是為了避免當瀏覽器無法顯示圖片的時候，可以提示使用者，對於無障礙設備也是有用的資訊，因為可以被 screen readers 給讀取，或許在無障礙設備可以聽到 webpage 講出這些字來提供給視障人士
    *   width & height - 建議要加，因為可以減少畫面閃爍，因為瀏覽器會預先留位置給image
    *   usemap - 指向 `<map>` ID
    
### Map
*   `<map>`用來定義一組 image-map mapping
*   `<area>` 用來定義在 image-map 可點選的區塊

```html
<img src="map.png" alt="Map" usemap="#pngmap" style="width:200px;height:100px;">

<map name="pngmap">
  <area shape="circle" coords="20, 20, 20" alt="Circle1" href="circle1.html">
  <area shape="rect" coords="0, 0, 50, 50" alt="Rect" href="rect.html">
  <area shape="circle" coords="10, 10, 10" alt="Circle2" href="circle2.html">
</map>
```

## A
*   attributes
    *   href - 鏈結路徑，可以是絕對路徑或相對路徑，或是 bookmark `#` 指向在頁面上的 HTML ID 
        TODO: 無子文件夾上的斜線，可能會產生兩個請求到 server。許多 server 會將一個斜線自動添加到位置，然後創建一個新的請求。好像跟 .icon 有類似用法(?)
    *   target - 開啟鏈結的方式
        *   _self - 預設值，會直接從 `<a>` 的 frame 開啟  
        *   _blank - 開新分頁或新視窗
        *   _parent - 透過 parent frame 開啟 (適用在 iframe 情境)
        *   _top - 當前這個視窗開啟 (適用在 iframe 情境)
        *   framename - 指定 iframe 的 name 開啟 (適用在 iframe 情境)
*   children
    裡面不一定要文字，可以是任何 html tags

## List
*   type
    *   ul: unordered list
    *   ol: ordered list
        type: "1", "A", "a", "I",  "i"
        ```html
        <ol type="1">
          <li>One</li>
          <li>Second</li>
          <li>Third</li>
        </ol>
        ```

    *   dl: description list   就像ppt裡的文字階層
        ```html
        <dl>
          <dt>Phone</dt>
          <dd>- small screen</dd>
          <dt>Tab</dt>
          <dd>- middle screen</dd>
        </dl>
        ```

*   children
    可以包含新的 list 或是其他 html tags\

## Form
如果 Form 有 submit，那 name attribute 就要存在
Bad
```html
<form>
    <input />
</form>
```

Good
```html
<form>
    <input name="price"/>
    <input type="submit"/>
</form>
```
`<fieldset>` 用來表示是相關的 Form element
`<legend>` 指 `<fieldset>` 的標題

`<textarea>` 要有 col and row
```
<textarea cols="25" rows="3" name="xx"></textarea>
```

## Table
`<td>` 放資料的

合併儲存格
```html
<th colspan="2">
<th rowspan="2">
```

`<caption>` 表格標題，必須放在緊接在 `<table>` 後面


## Script
`<noscript>` 用來表示如果使用者沒有開啟支援js 時，所顯示的區塊


## hr
水平線


##  Formatting text
`<b>` v.s `<strong>`
分別代表 bold, strong; 其中 b 沒有任何意思, strong 在語義上則有強調的意思

`<i>` v.s `<em>`
分別代表 italic, emphasized; 其中 i 沒有任何意思, emphasized 在語義上則有強調的意思

`<small>` 較小的文字
`<mark>` 標籤
`<del>` 刪除線
`<ins>` 加底線
`<sub>` 下標
`<sup>` 上標文字

## Quotation & Citation
*   `<abbr>` 定義縮寫，可以提供有用的資訊給 browser、搜尋引擎、翻譯系統
*   `<address>` 表示聯絡資訊，browser 通常會用斜體表示，並在前後各空一行
*   `<bdo>`  改變文字的方向，dir="rtl" 由右至左；dir="ltr" 由左至右
*   `<q>` 表示短引言，browser 通常會用引號來表示
*   `<blockquote>` 表示這段引用別的地方，browser 通常會縮排這段文字
*   `<cite>` 表示作品的名稱，browser 通常會斜體表示
