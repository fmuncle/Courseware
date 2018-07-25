# JavaScript 内置对象

## 1 Number

### 1.1 属性

* MAX_VALUE		JS可以表示的最大的数字
* MIN_VALUE		JS可以表示的最小的数字

### 1.2 方法

* toFixed(length)			指定保留长度的小数
* toExponential()			用科学计数法表示
* toPrecision(length)		要求数字按照指定长度显示   整数+小数
* toString(number)		      把数字转换为字符串 可以按照指定的 进制 返回



## 2 String

### 2.1 属性

* length			字符串长度

### 2.2 方法

* charAt(index)		返回指定位置的字符
* concat(string)		连接字符串
* indexOf(str)		返回小字符串在字符串对象中第一次出现位置  -1表示不存在
* lastIndexOf()		返回小字符在字符串中最后一次出现的位置
* substr(start, length)	截取字符串 省略长度截取到结束
* substring(start, end)	截取字符串, 省略结束位置 一直到最后
* slice(start, end)		与substring 一模一样
* split(char)		把字符串分割为数组
* toUpperCase()		把字符串转为大写
* toLowerCase()		把字符串转为小写
* match()		匹配字符串 可用正则
* search()		查找字符串 可用正则	
* replace()		替换字符串可用正则
* charCodeAt()		返回在指定的位置的字符的 Unicode 编码。
* String.formCharCode() 	从字符编码创建一个字符串。



## 3 Array

### 3.1 创建数组

* 使用直接量 `[]`
* 构造函数方式 `new Array()`

### 3.2 数组特点

* 索引必须连续
* 如果索引不连续，会产生稀疏数组

### 3.3 数组的遍历(迭代)	

* for 循环遍历		
* for...in 循环
* for...of 循环		



### 3.4 数组元素的添加和删除	

#### 添加	

* 为新索引赋值				
* 利用数组长度,在数组尾部插入新元素	
* push()					
* unshift()				
* splice()					

#### 删除	

* 改变数组长度				

* pop()					

* shift()					

* splice()					

* 运算符 delete	

  ​			

### 3.5 数组对象属性

* length  数组长度 元素个数

### 3.6 数组对象方法

* splice()	

  > 删除指定位置指定个数的元素	
  > 替换指定位置指定个数的元素	
  > 添加指定位置的元素		
  > 返回 被删除的元素组成的数组				

* reverse()  翻转数组

* sort()	数组排序

* push() 和 pop()	在数组的最后添加或删除元素	

* unshift()和shift()	在数组的最前面添加或删除元素	

* toString() 和 toLocalString()	把数组转换为字符串	

* join()	把数组的元素拼接成字符串	

* slice()	截取数组中的一部分,返回新的数组	slice(start, end)		

* concat()	 合并多个数组

* indexOf()   搜索数组中的元素，并返回它所在的位置。

* lastIndexOf()   返回一个指定的字符串值最后出现的位置，在一个字符串中的指定位置从后向前搜索。

* forEach()  遍历 循环

* map()  通过指定函数处理数组的每个元素，并返回处理后的数组。

* filter()   检测数值元素，并返回符合条件所有元素的数组。

* every()  检测数值元素的每个元素是否都符合条件。

* some()  检测数组元素中是否有元素符合指定条件。

* reduce()  将数组元素 索引值从低到高 进行组合
  reduceRight() 将数组元素 索引值从高到低进行组合

  

## 5 Function

### 5.1 属性

* prototype	原型

* length	形参的数量

### 5.2 方法

* apply()  将函数作为一个对象的方法调用
* call()    将函数作为对象的方法调用
* bind()  返回一个作为方法调用的函数



## 6 Math

### 6.1 属性

* PI		返回圆周率（约等于3.14159）。

### 6.2 方法

* abs(x)		返回数的绝对值。	
* sqrt(x)		返回数的平方根。	
* pow(x,y)	返回 x 的 y 次幂。	
* ceil(x)		对数进行上舍入。	
* floor(x)		对数进行下舍入。	
* round(x)	把数四舍五入为最接近的整数。	
* max(x,y)	返回 x 和 y 中的最高值。	
* min(x,y)	返回 x 和 y 中的最低值。	
* random()	返回 0 ~ 1 之间的随机数。	



## 7 Date

### 7.1 方法

* getYear()		请使用 getFullYear() 方法代替。	
* getFullYear()		从 Date 对象以四位数字返回年份。	
* getMonth()		从 Date 对象返回月份 (0 ~ 11)。	
* getDate()		从 Date 对象返回一个月中的某一天 (1 ~ 31)。	
* getDay()		从 Date 对象返回一周中的某一天 (0 ~ 6)。	
* getHours()		返回 Date 对象的小时 (0 ~ 23)。	
* getMinutes()		返回 Date 对象的分钟 (0 ~ 59)。	
* getSeconds()		返回 Date 对象的秒数 (0 ~ 59)。	
* getMilliseconds()	返回 Date 对象的毫秒(0 ~ 999)。	
* getTime()		返回 1970 年 1 月 1 日至今的毫秒数。	
* getTimezoneOffset()	返回本地时间与格林威治标准时间 (GMT) 的分钟差。	
* getUTC....		标准时区
* set...
* setUTC...
* toTimeString()		把 Date 对象的时间部分转换为字符串。	
* toDateString()		把 Date 对象的日期部分转换为字符串。	
* toUTCString()		根据世界时，把 Date 对象转换为字符串。	
* toLocaleString()	根据本地时间格式，把 Date 对象转换为字符串。	
* toLocaleTimeString()	根据本地时间格式，把 Date 对象的时间部分转换为字符串。	
* toLocaleDateString()	根据本地时间格式，把 Date 对象的日期部分转换为字符串。	



## 8 RegExp

### 8.1 属性

* global		RegExp 对象是否具有标志 g。	
* ignoreCase	RegExp 对象是否具有标志 i。	
* lastIndex	一个整数，标示开始下一次匹配的字符位置。	
* multiline	RegExp 对象是否具有标志 m。	
* source		正则表达式的源文本。

### 8.2 方法

* exec()		检索字符串中指定的值。返回找到的值，并确定其位置。	
* test()		检索字符串中指定的值。返回 true 或 false。



## 9 JSON

### 9.1方法 

* JSON.parse()		解析json格式的字符串
* JSON.stringify()	序列化对象 数组 或 原始值



## 10 Global

### 10.1 属性

* NaN
* InFinity

### 10.2 方法

* escape()			对字符串进行Unicode编码。	
* unescape()			对由 escape() 编码的字符串进行解码。
* encodeURI()			把字符串编码为 URI。	对其他一些在网址中有特殊含义的符号“; / ? : @ & = + $ , #”不进行编码
* decodeURI()			解码某个编码的 URI。
* encodeURIComponent()	把字符串编码为 URI 组件
* decodeURIComponent()	解码一个编码的 URI 组件。
* eval()			计算 JavaScript 字符串，并把它作为脚本代码来执行。	
* isFinite()		检查某个值是否为有穷大的数。	
* isNaN()			检查某个值是否是数字。	
* parseInt()		解析一个字符串并返回一个整数。	
* parseFloat()		解析一个字符串并返回一个浮点数。	
* Number()		把对象的值转换为数字。	
* String()			把对象的值转换为字符串。
* 所有内置构造函数 都是 全局对象的属性

