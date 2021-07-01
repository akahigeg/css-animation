# クリップパスの変更

クリップパスの値を変えてクリップされた表示領域を変更する。

<style>
  .box {
    display: flex;
    justify-content: center;
    align-items: center;

    background-color: #999;
    width: 80px;
    height: 80px;

    border-radius: 4px;

    clip-path: circle(80px at 50% 50%);
    transition: all 300ms 0s ease;
  }
  .box:hover {
    clip-path: circle(40px at 50% 50%);
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">HOVER!</div>
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
  display: flex;
  justify-content: center;
  align-items: center;

  background-color: #999;
  width: 80px;
  height: 80px;

  border-radius: 4px;

  clip-path: circle(80px at 50% 50%);
  transition: all 300ms 0s ease;
}
.box:hover {
  clip-path: circle(40px at 50% 50%);
}
```

### 解説
クリップ領域を変更するアニメーション。

circleからpolygonへの変更など、シェイプ形状を変えるとアニメーションしない。