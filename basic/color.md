# 色の変更

要素をクリックでテキストの色が変わったあと、徐々に元に戻る。

### 動作サンプル

<style>
  .box {
    height: 50px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    color: black;
    font-weight: bold;
    transition: all ease 2s 0s;
  }
  .box:active {
    transition: none;
    color: yellow;
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
.box {
  height: 50px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  color: blue;
  font-weight: bold;
  transition: all ease 2s 0s;
  overflow-y: hidden;
}
.box:active {
  transition: none;
  color: yellow;
}
```

### 解説
activeで元とは違うcolorを指定して、transitionをnoneにする。
これでクリック時に瞬時にその色に変化する。

戻るときは元のtransitionによって徐々に戻るアニメーション。
