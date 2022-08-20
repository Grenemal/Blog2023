# CSS垂直居中方案

```html
<style>
#container{

}
</style>
<div>实现垂直居中布局</div>
<div id="container">
  <div id="content">
  </div>
</div>
```

1. flex布局

```css
#container {
  display: flex;
  align-items: center;
  justify-content: center;
}
```

2. 绝对定位📌 + transform
```css
#container {
  position: relative;
}
#content {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

3. 绝对定位📌 + margin:auto

```css
#container {
  position: relative;
}
#content {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  margin: auto;
}
```

4. table-cell + 子元素为行内元素

```css
#container {
  display: table-cell;
  text-align: center;
  vertical-align: middle;
}
#content {
  display: inline-block;
}
```
