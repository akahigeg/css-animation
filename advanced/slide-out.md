# スライドアウト

要素が1秒後にスライドアウトして消える。

<style>
  .box-container {
    width: 200px;
    height: 30px;
    overflow: hidden;
  }
  .box {
    width: 200px;
    height: 30px;
    border: 2px solid #000;
    text-align: center;
    transition: none;
    animation: SlideOut 2s 1s forwards;
  }
  @keyframes SlideOut {
    from {
      transform: translateY(0px);
    }
    to {
      transform: translateY(500px);
    }
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">スライドアウト</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">スライドアウト</div>
</div>
```

### CSS
```css
.box-container {
  width: 200px;
  height: 30px;
  overflow: hidden;
}
.box {
  width: 200px;
  height: 30px;
  border: 2px solid #000;
  text-align: center;
  transition: none;
  animation: SlideOut 2s 1s forwards;
}
@keyframes SlideOut {
  from {
    transform: translateY(0px);
  }
  to {
    transform: translateY(500px);
  }
}
```

### 解説
transformでtranslateYを利用して下にスライドアウト。

box-containerのoverflowをhiddenにすることで、box-containerの外の動きを隠し、何もないところへスッとスライドして消えるように見せている。
