# 位置の移動（スライド）

要素が表示と同時にスライド。

### 動作サンプル

<style>
  .box {
    width: 20px;
    height: 20px;
    border: 2px solid #000;
    text-align: center;

    animation: Slide 1s forwards;
  }
  @keyframes Slide {
    from {
      transform: translateX(0px);
    }
    to {
      transform: translateX(300px);
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
.box {
  width: 20px;
  height: 20px;
  border: 2px solid #000;
  text-align: center;

  animation: Slide 1s;
}
@keyframes Slide {
  from {
    transform: translateX(0px);
  }
  to {
    transform: translateX(300px);
  }
}
```

### 解説
translateXで位置を変化させる。

```animation-fill-mode: forwards;```を指定することでアニメーション後の状態を維持（指定しないとfromの状態に戻る）