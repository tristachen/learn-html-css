# CSS Style Guide

-   縮排使用 2 Spaces
-   一行不要超過 80 個字元，除了一些無法避免的特殊用法以及 url

## 註解
-   在檔案開頭要有註解導覽說明這個檔案在做什麼，還有架構
    @header ，在前面加上 `@` 可以幫助搜尋的時候更方便

        /*===============================
        =            @header            =
        ===============================*/

-   兩大區塊間的用空行 5 行分開，再掃描檔案的時候有幫助

        /*===============================
        =            @header            =
        ===============================*/
        .header {
          top: 0
        }





        /*===============================
        =            @footer            =
        ===============================*/
        .footer {
          bottom: 0
        }

-   省略不必要的 selector ，有必要的話可以加上註解，既可以不影響瀏覽器的效能，又可以讓其他開發者瞭解這 selector 的用法。像下面這樣的例子，可以讓其他開發者知道，這些 selector 只會套用在什麼 html element

        /*ol*/.breadcrumb{}
        /*p*/.intro{}
        /*ul*/.image-thumbs{}

-   如果有兩個 selector 分隔很遠，例如兩個檔案，可以透過註解表明彼此的關係

        base.css
        /**
         * Extend `.btn` in theme.css
         */
         .btn{}

        theme.css
         /**
         * Extends `.btn` in base.css
         */
         .btn{}


## 語法本身
-   CSS 命名，以 `-` 連接 `app-header`
-   如果 js 需要用到 selector ，加上 `.js-` 前綴詞，目的是讓彼此行為分開，方便維護
-   在 html 裡撰寫 class 時，class 彼此之間用 2 個 spaces 區分以利閱讀
-   顏色使用 Hex 格式，並用小寫，可以縮寫就縮寫
        `#aaa`
-   使用單引號，然後 url() 內不需要引號，但 `input[type="text"]` 這種就要用雙引號
-   如果單位為 0，不要給單位
        `margin: 0`
-   逗號後面要空一格
-   每一個 selector 都獨立一行，方便偵錯

        /* Recommended */
        h1,
        h2,
        h3 {
          font-weight: normal;
          line-height: 1.2;
        }

-   { } 前後加上空格 `{ width: 10% }`
-   如果是小數，不要加 0 `margin: .5em`
-   盡量不要用簡寫，除非每個數值都有改到。這樣可以避免寫出越來越難維護的 css
    `background-color: red` 比 `background: red` 來的好
-   不要出現 ID selector，也盡量不要有 html element
-   selector 盡量簡短，如果能一層就一層，最好不要超過三層
-   使用 rem (root em)

        @mixin font-size($font-size){
            font-size:$font-size +px;
            font-size:$font-size / $base-font-size +rem;
        }

-   某些語法適當使用縮排，可增加可讀性，也方便修改

        .selector {
            background-image:
                linear-gradient(#fff, #ccc),
                linear-gradient(#f3c, #4ec);
            box-shadow:
                1px 1px 1px #000,
                2px 2px 1px 1px #ccc inset;
        }

        .selector {
          -webkit-box-shadow: 0 1px 2px rgba(0,0,0,.15);
                  box-shadow: 0 1px 2px rgba(0,0,0,.15);
        }


## 整體觀念
-   建議先寫好 html 架構，再撰寫 css
-   盡量不要定義寬度，盡量由上層或 grid system 定義
-   不要定義元件高度，除非是 圖片 or css sprite，如果有必要，用 line-height 會較好
-   整體撰寫順序：
    1. 重置 html element 的樣式，以確保在各瀏覽器的一致性
    1. 重新定義 html element 的樣式 (h1, ul)
    1. 通用、共用或基礎的 selector
    1. 組合而成的 selector
    1. 特殊應用，像是用來修正特殊問題或是瀏覽器問題
-   file 分類：
    1. base: reset
    1. layout: 整體大區塊，ex: .header, .footer
    1. module: 一個整體的元件，ex: .nav, .list
    1. theme: 整體的主視覺設定，像是顏色，字體大小

-   selector order：

        /* Positioning */
          position: absolute;
          z-index: 10;
          top: 0;
          right: 0;
          bottom: 0;
          left: 0;

        /* Box Model */
          display: inline-block;
          overflow: hidden;
          box-sizing: border-box;
          width: 100px;
          height: 100px;
          padding: 10px;
          margin: 10px;
          float: right;

        /* Typographic */
          font: normal 13px "Helvetica Neue", sans-serif;
          line-height: 1.5;
          color: #333;
          text-align: center;

        /* Visual */
          background-color: #f5f5f5;
          border: 1px solid #e5e5e5;
          border-radius: 3px;

        /* Misc */
          opacity: 1;

-   將 Media Query 與其最相關的規則放在一起。而不是放在最後面，或是另一個 css file。否則接手的人很難看到其相關性
