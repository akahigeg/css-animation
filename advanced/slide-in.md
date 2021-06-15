# スライドイン

要素がスライドインして表示。

<style>
  .box-container {
    width: 200px;
    overflow: hidden;
  }
  .box {
    width: 200px;
    height: 30px;
    border: 2px solid #000;
    text-align: center;

    animation: SlideIn 1s forwards;
  }
  @keyframes SlideIn {
    from {
      transform: translateX(500px);
    }
    to {
      transform: translateX(0px);
    }
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">スライドイン</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">スライドイン</div>
</div>
```

### CSS
```css
.box-container {
  width: 200px;
  overflow: hidden;
}
.box {
  width: 200px;
  height: 30px;
  border: 2px solid #000;
  text-align: center;

  animation: SlideIn 1s forwards;
}
@keyframes SlideIn {
  from {
    transform: translateX(500px);
  }
  to {
    transform: translateX(0px);
  }
}
```

### 解説
transformでtranslateXを利用して横からスライドイン。

box-containerの幅をboxと同じにしてoverflowをhiddenにすることで、box-containerの外の動きを隠し、何もないところからスッとスライドしてきたように見せている。