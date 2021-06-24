# 垂直フリップ

要素にhoverで垂直フリップする。

<style>
  .box {
    width: 80px;
    height: 80px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    transition: all 300ms 0s ease;
  }
  .box:hover {
    transform: rotateX(180deg);
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">HOVER!?</div>
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
  width: 80px;
  height: 80px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  transition: all 300ms 0s ease;
}
.box:hover {
  transform: rotateY(360deg);
}
```

### 解説
hover時のスタイルにtransformでrotateXを適用して3D方向に回転させたもの。
中の要素も含めて回転する。