# JavaScript 基础语法

## 1 谈谈 JavaScript

JavaScript，通常会简称为'JS', 是一种浏览器脚本语言
### 1.1 JavaScript 编程语言特点
* JavaScript是一种脚本编程语言		

	 JavaScript是一种解释性语言		 

	 Javas的语法结构与C++、java十分类似	

	 JavaScript是弱类型语言			

	 JavaScript是事件驱动的语言		

	 JavaScript是一种基于对象的语言 	

	 JavaScript具有跨平台性。		

	 JavaScript具有安全性与简单性		

   

### 1.2 JavaScript的发展历史 

* 1990年底，欧洲核能研究组织（CERN）科学家Tim Berners-Lee，发明了万维网（World Wide Web）.
* 1992年底，美国国家超级电脑应用中心（NCSA）开始开发一个独立的浏览器，叫做Mosaic。
* 1994年10月，NCSA的一个主要程序员Marc Andreessen联合风险投资家Jim Clark，成立了Mosaic通信公司，不久后改名为Netscape(网景)。
* 1994年12月，Netscape发布浏览器Navigator1.0，市场份额一举超过90%。
* 1995年 Netscape 程序员 Brendan Eich 设计出了LiveScript1.0  后来 改名 JavaScript
* 1996年3月，Navigator 2.0浏览器正式内置了JavaScript脚本语言。
* 1996年8月，微软模仿JavaScript开发了一种相近的语言，取名为JScript, 内置于IE3.0
* 1996年11月，网景公司决定将JavaScript提交给欧洲计算机制造联合会ECMA，希望JavaScript能够成为国际标准，以此抵抗微软。
* 1997年7月，ECMA组织发布262号标准文件（ECMA-262）的第一版，规定了浏览器脚本语言的标准，并将这种语言称为ECMAScript。这个版本就是ECMAScript 1.0版。
* 1998年6月，ECMAScript 2.0版发布。
* 1999年12月，ECMAScript 3.0版发布
* 2008年7月，由于对于下一个版本应该包括哪些功能，各方分歧太大，争论过于激进，ECMA开会决定，中止ECMAScript 4.0的开发，将其中涉及现有功能改善的一小部分，发布为ECMAScript 3.1
* 2009年12月，ECMAScript 5.0版正式发布。
* 2011年6月，ECMAscript 5.1版发布，并且成为ISO国际标准
* 2015年6月17日，ECMAScript 6发布正式版本，即ECMAScript 2015
* 此后，每年6月ECMAScript 都会发布新的版本 (ES2016、ES2017、ES2018)



### 1.3 JavaScript 应用领域

* WEB前端 (页面特效，页面渲染)

* WEB后端 (Node.js)

* Hybrid App(混合App) 

* 桌面应用  如 网易有道的产品、豌豆荚

* 游戏 (Cocos2d.js、Unity3D)

  

### 1.4 JavaScript 组成部分

* ECMAScript 核心语法 (ActionScript有使用ECMAScript语法)
* BOM 浏览器对象模型
* DOM 文档对象模型



## 2 JavaScript基本语法

### 2.1 在HTML中使用

* 在`<script>`标签内 写代码

  ```html
  <script>
      alert('hello world')
  </script>
  ```

* 引入外部 脚本文件

  ```html
  <script src="./script.js"></script>
  ```

* 通过事件属性定义在元素内部

  ```html
  <button onclick="alert('啊，好疼啊')">点我啊</button>
  ```



### 2.2 JavaScript 注释

* 单行注释

  ```js
  // 我是注释
  ```

* 多行注释

  ```js
  /*
   多行注释
  */
  ```

  

### 2.3 指令(语句)结束符

```js
alert('大家好');
alert('大家好');

alert('大家好')
alert('大家好')
alert('大家好')
```



### 2.4 输出内容

```js
document.write('你是不是喜欢我?');  //直接输出到页面
console.log('hello world');  //控制台输出
```



### 2.5 变量

```js
//javascript 使用var 关键字定义变量
var username = 'xiaolili'

//ES6 中新增 let关键字
let userage = 100
```

**变量名命名规范**

```
标识符必须 由 "数字","字母", "_"  或者 "$" 组成,并且不能以数字 开头
标识符不能与保留字冲突
区分大小写
```

**保留字**

