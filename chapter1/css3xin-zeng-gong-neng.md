# CSS3新增功能

## 1 CSS3选择器详解

### 1.1 基础选择器

* 通配选择器`*`
* 元素选择器`E`
* ID选择器`#id`
* CLASS选择器`.class`
* 群组选择器`select1,selectN`



### 1.2 层次选择器

* 后代选择器  `E F`
* 子选择器  `E>F`
* 相邻兄弟选择器  `E+F`
* 通用兄弟选择器  `E~F`



### 1.3 属性选择器

* `E[attr]`  选择具有att属性的E元素。 
* `E[attr="val"]`  选择具有att属性且属性值等于val的E元素。 
* `E[attr~="val"]`  选择具有att属性且属性值为一用空格分隔的字词列表，其中一个等于val的E元素（包含只有一个值且该值等于val的情况）。 
* `E[attr^="val"] ` 选择具有att属性且属性值为以val开头的字符串的E元素。
* `E[attr$="val"] `选择具有att属性且属性值为以val结尾的字符串的E元素。 
* `E[attr*="val"]` 选择具有att属性且属性值为包含val的字符串的E元素。 
* `E[attr|="val"]` 选择具有att属性且属性值为以val开头并用连接符"-"分隔的字符串的E元素，如果属性值仅为val，也将被选择。



### 1.4 伪类选择器

#### 动态伪类选择器

* `E:link`

​	设置超链接a在未被访问前的样式。 
	注意，a:hover 必须位于 a:link 和 a:visited 之后，a:active 必须位于 a:hover 之后

* `E:visited`

​	设置超链接a在其链接地址已被访问过时的样式。 

* `E:hover`

​	设置元素在其鼠标悬停时的样式。 

* `E:active`

​	设置元素在被用户激活（在鼠标点击与释放之间发生的事件）时的样式。

* `E:focus`

​	设置对象在成为输入焦点（该对象的onfocus事件发生）时的样式。

#### 目标伪类选择器

* `E:target`

​	匹配相关URL指向的E元素。 

#### 语言伪类选择器

* `E:lang(fr)`

​	匹配使用特殊语言的E元素

#### UI元素伪类选择器

* `E:checked`

​	匹配用户界面上处于选中状态的元素E。(用于input type为radio与checkbox时) 

* `E:enabled`

​	匹配用户界面上处于可用状态的表单元素

* `E:disabled`

​	匹配用户界面上处于禁用状态的表单元素

#### 结构伪类选择器

* `E:root`

​	匹配E元素在文档的根元素。在HTML中，根元素永远是HTML 

* `E:first-child`

​	匹配父元素的第一个子元素E。 

* `E:last-child`

​	匹配父元素的最后一个子元素E。 

* `E:only-child`

​	匹配父元素仅有的一个子元素E。

* `E:nth-child(n)`

​	匹配父元素的第n个子元素E，假设该子元素不是E，则选择符无效。

* `E:nth-last-child(n)`

​	匹配父元素的倒数第n个子元素E，假设该子元素不是E，则选择符无效。

* `E:first-of-type`

​	匹配同类型中的第一个同级兄弟元素E

* `E:last-of-type`

​	匹配同类型中的最后一个同级兄弟元素E

* `E:only-of-type`

​	匹配同类型中的唯一的一个同级兄弟元素E

* `E:nth-of-type(n)`

​	匹配同类型中的第n个同级兄弟元素E

* `E:nth-last-of-type(n)`

​	匹配同类型中的倒数第n个同级兄弟元素E

* `E:empty`

​	匹配没有任何子元素（包括text节点）的元素E

#### 否定伪类选择器

* `E:not(s)`

​	匹配不含有s选择符的元素E



### 1.5 伪元素选择器

* `E:first-letter/E::first-letter`

​	设置对象内的第一个字符的样式。 

* `E:first-line/E::first-line` 

​	设置对象内的第一行的样式。

* `E:before/E::before` 

​	设置在对象前（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用

* `E:after/E::after`

​	设置在对象后（依据对象树的逻辑结构）发生的内容。用来和content属性一起使用

* `E::placeholder` 

​	设置对象文字占位符的样式。 

* `E::selection` 

​	设置对象被选择时的样式。 





## 2 

