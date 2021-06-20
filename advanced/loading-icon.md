# ローディングアイコン

ローディングアイコンをコンテナエリアの中央に表示。

### 動作サンプル

<style>
  .box-container {
    width: 100%;
    height: 200px;

    border: 2px solid #000;

    display: flex;
    justify-content: center;
    align-items: center;
  }
  .loading-icon {
    box-sizing: border-box;
    width: 15px;
    height: 15px;
    margin: auto;
    padding: auto;
    border-radius: 50%;
    box-shadow:
      0 -30px 0 #eee,     /*  上  */
      21px -21px 0 #ddd,  /* 右上 */
      30px 0 0 #ccc,      /*  右  */
      21px 21px 0 #bbb,   /* 右下 */
      0 30px 0 #aaa,      /*  下  */
      -21px 21px 0 #999,  /* 左下 */
      -30px 0 0 #666,     /*  左  */
      -21px -21px 0 #000; /* 左上 */
    animation: rotate 1s steps(8) 0s infinite; 
  }
  @keyframes rotate {
    from {
      transform: rotate(0deg);
    }
    to {
      transform: rotate(360deg);
    }
  }
</style>

<div class="box-container">
  <div class="loading-icon"></div>
</div>

### HTML
```html
<div class="box-container">
  <div class="loading-icon"></div>
</div>
```

### CSS
```css
.box-container {
  width: 100%;
  height: 200px;

  border: 2px solid #000;

  display: flex;
  justify-content: center;
  align-items: center;
}
.loading-icon {
  box-sizing: border-box;
  width: 15px;
  height: 15px;
  margin: auto;
  padding: auto;
  border-radius: 50%;
  box-shadow:
    0 -30px 0 #eee,     /*  上  */
    21px -21px 0 #ddd,  /* 右上 */
    30px 0 0 #ccc,      /*  右  */
    21px 21px 0 #bbb,   /* 右下 */
    0 30px 0 #aaa,      /*  下  */
    -21px 21px 0 #999,  /* 左下 */
    -30px 0 0 #666,     /*  左  */
    -21px -21px 0 #000; /* 左上 */
  animation: rotate 1s steps(8) 0s infinite; 
}
@keyframes rotate {
  from {
    transform: rotate(0deg);
  }
  to {
    transform: rotate(360deg);
  }
}
```

### 解説
色違いのbox-shadowで円を描き、それを永遠に回転させる。

上下中央寄せにはflexboxを使った方法を利用。

参考: [簡単CSSアニメーション＆デザイン20選（ソースコードと解説付き）](https://baigie.me/officialblog/2021/02/25/css-tips-1/)