|          |           |            |           |              |
| -------- | --------- | ---------- | --------- | ------------ |
| abstract | arguments | boolean    | break     | byte         |
| case     | catch     | char       | class*    | const        |
| continue | debugger  | default    | delete    | do           |
| double   | else      | enum*      | eval      | export*      |
| extends* | false     | final      | finally   | float        |
| for      | function  | goto       | if        | implements   |
| import*  | in        | instanceof | int       | interface    |
| let      | long      | native     | new       | null         |
| package  | private   | protected  | public    | return       |
| short    | static    | super*     | switch    | synchronized |
| this     | throw     | throws     | transient | true         |
| try      | typeof    | var        | void      | volatile     |
| while    | with      | yield      |           |              |



##  3 第一个JavaScript 程序

* 三个基本弹框	

  ```js
  alert()
  confirm()
  prompt()
  ```

* 获取HTML中的DOM元素

  ```js
  document.getElementById()	
  ```

	 元素的应用	得到元素的属性

	 事件的应用	触发了事件在执行某段代码

	 函数的应用	

	 运算符的应用		
	 添加改变元素的内容		 



## 4 JavaScript 数据类型

### 4.1 数据类型

JavaScript的数据类型分为原始类型和对象类型，这里我们先来了解原始类型

#### 原始类型

* 数字 Number	
	 字符串  String	
* 布尔值  Boolean
	 空  null		
* 未定义  undefind

#### 对象类型

数组  Array、函数  Function、日期  Date	、正则  RegExp、错误  Error、对象 Object等

#### 函数监测

```
typeof(100)
typeof(username)
```



### 4.2 数字 Number

#### 定义

* 十进制表示			
	 十六进制表示			
	 科学计数法表示	

#### 浮点精度问题

```js
console.log(.1 + .2)
```

#### 数值范围

可表示的数字范围： `-5e324 ~ 1.7976931348623157e+308`	 

超过范围，会显示为 Infinity(正无穷) 或 -Infinity(负无穷)	

```js
isFinite()	//函数判断是否在范围内
```

#### 特殊的Number值 NaN

表示Not A Number，类型是Number 但又不是常规的数字

和任何值都不相等		

与任何值运算,结果还是NaN	

```js
isNaN()	//函数 判读是否是 NaN	
```



### 4.3 字符串 String

#### 声明方式

* 双引号

* 单引号

* 模板字符串(ES6新增)

  ```js
  content = `
  打扎好，我寺${username}.
  是兄弟，就来砍我
  今晚八点，不见不散
  `
  //多行，${}方式 嵌入变量。 传统方式变量字符串连接必须用字符串连接符
  ```

#### 字符串连接符

* `+`

#### 转义字符

```
\b 退格 		
\f 走纸换页 	
\n 换行 		
\r 回车 		
\t 水平制表符	
\' 单引号 	
\" 双引号 	
\\ 反斜杠 	
\xXX 十六进制XX指定的Latin-1 字符		
\xXXXX 十六进制XXXX指定的Unicode 字符	
```



### 4.4 布尔值 Boolean

```js
let a = true
let b = false
while (true) {
    
}
```



### 4.5 null和undefind

* `null` 表示未定义的对象
* `undefined` 表示"缺少值"



### 4.6 数据类型转换

#### 显示类型转换

* Number()
* parseInt()
* parseFloat()	
* String()		
* Boolean()	

#### 自动类型转换

当JavaScript想使用A类型的值得时候,而你提供的是B类型的值,JavaScript会自动把B类型转换为A类型 

#### 转换规则

| 原始值              | 转换为数字 | 转换为字符串      | 转换为布尔值 |
| ------------------- | ---------- | ----------------- | ------------ |
| false               | 0          | "false"           | false        |
| true                | 1          | "true"            | true         |
| 0                   | 0          | "0"               | false        |
| 1                   | 1          | "1"               | true         |
| "0"                 | 0          | "0"               | true         |
| "000"               | 0          | "000"             | true         |
| "1"                 | 1          | "1"               | true         |
| NaN                 | NaN        | "NaN"             | false        |
| Infinity            | Infinity   | "Infinity"        | true         |
| -Infinity           | -Infinity  | "-Infinity"       | true         |
| ""                  | 0          | ""                | false        |
| "20"                | 20         | "20"              | true         |
| "Runoob"            | NaN        | "Runoob"          | true         |
| [ ]                 | 0          | ""                | true         |
| [20]                | 20         | "20"              | true         |
| [10,20]             | NaN        | "10,20"           | true         |
| ["Runoob"]          | NaN        | "Runoob"          | true         |
| ["Runoob","Google"] | NaN        | "Runoob,Google"   | true         |
| function(){}        | NaN        | "function(){}"    | true         |
| { }                 | NaN        | "[object Object]" | true         |
| null                | 0          | "null"            | false        |
| undefined           | NaN        | "undefined"       | false        |



