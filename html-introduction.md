# HTML Introduction

*   HTML 全名是：Hyper Text Markup Language
*   由一堆標籤組合而成，藉此來描述 web page 的結構組成。這些標籤是用尖括號組成，通常會是一組`<tag></tag>`
*   無論有多少空格，空行，都會被計算成1個空格; 除了`<pre></pre>`內的
*   副檔名是 .html 或 .htm
*   檔案編碼請用 UTF-8
*   HTML 結構
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Document</title>
</head>
<body>
  
</body>
</html>
```

*   DOCTYPE 是用來表示這份 web page 的類型，沒有大小寫區別
    *   HTML5
        ```html
        <!DOCTYPE html>
        ```

    *   HTML 4.01
        ```html
        <!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01 Transitional//EN" "http://www.w3.org/TR/html4/loose.dtd">
        ```

    *   XHTML 1.0
        ```html
        <!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN" "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
        ```

*   `<html>` 是用來表示整個 html document，加入 lang attribute，這對於搜尋引擎還有無障礙設備(accessibility applications)是很重要的
    ```html
    <html lang="en-US">
    ```

*   `<head>` 會放入一些 Web page 的相關資訊
    *   `<base>` 定義 base URL and base target
        ```
        <base href="http://example.com/images/" target="_blank">
        ```

    *   `<meta>` 會提供 browser 如何顯示內容、提供搜尋引擎建立關鍵字index、或是提供其他 web services 有用的資訊


    *   `<title>` 會做為 Web page 的 title 供 browser tab 顯示

*   `<body>` 指的是 html 可以看到的 content

