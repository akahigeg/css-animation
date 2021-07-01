# 2D回転

要素にhoverで回転する。

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
    transform: rotate(180deg);
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
  width: 80px;
  height: 80px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  transition: all 300ms 0s ease;
}
.box:hover {
  transform: rotate(180deg);
}
```

### 解説
hover時のスタイルにtransformでrotateを適用して回転させたもの。
中の要素も含めて回転する。

180degは半回転だがこれを360degにすれば1回転。720degにすれば2回転。
-180degにすれば逆に半回転する。

このサンプルでは回転時に欠けてしまうが、例としてそのままにしてある。
box-containerに十分なpaddingを取れば欠けない。
