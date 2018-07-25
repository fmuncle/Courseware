# JavaScript 函数和对象

## 1 JavaScript 函数

### 1.1 声明函数的方式

* function 关键字			

* 匿名函数方式(表达式方式)	

* Function 构造函数方式		

  

### 1.2 参数问题

* 形参和实参数量问题			
* 可选形参(参数默认值)			
* 可变长的实参列表:实参对象 aruguments 



### 1.3 回调函数

一个函数就可以接收另一个函数作为参数，这种函数就称之为回调函数(高阶函数)

```js
function add(x, y, f) {
    return f(x) + f(y);
}
add(-5, 6, Math.abs)
```



### 1.4 递归函数

函数内部调用自己就是递归函数，

```js
//用递归 实现阶乘
function multiply(n) {
    if (n == 1) {
        return 1
    }
    return n * multiply(n - 1)
}
```



### 1.5 自调函数

函数生声明完 直接调用

```js
(function(){
    console.log('ok')
})()
```



### 1.6 闭包函数

当一个函数返回了一个函数后，其内部的局部变量还被新函数引用，形成闭包

```js
function count() {
    var arr = [];
    for (var i=1; i<=3; i++) {
        arr.push((function (n) {
            return function () {
                return n * n;
            }
        })(i));
    }
    return arr;
}

var results = count();
var f1 = results[0];
var f2 = results[1];
var f3 = results[2];

f1(); // 1
f2(); // 4
f3(); // 9
```



## 2 JavaScript 作用域

### 2.1 局部作用域

函数中使用定义的变量就是局部变量，只能在本函数中使用



### 2.2 全局作用域

在，函数外面，定义的变量是全局变量。哪都可以用

**变量提升**

```js
var a = 100
function demo(){
    console.log(a)
    var a = 200
}
```



### 2.3 作用域链

函数嵌套函数会形成作用域链

```js
function demo(){
    function fn(){
        function fn1() {
            
        }
    }
}
```



### 2.4 块状作用域(ES6)

使用`let`关键字声明的变量会具有块状作用域

```j&#39;s
for (let i = 0; i < 10; i ++) {
    
}

console.log(i) //变量不存在
```





