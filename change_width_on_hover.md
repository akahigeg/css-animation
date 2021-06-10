## hover時に幅を伸ばす
<style>
  .box {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    transition: all ease 1s 0s;
  }
  .box:active {
    width: 200px;
  }
</style>

### サンプル
<div class="box-container">
  <div class="box">BOX</div>
</div>

### HTML
```html
<div class="box-container">
  <div class="box">BOX</div>
</div>
```

### CSS
    <style>
      .box {
        width: 100px;
        padding: 10px 0;
        border: 2px solid #000;
        text-align: center;
        transition: all ease 300ms 0s;
      }
      .box:hover {
        width: 300px;
        transition-duration: 10s;
      }
    </style>

### 解説
box1クラスにtransitionを指定することでhover時の変化にアニメーションの効果を得られる。box1クラスにtransitionを指定することでhover時の変化にアニメーションの効果を得られる。box1クラスにtransitionを指定することでhover時の変化にアニメーションの効果を得られる。box1クラスにtransitionを指定することでhover時の変化にアニメーションの効果を得られる。box1クラスにtransitionを指定することでhover時の変化にアニメーションの効果を得られる。

    transition: all 300ms 0s ease

は以下のプロパティをまとめたもの。
  
    transition-property: all;
    transition-timing-function: ease;
    transition-duration: 300ms;
    transition-delay: 0s;

<dl>
  <dt>transition-property</dt><dd>アニメーションの対象となるプロパティ</dd>
  <dt>transition-timing-function</dt><dd>アニメーションのタイミング</dd>
  <dt>transition-duration</dt><dd>アニメーションに要する時間</dd>
  <dt>transition-delay</dt><dd>アニメーション開始までの時間（ディレイ）</dd>
</dl>