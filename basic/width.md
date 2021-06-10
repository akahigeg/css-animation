# 幅の変更

---

### 要素にhoverで幅が徐々に大きくなる

#### 動作サンプル

<style>
  .box {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    margin-right: 10px;
    transition: all ease 1s 0s;
  }
  .box:hover {
    width: 300px;
  }
</style>

<div class="box-container">
  <div class="box">HOVER!</div>
</div>

#### HTML
```html
<div class="box-container">
  <div class="box">HOVER!</div>
</div>
```

#### CSS
```css
.box {
  width: 100px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  margin-right: 10px;
  transition: all ease 300ms 0s;
}
.box:hover {
  width: 300px;
}
```

#### 解説
hoverでwidthを変化させ、transitionによってアニメーション。

---

### 要素クリック時に一気に幅が伸び、徐々に元の幅に戻る

#### 動作サンプル

<style>
  .box2 {
    width: 100px;
    padding: 10px 0;
    border: 2px solid #000;
    text-align: center;
    margin-right: 10px;
    transition: all linear 1s 0s;
  }
  .box2:active {
    transition: none;
    width: 300px;
  }
</style>

<div class="box2-container">
  <div class="box2">CLICK!</div>
</div>

#### HTML
```html
<div class="box2-container">
  <div class="box2">CLICK!</div>
</div>
```

#### CSS
```css
.box2 {
  width: 100px;
  padding: 10px 0;
  border: 2px solid #000;
  text-align: center;
  margin-right: 10px;
  transition: all linear 300ms 0s;
}
.box2:active{
  transition: none;
  width: 300px;
}
```

#### 解説
activeでwidthを変化。transitionをnoneにすることで一瞬で幅が変化する。

activeが外れて元に戻る過程ではbox2のtransitionによるアニメーションが適用される。
