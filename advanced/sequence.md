# 連続アニメーション

複数のアニメーションを時間差で実行する例。

<style>
  .box {
    width: 20px;
    height: 20px;
    border: 2px solid #000;
    text-align: center;
    animation: 
      changeH 1s ease 0s alternate forwards,
      changeW 1s ease 1s alternate forwards,
      changeH 1s ease 2s reverse forwards,
      changeW 1s ease 3s reverse forwards;
  }
  @Keyframes changeH {
    from { height: 20px; }
    to   { height: 40px;}
  }
  @Keyframes changeW {
    from { width: 20px;}
    to   { width: 40px;}
  }
</style>

### サンプル
<div class="box-container">
  <div class="box"></div>
</div>

### HTML
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
  animation: 
    changeH 1s ease 0s alternate forwards,
    changeW 1s ease 1s alternate forwards,
    changeH 1s ease 2s reverse forwards,
    changeW 1s ease 3s reverse forwards;
}
@Keyframes changeH {
  from { height: 20px; }
  to   { height: 40px;}
}
@Keyframes changeW {
  from { width: 20px;}
  to   { width: 40px;}
}
```

### 解説
animationに複数の関数を指定できる。ディレイを調整すれば自然なアニメーションとなる。
