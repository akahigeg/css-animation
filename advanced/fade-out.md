# フェードアウト

要素がフェードアウトして非表示に。

<style>
  .box {
    width: 200px;
    height: 30px;
    border: 2px solid #000;
    text-align: center;

    animation: FadeOut 3s forwards;
  }
  @keyframes FadeOut {
    from {
      opacity: 1;
    }
    to {
      opacity: 0;
    }
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">フェードアウト</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">フェードアウト</div>
</div>
```

### CSS
```css
.box {
  width: 200px;
  height: 30px;
  border: 2px solid #000;
  text-align: center;

  animation: FadeIn 3s forwards;
}
@keyframes FadeIn {
  from {
    opacity: 0;
  }
  to {
    opacity: 1;
  }
}
```

### 解説
3秒かけてopacityを1から0に変化させてフェードアウト。

