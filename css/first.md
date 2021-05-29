### 垂直居中
- 块级元素: margin: 0 auto
- 行内元素: 
  - 其父元素: text-align: center;
- 单行文本垂直居中: line-height设为其高度
- 垂直居中图片
```html
<div id="parent">
<img src="image.png" alt="" />
</div>
```
```css
#parent {
line-height: 200px;
}
#parent img {
vertical-align: middle;
}
```