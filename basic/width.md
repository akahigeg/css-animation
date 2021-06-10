# 幅の変更

要素にhoverで幅が徐々に大きくなる

### 動作サンプル

<style>
  .box {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    transition: all ease 1s 0s;
  }
  .box:hover {
    width: 300px;
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
  transition: all ease 1s 0s;
}
.box:hover {
  width: 300px;
}
```

### 解説
hoverでwidthを変化させ、transitionによってアニメーション。
