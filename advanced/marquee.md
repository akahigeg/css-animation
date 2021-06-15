# マーキー

なつかしのマーキーっぽいもの。

<style>
  .box-container {
    width: 400px;
    height: 20px;
    overflow: hidden;
  }
  .box {
    text-align: center;
    animation: marquee 5s linear infinite;
  }
  @Keyframes marquee {
    /* テキストの長さに合わせてtranslateXを調整する必要あり */
    from { transform: translateX(300px); }
    to   { transform: translateX(-300px); }
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">私のホームページへようこそ！</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">BOX</div>
</div>
```

### CSS
```css
.box-container {
  width: 400px;
  height: 20px;
  overflow: hidden;
}
.box {
  text-align: center;
  animation: marquee 5s linear infinite;
}
@Keyframes marquee {
  /* テキストの長さに合わせてtranslateXを調整する必要あり */
  from { transform: translateX(300px); }
  to   { transform: translateX(-300px); }
}
```

### 解説
marqueeタグの機能を完全再現することは難しいが、コンテンツに応じて似た動きをつけることは比較的容易。

opacityの1と0をキーフレームの50%と51%でパッと切り替わるようにしてある。

このあたりの調整で点滅のタイミングを調整することが可能。

