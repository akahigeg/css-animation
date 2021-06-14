# バウンド

要素がバウンドし続ける。

### 動作サンプル

<style>
.box-container {
  height: 120px;
}
.box {
  width: 20px;
  height: 20px;
  border: 2px solid #000;
  text-align: center;
  animation: Bound 1s infinite;
}

@keyframes Bound {
  0% {
    transform: translateY(100px);
  }
  50% {
    transform: translateY(0px);
    animation-timing-function: ease-out;
  }
  75% {
    transform: translateY(5px);
    animation-timing-function: ease-in;
  }
  100% {
    transform: translateY(100px);
  }
}
</style>

<div class="box-container">
  <div class="box"></div>
</div>

#### HTML
```html
<div class="box-container">
  <div class="box"></div>
</div>
```

### CSS
```css
.box-container {
  height: 120px;
}
.box {
  width: 20px;
  height: 20px;
  border: 2px solid #000;
  text-align: center;
  animation: Bound 1s infinite;
}

@keyframes Bound {
  0% {
    transform: translateY(100px);
  }
  50% {
    transform: translateY(0px);
    animation-timing-function: ease-out;
  }
  75% {
    transform: translateY(5px);
    animation-timing-function: ease-in;
  }
  100% {
    transform: translateY(100px);
  }
}
```

### 解説
keyframesでtranslateYの値を変更し、パーセントとanimation-timing-functionで加速と失速のタイミングを調整。

バウンドの速さはanimation-durationで調整できる。