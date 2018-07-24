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





## 2 CSS3 基本功能

### 2.1 CSS3新增长度单位

* rem  **相对于根元素(即html元素)font-size计算值的倍数**
* vm  **视口被均分为100单位的vw**
* vh  **视口被均分为100单位的vh**
* vmax **相对于视口的宽度或高度中较大的那个。其中最大的那个被均分为100单位的vmax**
* vmin **相对于视口的宽度或高度中较小的那个。其中最小的那个被均分为100单位的vmin**

### 2.2 CSS3新增颜色单位

* RGBA(R,G,B,A)    A：Alpha透明度。取值0~1之间。

* HSL(H,S,L)   

  > H:  Hue(色调)。0(或360)表示红色，120表示绿色，240表示蓝色，也可取其他数值来指定颜色。取值为：0 - 360
  >
  > S：Saturation(饱和度)。取值为：0.0% - 100.0%
  >
  > L：Lightness(亮度)。取值为：0.0% - 100.0%

* HSLA(H,S,L,A)

### 2.3 CSS3渐变(了解)

#### 线性渐变

**语法**

```
<linear-gradient> = linear-gradient([ [ <angle> | to <side-or-corner> ] ,]? <color-stop>[, <color-stop>]+)

<side-or-corner> = [left | right] || [top | bottom]

<color-stop> = <color> [ <length> | <percentage> ]?
```

**取值**

```
<angle>：用角度值指定渐变的方向（或角度）。
	to left： 设置渐变为从右到左。相当于: 270deg
	to right：设置渐变从左到右。相当于: 90deg
	to top：  设置渐变从下到上。相当于: 0deg
	to bottom： 设置渐变从上到下。相当于: 180deg。这是默认值，等同于留空不写。
<color-stop> 用于指定渐变的起止颜色：
	<color>：  指定颜色。
	<length>： 用长度值指定起止色位置。不允许负值
	<percentage>： 用百分比指定起止色位置。
```

**示例**

```css
linear-gradient(#fff, #333);
linear-gradient(to bottom, #fff, #333);
linear-gradient(to top, #333, #fff);
linear-gradient(180deg, #fff, #333);
linear-gradient(to bottom, #fff 0%, #333 100%);
```

#### 径向渐变

**语法**

```
<radial-gradient> = radial-gradient([ [ <shape> || <size> ] [ at <position> ]? , | at <position>, ]?<color-stop>[ , <color-stop> ]+)

<position> = [ <length>① | <percentage>① | left | center① | right ]? [ <length>② | <percentage>② | top | center② | bottom ]?

<shape> = circle | ellipse

<size> = <extent-keyword> | [ <circle-size> || <ellipse-size> ]

<extent-keyword> = closest-side | closest-corner | farthest-side | farthest-corner

<circle-size> = <length>

<ellipse-size> = [ <length> | <percentage> ]{2}

<shape-size> = <length> | <percentage>

<color-stop> = <color> [ <length> | <percentage> ]?
```

**取值**

```
<position> 确定圆心的位置。如果提供2个参数，第一个表示横坐标，第二个表示纵坐标；如果只提供一个，第二值默认为50%，即center
	<percentage>①：用百分比指定径向渐变圆心的横坐标值。可以为负值。
	<length>①：用长度值指定径向渐变圆心的横坐标值。可以为负值。
	left：设置左边为径向渐变圆心的横坐标值。
	center①：设置中间为径向渐变圆心的横坐标值。
	right：设置右边为径向渐变圆心的横坐标值。
	<percentage>②：用百分比指定径向渐变圆心的纵坐标值。可以为负值。
	<length>②：用长度值指定径向渐变圆心的纵坐标值。可以为负值。
	top：设置顶部为径向渐变圆心的纵坐标值。
	center②：设置中间为径向渐变圆心的纵坐标值。
	bottom：设置底部为径向渐变圆心的纵坐标值。

<shape> 确定圆的类型
	circle：指定圆形的径向渐变
	ellipse：指定椭圆形的径向渐变。

<extent-keyword> circle | ellipse 都接受该值作为 size
	closest-side：指定径向渐变的半径长度为从圆心到离圆心最近的边
	closest-corner：指定径向渐变的半径长度为从圆心到离圆心最近的角
	farthest-side：指定径向渐变的半径长度为从圆心到离圆心最远的边
	farthest-corner：指定径向渐变的半径长度为从圆心到离圆心最远的角

<circle-size> circle 接受该值作为 size
	<length>：用长度值指定正圆径向渐变的半径长度。不允许负值。

<ellipse-size> ellipse 接受该值作为 size
	<length>：用长度值指定椭圆径向渐变的横向或纵向半径长度。不允许负值。
	<percentage>：用百分比指定椭圆径向渐变的横向或纵向半径长度。不允许负值。

<color-stop> 用于指定渐变的起止颜色：
	<color>：指定颜色。
	<length>：用长度值指定起止色位置。不允许负值
	<percentage>：用百分比指定起止色位置。不允许负值
```

**示例**

```css
radial-gradient(circle, #f00, #ff0, #080);
radial-gradient(circle at center, #f00, #ff0, #080);
radial-gradient(circle at 50%, #f00, #ff0, #080);
radial-gradient(circle farthest-corner, #f00, #ff0, #080);
```



## 3 CSS3 新增基本属性

### 3.1 布局相关属性

* box-sizing	定义盒子模型的尺寸解析方式

  >content-box(默认)	
  >border-box		

