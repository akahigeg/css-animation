# 表示/非表示の切り替え

displayはアニメーションできない模様。

### 動作サンプル

※アニメーションとしては動作しない

<style>
  .box {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    transition: all ease 1s 0s;
  }
  .box:hover {
    display: none;
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
  display: none;
}
```

### 解説
フェードアウトやフェードインさせたいならdisplayではなくopacityを使う。

animationの最後で要素を消したいならばキーフレームの99%まではdisplayをnone以外にし、100%でdisplayをnoneにする。
