<style>
  .box {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    transition: all 300ms 0s ease;
  }
  .box:hover {
    transform: rotate(180deg);
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">BOX</div>
</div>

### 解説
hover時のスタイルにtransformでrotateを適用して回転させたもの