# CSS Declaration


## Position
relative 相對與同層物件排 x,y
absolute 絕對與上層 x,y 同起點，如果要使用 right/bottom，一定要搭配這個

## Display
inline-block 水平排列

## Padding & Margin
padding 不能負
margin 可以負

## A
a:link
a:visited
a:hover 
a:active

## Table
```css
table, th, td {
    border: 1px solid black;
    border-collapse: collapse;
    border-spacing: 5px;       //td 彼此間的距離
}
```

## List

```css
ul {
  list-style-type:disc
  list-style-type:circle
  list-style-type:square
  list-style-type:none
}
```

## Image
新寫法，可以用 css 來表示圖檔位置，不用為了想在 css 表示圖檔而用 backage-image 來達成。但還不是每個瀏覽器都有支援
```css
.img {
  width: 223px;
  height: 36px;
  content: url('images/logo.png');
}
```