* resize	否允许用户缩放，调节元素尺寸大小

  >none： 不允许用户调整元素大小。 (默认)
  >both： 用户可以调节元素的宽度和高度。 
  >horizontal： 用户可以调节元素的宽度 	
  >vertical： 用户可以调节元素的高度。 	

* display	盒子是否以及如何显示

  > none： 隐藏对象。与visibility属性的hidden值不同，其不为被隐藏的对象保留其物理空间 
  > inline： 指定对象为内联元素。 
  > block： 指定对象为块元素。 
  > list-item： 指定对象为列表项目。 
  > inline-block： 指定对象为内联块元素。（CSS2） 
  > table： 指定对象作为块元素级的表格。类同于html标签<table>（CSS2） 
  > inline-table： 指定对象作为内联元素级的表格。类同于html标签<table>（CSS2） 
  > table-caption： 指定对象作为表格标题。类同于html标签<caption>（CSS2） 
  > table-cell： 指定对象作为表格单元格。类同于html标签<td>（CSS2） 
  > table-row： 指定对象作为表格行。类同于html标签<tr>（CSS2） 
  > table-row-group： 指定对象作为表格行组。类同于html标签<tbody>（CSS2） 
  > table-column： 指定对象作为表格列。类同于html标签<col>（CSS2） 
  > table-column-group： 指定对象作为表格列组显示。类同于html标签<colgroup>（CSS2） 
  > table-header-group： 指定对象作为表格标题组。类同于html标签<thead>（CSS2） 
  > table-footer-group： 指定对象作为表格脚注组。类同于html标签<tfoot>（CSS2）
  >
  > run-in： 根据上下文决定对象是内联对象还是块级对象。（CSS3） 
  >
  > box： 将对象作为弹性伸缩盒显示。（伸缩盒最老版本）（CSS3） 
  > inline-box： 将对象作为内联块级弹性伸缩盒显示。（伸缩盒最老版本）（CSS3） 
  > flexbox： 将对象作为弹性伸缩盒显示。（伸缩盒过渡版本）（CSS3） 
  > inline-flexbox： 将对象作为内联块级弹性伸缩盒显示。（伸缩盒过渡版本）（CSS3） 
  > flex： 将对象作为弹性伸缩盒显示。（伸缩盒最新版本）（CSS3） 
  > inline-flex： 将对象作为内联块级弹性伸缩盒显示。（伸缩盒最新版本）（CSS3） 

​		

### 3.2 外轮廓

- outline	给元素周围绘制一条轮廓线

  ```css
  <' outline-width '> || <' outline-style '> || <' outline-color '>
  ```

- outline-width  外廓线宽度

  > <length>： 用长度值来定义轮廓的厚度。不允许负值 
  > medium： 定义默认宽度的轮廓。 
  > thin： 定义比默认宽度细的轮廓。 
  > thick： 定义比默认宽度粗的轮廓。 	

- outline-style	外廓线风格

  > none： 无轮廓。与任何指定的 <' outline-width '> 值无关 
  > dotted： 点状轮廓。 
  > dashed： 虚线轮廓。 
  > solid： 实线轮廓 
  > double： 双线轮廓。两条单线与其间隔的和等于指定的 <' outline-width '> 值 
  > groove： 3D凹槽轮廓。 
  > ridge： 3D凸槽轮廓。 
  > inset： 3D凹边轮廓。 
  > outset： 3D凸边轮廓。 	

- outline-color	  外廓线颜色
- outline-offset  外廓线的偏移量



### 3.3 颜色

* opacity  检索或设置对象的不透明度。  对于尚不支持opacity属性的IE浏览器可以使用IE私有的滤镜属性来实现与opacity相同的效果 





## 4 CSS3新增边框和背景属性

### 4.1 边框圆角

* border-radius			

  > 设置或检索对象使用圆角边框。提供2个参数，2个参数以“/”分隔，每个参数允许设置1~4个参数值，第1个参数表示水平半径，第2个参数表示垂直半径，如第2个参数省略，则默认等于第1个参数 
  > 水平半径：如果提供全部四个参数值，将按上左(top-left)、上右(top-right)、下右(bottom-right)、下左(bottom-left)的顺序作用于四个角。 
  > 如果只提供一个，将用于全部的于四个角。 
  > 如果提供两个，第一个用于上左(top-left)、下右(bottom-right)，第二个用于上右(top-right)、下左(bottom-left)。 
  > 如果提供三个，第一个用于上左(top-left)，第二个用于上右(top-right)、下左(bottom-left)，第三个用于下右(bottom-right)。 
  >
  > 垂直半径也遵循以上4点。 

* border-top-left-radius		设置或检索对象的左上角圆角边框

* border-top-right-radius	设置或检索对象的右上角圆角边框

* border-bottom-right-radius	设置或检索对象的右下角圆角边框

* border-bottom-left-radius	   设置或检索对象的左下角圆角边框



### 4.2 盒子阴影

box-shadow			
	值: none | <shadow> [ , <shadow> ]*			
	<shadow> = inset? && <length>{2,4} && <color>?	
	阴影			
		none： 无阴影 
		<length>①： 第1个长度值用来设置对象的阴影水平偏移值。可以为负值 
		<length>②： 第2个长度值用来设置对象的阴影垂直偏移值。可以为负值 
		<length>③： 如果提供了第3个长度值则用来设置对象的阴影模糊值。不允许负值 
		<length>④： 如果提供了第4个长度值则用来设置对象的阴影外延值。可以为负值 
		<color>： 设置对象的阴影的颜色。 
		inset： 设置对象的阴影类型为内阴影。该值为空时，则对象的阴影类型为外阴影 
	可以设定多组效果，每组参数值以逗号分隔		