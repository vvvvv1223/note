### 得到当前年月日时分秒

```js
// 要求输出: xx年xx月xx日星期x xx:xx:xx
function getTime() {
  var date = new Date();
  var year = date.getFullYear();
  var month = date.getMonth() + 1;
  var day = date.getDate();
  var arr = ["星期日", "星期一", "星期二", "星期三", "星期四", "星期五", "星期六"];
  var d = date.getDay(); // 返回指定日期对象的星期中的第几天（0-6）
  var h = date.getHours();
  h = h < 10 ? "0" + h : h;
  var m = date.getMinutes();
  m = m < 10 ? "0" + m : m;
  var s = date.getSeconds();
  s = s < 10 ? "0" + s : s;
  return `${year}年${month}月${day}日${arr[d]} ${h}:${m}:${s}`;
}
console.log(getTime()); //2021年6月6日星期日 09:35:13
```

### 获取 date 总的毫秒数

```js
// 距离1970年1月1号过了多少毫秒数
var date = new Date();

// 方法一:
date.valueOf(); //1622943614259
date.getTime();

// 方法二:
var date1 = +new Date();

// 方法三: h5新增
Date.now();
```

### 5 秒后自动跳转页面 并倒计时

```js
var div = document.getElementById("hh");
var timer = 5;
setInterval(() => {
  if (timer == 0) {
    location.href = "http://www.baidu.com";
  } else {
    div.innerHTML = "您将在" + timer + "秒后跳转到百度";
  }
  timer--;
}, 1000);
```

### 数组去重 简易版
```js
// 数组去重 简易版
// 遍历旧数组 用旧数组的元素查询新数组 如果该元素在新数组中则不添加
var arr = ['c','a','z','a','x','a','x','c','b'];
var newArr = [];
arr.map((item,i,arr) => {
if(newArr.indexOf(item) == -1) {
  newArr.push(item);
}
})
console.log(newArr); //["c", "a", "z", "x", "b"]
```