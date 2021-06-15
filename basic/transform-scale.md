# スケールの変更

要素をクリックで拡大する。

### 動作サンプル

<style>
  .box-container {
    padding: 20px 0;
  }
  .box {
    width: 100px;
    height: 50px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    transform: scale(1);
    transition: all ease 2s 0s;
  }
  .box:active {
    transition: none;
    transform: scale(1.5) ;
  }
</style>

<div class="box-container">
  <div class="box">
    <div>CLICK!</div>
  </div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">CLICK!</div>
</div>
```

### CSS
```css
.box-container {
  padding: 20px 0;
}
.box {
  width: 100px;
  height: 50px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  transform: scale(1);
  transition: all ease 2s 0s;
}
.box:active {
  transition: none;
  transform: scale(1.5) ;
}
```

### 解説
activeでtransformのscaleを2倍に。
scaleを0.5など1より小さくすれば縮小になる。中の要素も含めて拡大縮小する。

戻るときは元のtransitionによって徐々に戻るアニメーション。

このサンプルでは回転時に欠けてしまうが、例としてそのままにしてある。
box-containerに十分なpaddingを取れば欠けない。
