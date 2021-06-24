# バウンドするNEXTボタン

バウンドのアニメーションで目を引くNEXTボタン。

### 動作サンプル

<style>
  .box {
    display: flex;
    justify-content: center;
    align-items: center;

    width: 100px;

    padding: 5px 5px 5px 2px;
    background-color: #eee;

    border-radius: 5px;
    border: 2px solid #333;

    animation: Bound 1s infinite;
  }
  .arrow-icon {
    box-sizing: border-box;
    display: inline-block;
    width: 10px;
    height: 10px;
    border-style: solid;
    border-width: 3px 3px 0 0;
    border-color: #666;
    transform: rotate(45deg);
    margin-left: -4px;
  }
  .next-text {
    padding-left: 6px;
    font-size: 16px;
    font-weight: bold;

    color: #666;
  }

  @keyframes Bound {
    from {
      transform: translateY(-5px);
    }
    40% {
      transform: translateY(-1px);
      animation-timing-function: linear;
    }
    50% {
      transform: translateY(0px);
      animation-timing-function: linear;
    }
    95% {
      transform: translateY(0px);
      animation-timing-function: linear;
    }
    to {
      transform: translateY(-5px);
    }
  }
</style>

<div class="box-container">
  <div class="box">
    <i class="arrow-icon"></i><i class="arrow-icon"></i><div class="next-text">NEXT</div>
  </div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">
    <i class="arrow-icon"></i><i class="arrow-icon"></i><div class="next-text">NEXT</div>
  </div>
</div>
```

### CSS
```css
  .box {
    display: flex;
    justify-content: center;
    align-items: center;

    width: 100px;

    padding: 5px 5px 5px 2px;
    background-color: #eee;

    border-radius: 5px;
    border: 2px solid #333;

    animation: Bound 1s infinite;
  }
  .arrow-icon {
    box-sizing: border-box;
    display: inline-block;
    width: 10px;
    height: 10px;
    border-style: solid;
    border-width: 3px 3px 0 0;
    border-color: #666;
    transform: rotate(45deg);
    margin-left: -4px;
  }
  .next-text {
    padding-left: 6px;
    font-size: 16px;
    font-weight: bold;

    color: #666;
  }

  @keyframes Bound {
    from {
      transform: translateY(-5px);
    }
    40% {
      transform: translateY(-1px);
      animation-timing-function: linear;
    }
    50% {
      transform: translateY(0px);
      animation-timing-function: linear;
    }
    95% {
      transform: translateY(0px);
      animation-timing-function: linear;
    }
    to {
      transform: translateY(-5px);
    }
  }
```

### 解説
矢印アイコンはCSSで作成。
正方形の要素のborderを上と右だけ表示して45度傾け。

キーフレームでバウンドのアニメーションを定義してボックスに付加。いいかんじにバウンドするよう調整するのが難しい。

