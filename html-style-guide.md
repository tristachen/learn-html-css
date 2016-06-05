# HTML Style Guide

*   縮排使用 2 Spaces
*   一行不要超過 80 個字元
*   避免無意義的空行
*   使用小寫來表示 tag & attribute name
    Bad

        <DIV></DIV>

    Good

        <div></div>

*   等號前後不要空格
    Bad

        <div class = "css"></div>
    Good

        <div class="css"></div>

*   attribute 請加上雙引號
    Bad

        <div class=css></div>
    Good

        <div class="css"></div>

*   要有關閉符號  /
    Bad
    
        <input>
        <br>

    Good

        <input />
        <br />

*   在html要使用到 url 時，請用 &amp; 取代 &

*   style 放在 `<head>` 裡

        <link rel="stylesheet" href="styles.css">

*   javascript 放在 `</body>` 後面
        
        <script src="scripts.js">

