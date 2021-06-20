# フェードイン

要素がフェードインして表示。

<style>
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
</style>

### サンプル
<div class="box-container">
  <div class="box">フェードイン</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">フェードイン</div>
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
3秒かけてopacityを0から1に変化させてフェードイン。
