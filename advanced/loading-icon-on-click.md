# クリックでローディングアイコン

ボタンクリックでローディングアイコンをボタンの中央に表示。

処理が終わったらローディングアイコンを非表示に。

### 動作サンプル

<style>
  .box {
    width: 200px;
    border: 2px solid #000;

    text-align: center;
    position: relative;
  }
  .box_loading {
    background-color: #eee;
    border-color: #999;
  }
  .loading-icon {
    position: absolute;
    top: 0;
    right: 0;
    bottom: 0;
    left: 0;
    margin: auto;

    box-sizing: border-box;
    width: 4px;
    height: 4px;
    margin: auto;
    padding: auto;
    border-radius: 50%;
    box-shadow:
      0 -10px 0 #eee,     /*  上  */
      7px -7px 0 #ddd,  /* 右上 */
      10px 0 0 #ccc,      /*  右  */
      7px 7px 0 #bbb,   /* 右下 */
      0 10px 0 #aaa,      /*  下  */
      -7px 7px 0 #999,  /* 左下 */
      -10px 0 0 #666,     /*  左  */
      -7px -7px 0 #000; /* 左上 */
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
  <div id="box" class="box">CLICK!</div>
</div>

<script>
  const box = document.getElementById("box");
  const loadingIcon = document.createElement("div");
  loadingIcon.className = "loading-icon";

  box.addEventListener("click", () => {
    /* ローディング中にクリックしても反応しないように */
    if (box.className.indexOf("box_loading") == -1) {
      box.appendChild(loadingIcon);
      box.className = box.className + " box_loading";
      window.setTimeout(() => {
        box.removeChild(loadingIcon);
        box.className = box.className.replace(" box_loading", "");
      }, 2000);
    }

  });
</script>

### HTML
```html
<div class="box-container">
  <div id="box" class="box">CLICK!</div>
</div>

<script>
  const box = document.getElementById("box");
  const loadingIcon = document.createElement("div");
  loadingIcon.className = "loading-icon";

  box.addEventListener("click", () => {
    /* ローディング中にクリックしても反応しないように */
    if (box.className.indexOf("box_loading") == -1) {
      box.appendChild(loadingIcon);
      box.className = box.className + " box_loading";
      window.setTimeout(() => {
        box.removeChild(loadingIcon);
        box.className = box.className.replace(" box_loading", "");
      }, 2000);
    }

  });
</script>
```

### CSS
```css
.box {
  width: 200px;
  border: 2px solid #000;

  text-align: center;
  position: relative;
}
.box_loading {
  background-color: #eee;
  border-color: #999;
}
.loading-icon {
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  margin: auto;

  box-sizing: border-box;
  width: 4px;
  height: 4px;
  margin: auto;
  padding: auto;
  border-radius: 50%;
  box-shadow:
    0 -10px 0 #eee,     /*  上  */
    7px -7px 0 #ddd,  /* 右上 */
    10px 0 0 #ccc,      /*  右  */
    7px 7px 0 #bbb,   /* 右下 */
    0 10px 0 #aaa,      /*  下  */
    -7px 7px 0 #999,  /* 左下 */
    -10px 0 0 #666,     /*  左  */
    -7px -7px 0 #000; /* 左上 */
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
JavaScriptを利用してボタンクリックした時に[ローディングアイコン](loading-icon.md)をボタン上にappendChildで表示させ、ボタンにbox_loadingクラスを付加して非アクティブ状態とする。

処理が終了したらローディングアイコンをremoveChildで非表示にして、ボタンからbox_loadingクラスを削除してアクティブ状態に戻す。

setTimeoutで2秒後に処理終了をシミュレート。


参考: [簡単CSSアニメーション＆デザイン20選（ソースコードと解説付き）](https://baigie.me/officialblog/2021/02/25/css-tips-1/)
