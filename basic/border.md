# ボーダーの変更

hoverでボーダーの色が変わったあと、徐々に元に戻る。

### 動作サンプル

<style>
  .box {
    height: 50px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    font-weight: bold;
    transition: all ease 2s 0s;
  }
  .box:active {
    border: 2px solid #999;
    transition: none;
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
  font-weight: bold;
  transition: all ease 2s 0s;
}
.box:active {
  border: 2px solid #999;
  transition: none;
}
```

### 解説
activeで元とは違うborder-colorを指定して、transitionをnoneにする。
これでクリック時に瞬時にその色に変化する。

戻るときは元のtransitionによって徐々に戻るアニメーション。

border-styleやborder-widthも変えられるが効果的に使うのは難しいか。


