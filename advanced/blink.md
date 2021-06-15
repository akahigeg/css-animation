# ブリンク

なつかしのブリンク。

<style>
  .box {
    width: 50px;
    border: 2px solid blue;
    text-align: center;
    animation: blink 0.5s linear alternate infinite forwards;
  }
  @Keyframes blink {
    from { opacity: 1; }
    50%  { opacity: 1; }
    51%  { opacity: 0; }
    to   { opacity: 0; }
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">BOX</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">BOX</div>
</div>
```

### CSS
```css
.box {
  width: 50px;
  border: 2px solid blue;
  text-align: center;
  animation: blink 0.5s linear alternate infinite forwards;
}
@Keyframes blink {
  from { opacity: 1; }
  50%  { opacity: 1; }
  51%  { opacity: 0; }
  to   { opacity: 0; }
}
```

### 解説
opacityの1と0をキーフレームの50%と51%でパッと切り替わるようにしてある。

このあたりの調整で点滅のタイミングを調整することが可能。
