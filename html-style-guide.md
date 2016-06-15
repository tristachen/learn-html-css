# HTML Style Guide

-   縮排使用 2 Spaces
-   一行不要超過 80 個字元
-   避免無意義的空行
-   使用小寫來表示 tag & attribute name
    Bad

        <DIV></DIV>

    Good

        <div></div>

-   等號前後不要空格
    Bad

        <div class = "css"></div>
    Good

        <div class="css"></div>

-   attribute 請加上雙引號
    Bad

        <div class=css></div>
    Good

        <div class="css"></div>

-   要有關閉符號  /
    Bad

        <input>
        <br>

    Good

        <input />
        <br />

-   在html要使用到 url 時，請用 &amp; 取代 &
    除了 < , &, 控制符號, 或是斷行符號, 可以使用 entity references, 其他字元請不要使用，只要確保檔案格式是 UTF-8

-   style 放在 `<head>` 裡

        <link rel="stylesheet" href="styles.css">

-   javascript 放在 `</body>` 後面

        <script src="scripts.js">

-   忽略 protocol, good src='abc.js'  bad src='http://abc.js'

-   使用 UTF-8(no BOM - byte order mark)
    `<meta charset="utf-8">`

-   不叫 html tags, 叫 html elements
-   每一個區塊、清單、表格，用一個空行隔開
-   使用雙引號
-   attribute order：
    0. class
    0. id, name
    0. data-*
    0. src, for, type, href
    0. title, alt
    0. aria-*, role

-   如果是布林的話，可以不用寫值   `<input disabled>`
