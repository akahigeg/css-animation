# ワイプイン

要素がワイプインして表示。文字が動くのではなく、もともと固定されて隠されていた文字が見えるようになるところがスライドインとは違う。

<style>
.box-container {
  width: 300px;
  display: flex;
  justify-content: center;
  align-items: center;

  border: 2px solid #333;
  padding: 5px;
}

.box {
  overflow: hidden;
  transform: translateX(-100%);
  transition: transform ease-in-out 0.5s;
}

.text {
  display: block;
  transform: translateX(100%);
  transition: transform ease-in-out 0.5s;
}

.box.-visible,
.box.-visible .text {
  transform: translateX(0);
}
</style>

### サンプル

<div class="box-container">
  <div class="box">
    <div class="text">ワイプイン</div>
  </div>
</div>

<script>
const box = document.getElementsByClassName("box")[0];

setInterval(() => {
  box.className = box.className + " -visible";
}, 1000);
</script>

### HTML
```html
<div class="box-container">
  <div class="box">
    <div class="text">ワイプイン</div>
  </div>
</div>

<script>
const box = document.getElementsByClassName("box")[0];

setInterval(() => {
  box.className = box.className + " -visible";
}, 1000);
</script>
```

### CSS
```css
.box-container {
  width: 300px;
  display: flex;
  justify-content: center;
  align-items: center;

  border: 2px solid #333;
  padding: 5px;
}

.box {
  overflow: hidden;
  transform: translateX(-100%);
  transition: transform ease-in-out 0.5s;
}

.text {
  display: block;
  transform: translateX(100%);
  transition: transform ease-in-out 0.5s;
}

.box.-visible,
.box.-visible .text {
  transform: translateX(0);
}
```

### 解説
初期はboxが左に100%ずれ、textが右に100%ずれた状態。boxのoverflow: hidden;によってtextの内容は表示されない。

1秒後にtranslateXでboxとtextの位置を0に戻すと、もともと隠れていたテキストがワイプインしてきたように見える。

100%と-100%を入れ替えたり、transralteXをtranslateYにすればワイプ方向を上下左右に切り替えられる。

参考: [簡単CSSアニメーション＆デザイン20選（ソースコードと解説付き）](https://baigie.me/officialblog/2021/02/25/css-tips-1/)