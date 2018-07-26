# JavaScript 事件机制

## 1 什么是事件

JavaScript 使我们有能力创建动态页面。事件是可以被 JavaScript 侦测到的行为。

网页中的每个元素都可以产生某些可以触发 JavaScript 函数的事件。比方说，我们可以在用户点击某按钮时产生一个 onClick 事件来触发某个函数。事件在 HTML 页面中定义。



## 2 把事件绑定给元素

#### 事件监听方式(标准方式)		

```
addEventListener(Event, fn)    (非IE IE9+)  
attachEvent(Event, fn)  (IE8-)
```

#### 把事件作为元素的方法		

```
dom.onclick = fn	
```

#### 把事件作为标签的内部属性	

```
<button onclick="code..">
```



## 3 给元素解除事件绑定	

#### 标准方式绑定的事件	

```
removeEventListener(event, fn)  (IE9+ 非IE)
detachEvent(Event, fn)   (IE8-)
```

#### 其他方式绑定		

```
重新绑定事件,用空的函数 覆盖 前面的
dom.onclick = function(){}
```



## 4 this在事件中的作用	

* 给一组元素绑定事件
* 在元素内部 通过属性形式 `<button onclick="fn(this)">`  此时this表示所在的元素		



## 5 事件列表

### 5.1 鼠标事件

```
click		单击左键
dblclick	双击 左键
contextmenu	右单击
mouseover	鼠标悬浮
mouseout	鼠标移出
mousedown	鼠标按键按下
mouseup	  	鼠标按键抬起
mousemove	鼠标移动
```



### 5.2 键盘事件

```
keydown		键盘按键 按下
keyup		键盘按键 抬起
keypress	 键盘按键 按下 (只有字符按键)  (控制按键不可以 Ctrl shift 上下左右都不行)
```

​	

### 5.3 文档事件

```
load			加载完成
unload			文档关闭
beforeunload	 文档关闭 (兼容性好)
```

​	

### 5.4 表单事件

```
submit		表单提交的时候, 绑定给form元素
reset		表单重置, 绑定给form元素
blur		失去焦点
focus		获得焦点
change		表单控制的内容改变   通常绑定给 radio checkbox select  如果绑定给输入的input, 必须满足 内容改变和失去焦点才能触发
select		input 或 textarea  内容被选中的时候触发
```



### 5.5 图片事件

```
abort		图片加载中断
load		图片加载完成
error		图片加载错误
```



### 5.6 其他事件

```
scroll		元素内部的内容滚动  适合于有滚动条的元素
resize		绑定给window, 窗口尺寸发生变化
```



## 6 Event对象

### 6.1 分类	

```
Event		
MouseEvent	
KeyboardEvent	
FocusEvent	
...................	
```



### 6.2 属性	

* clientX	鼠标的x坐标

* clientY	鼠标的Y坐标

* button	鼠标按键的标示

  ```
  值
  0	按了左键
  1	按了滚轮
  2	按了右键	
  ```

* keyCode	 键盘按键的值

* cancelBubble	阻止事件冒泡 设置为true

* target	返回触发此事件的元素

* tyep	返回事件类型

* timeStamp	返回触发事件的那一刻的时间戳(从页面打开的那一刻开始

* altKey		返回当事件被触发时，"ALT" 是否被按下。

* ctrlKey		返回当事件被触发时，"CTRL" 键是否被按下。

* shiftKey	   返回当事件被触发时，"SHIFT" 键是否被按下。

### 6.3 方法	

* stopPropagation()	阻止事件冒泡

* preventDefault()	 阻止元素默认的事件