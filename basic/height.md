# 高さの変更

要素にhoverで高さが徐々に大きくなる

### 動作サンプル

<style>
  .box {
    height: 50px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    margin-bottom: 10px;
    transition: all ease 1s 0s;
    overflow-y: hidden;
  }
  .box:hover {
    height: 100px;
  }
</style>

<div class="box-container">
  <div class="box">
    <div>HOVER!</div>
    <div>HOVER!</div>
    <div>HOVER!</div>
  </div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">HOVER!</div>
</div>
```

### CSS
```css
.box {
  height: 100px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  margin-bottom: 10px;
  transition: all ease 300ms 0s;
}
.box:hover {
  height: 300px;
}
```

### 解説
hoverでheightを変化させ、transitionによってアニメーション。

overflow-yでhiddenにしといた要素を表示させることもできるよ。