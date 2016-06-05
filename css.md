# CSS

## 摘要
- [Style Guide](#style-guide)

## Style Guide
<a name="style-guide"></a>
- 命名
- 順序


## TODO
*   [Box Model](http://www.w3.org/TR/CSS2/box.html)
*   Selector 的計算方式 
*   Webfonts (ex: fontawe)
*   漸層、陰影
*   圓角、邊框背景
*   Transition
*   Transform
*   Animation
*   置中
*   偽元素
*   browser 是由右到左來解析 selector。id v.s class 其實速度不會差很多，可以都用 class。但請盡量不要用 html tag，效能上確實變慢很多。

    ```
    .nav a          //這效能最差
    .nav .nav-link  //效能較好
    ```
