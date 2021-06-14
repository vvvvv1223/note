[toc]

### 下拉菜单

js

```js

```

jquery

```js

```

### 显示隐藏密码

```html
<div class="box">
  <label for="">
    <img src="./img/eyes.png" alt="" id="eye" />
  </label>
  <input type="password" name="" id="password" />
</div>
```

```js
var eye = document.getElementById("eye");
var password = document.getElementById("password");
var flag = true; // true为隐藏
eye.onclick = function () {
  if (flag) {
    password.type = "value";
    eye.src = "./img/eye.png";
    // flag = false;
  } else {
    password.type = "password";
    eye.src = "./img/eyes.png";
    // flag = true;
  }
  flag = !flag;
};
```

### 排他思想
`如果有同一组元素, 我们想要某一个元素实现某种样式, 需要用到循环的排他思想(干掉其他人 留下我自己;即所有元素清除全部样式 再给当前元素设置元素)`
> js 实现

```html
<!-- 排他思想: 实现一排按钮的点击切换颜色 -->
<button>按钮1</button>
<button>按钮2</button>
<button>按钮3</button>
<button>按钮4</button>
<button>按钮5</button>
```

```js
// 1. 获取所有按钮 btns得到的是伪数组 里面的每一个元素为btns[i]
var btns = document.getElementsByTagName("button");
for (var i = 0; i < btns.length; i++) {
  btns[i].onclick = function () {
    // 先去掉所有按钮的背景颜色 再改变当前点击的按钮颜色
    for (var i = 0; i < btns.length; i++) {
      btns[i].style.backgroundColor = "";
    }
    this.style.backgroundColor = "pink"; // 这里只能用this
  };
}
```

> jQuery 实现

```js

```