## 5 JavaScript 运算符

### 5.1 算术运算符	

* 加法运算符		+
* 减法运算符		-
* 乘法运算符		*
* 除法运算符		/
* 模运算符		  %
* 负号运算符		-
* 正号运算符		+
* 递增运算符		++
* 递减运算符		--



### 5.2 关系运算符	

* 相等运算符 `==`
* 全等运算符 `===`
* 不等运算符 `!=`
* 不全等运算符 `!==`
* 小于运算符 `<`
* 大于运算符 `>`
* 小于或等于运算符 `<=`
* 大于或等于运算符 `>=`
* `in`运算符	 判断一个值是否属于某个数组或者一个属性是否属于一个对象
* `instanceof`	判断一个对象的实例是否属于某个对象



### 5.3 逻辑运算符	

* 逻辑与 `&&`
* 逻辑或 `||`
* 逻辑非 `!`



### 5.4 位运算符	

* 按位与 `&`
* 按位或  `|`
* 按位异或  `^`
* 按位非  `~`
* 左移  `<<`
* 右移  `>>`



### 5.5 赋值运算符	

* `=`

* `+=`

* `-=`

* `/=`

* `*=`

* `%/`

* `<<=`

* `>>=`

* `&=`

* `|=`

* `^=`

  

### 5.6 其他运算符	

* 条件运算符   `?:`
* `typeof`运算符   判断操作数类型
* `delete`运算符  删除对象属性或者数组元素
* `void`运算符    忽略操作数的值
* 逗号运算符 ` ,`
* 字符串连接  `+`



### 5.7 运算符分类

#### 按照功能

* 算数运算符	
* 关系运算符	
* 逻辑运算符	
* 位运算符	
* 赋值运算符	
* 其他运算符	

#### 按照操作数

* 一元运算符
* 二元运算符
* 三元运算符



### 5.8 运算符优先级

| 运算符                             | 描述                                         |
| ---------------------------------- | -------------------------------------------- |
| . [] ()                            | 字段访问、数组下标、函数调用以及表达式分组   |
| ++ -- - ~ ! delete new typeof void | 一元运算符、返回数据类型、对象创建、未定义值 |
| * / %                              | 乘法、除法、取模                             |
| + - +                              | 加法、减法、字符串连接                       |
| << >> >>>                          | 移位                                         |
| < <= > >= instanceof               | 小于、小于等于、大于、大于等于、instanceof   |
| == != === !==                      | 等于、不等于、严格相等、非严格相等           |
| &                                  | 按位与                                       |
| ^                                  | 按位异或                                     |
| \|                                 | 按位或                                       |
| &&                                 | 逻辑与                                       |
| \|\|                               | 逻辑或                                       |
| ?:                                 | 条件                                         |
| = oP=                              | 赋值、运算赋值                               |
| ,                                  | 多重求值                                     |



## 6 流程控制语句

### 6.1 条件语句(分支结构)

#### 单向分支 if

```js
if (表达式) {
    code...
}
```

#### 双向分支 if...else

```js
if (表达式) {
    code...
} else {
    code...
}
```

#### 多向分支 if... else if

```js
if (表达式) {
    code...
} else if (表达式) {
    code...
} else if (表达式) {
    code...
} else {
    code...
}
```

#### 多向分支 switch...case

```js
switch (表达式) {
    case 表达式可能的值: code....; break;
    case 表达式可能的值: code....; break;
    case 表达式可能的值: code....; break;
    case 表达式可能的值: code....; break;
    default: code....;
}
```

#### 分支结构嵌套

```js
if (表达式) {
    if (表达式) {
        code....
    }
    code ...
} else {
    code...
}
```



### 6.2 循环

#### while 循环

```js
while (循环条件) {
    code...
}
```

#### do...while循环

```js
do {
    code...
} while (循环条件)
```

#### for 循环

```js
for (循环变量; 循环条件; 循环变量变化) {
    code ...
}
    
//循环输出 0-10
for (var i = 0; i <= 10; i ++) {
	console.log(i)
}
```







