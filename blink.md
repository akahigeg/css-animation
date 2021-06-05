## ブリンク

<style>
  .box {
    width: 50px;
    border: 2px solid #000;
    text-align: center;
    animation: blink 0.5s linear alternate infinite forwards;
  }
  @Keyframes blink {
    from { opacity: 1; }
    50%  { opacity: 1; }
    51%  { opacity: 0; }
    to   { opacity: 0; }
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">BOX</div>
</div>

### HTML
    <div class="box-container">
      <div class="box">BOX</div>
    </div>

### CSS
    <style>
      .box {
        width: 50px;
        border: 2px solid #000;
        text-align: center;
        animation: blink 0.5s linear alternate infinite forwards;
      }
      @Keyframes blink {
        from { opacity: 1; }
        50%  { opacity: 1; }
        51%  { opacity: 0; }
        to   { opacity: 0; }
      }
    </style>

### 解説
なつかしの