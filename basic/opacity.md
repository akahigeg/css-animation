# 透明度の変化

hover時にフェードアウト、hoverが外れるとフェードイン。

### 動作サンプル

<style>
  .box {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    opacity: 1;
    transition: all linear 1s 0s;
  }
  .box:hover {
    opacity: 0;
  }
</style>

<div class="box-container">
  <div class="box">HOVER!</div>
</div>

#### HTML
```html
<div class="box-container">
  <div class="box">HOVER!</div>
</div>
```

### CSS
```css
.box {
  width: 100px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  opacity: 1;
  transition: all linear 1s 0s;
}
.box:hover {
  opacity: 0;
}
```

### 解説
徐々に透明度を変化させることでフェードインやフェードアウトを実装できる。