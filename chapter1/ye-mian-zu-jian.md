#页面组件

## 1 元素的尺寸/边框/背景

### 1.1 css尺寸相关属性

* height		 高度
* min-height	最小高度
* max-height	最大高度
* width		宽度
* min-width	最小宽度
* max-width	最大宽度

### 1.2 css内边距

* padding	内边距
* padding-left	     左内边距
* padding-right     右内边距
* padding-top	      上内边距
* padding-bottom	 下内边距		

### 1.3 边框

* border		border-left|border-right|border-top|border-bottom

  ```css
  border: 边框宽度  边框样式  边框颜色
  ```

* border-style	    border-top-style | border-right-style | * border-bottom-style | border-left-style
  ```
  dotted   点线
  dashed  虚线
  solid      实线
  double 双实线
  groove 槽状线
  ridge     脊线
  inset      内嵌效果
  outset   外凸效果 
  ```
* border-color	 边框颜色   border-left-color | border-right-color | border-top-color | border-bottom-color
* border-width    边框宽度  border-left-width | border-right-width | border-top-width | border-bottom-width

### 1.4 背景

* background

  ```			css
  background:<背景颜色>|<背景图像>|<背景重复>|<背景附件>|<背景位置>
  
  例：background:red url('./123.png') no-repeat 100px 10px;
  ```

	 background-color	设置背景色，或设置为transparent（透明）

	 background-image	背景图片 url  或者 none

	 background-repeat	背景重复  repeat | repeat-x | repeat-y | no-repeat

	 background-attachment	背景附件 scroll | fixed

	 background-position		背景位置

  ```
  background-position: 水平方向 垂直方向
  background-position:left top;
  background-position:100px 100px;
  
  left | center | right (横向) 
  top | center | bottom (纵向) 
  或者使用百分比或者数值
  ```



## 2 超链接和锚点

### 2.1 超链接

```html
<a href='要跳转的地址'>超链接文字</a>
```

#### a标签的属性

* href -- 代表一个url链接源(就是链接到什么地方) 

  ```
  url除了是网页外,还可以是其它的文件(如文本文件,pdf文件等)。 
  url还可以是指向HTML文件中的一个位置。 
  url还可以是Email地址。 
  ```

* target -- 用来指出哪个窗口或框架应该被此链接打开 

  ```
  target=_blank： 将链接内容在新的浏览窗口中打开。 
  target=_self：  将链接的内容，显示在目前的窗口中。 
  target=_parent：将链接的内容，当成文件的上一个画面。 
  target=_top：这个参数可以解决新内容被旧框窗包围的困扰，使用这参数，会将整个画面重新显示成链接的画面内容。
  ```

* title -- 代表链接的附加提示信息 
* download  HTML5新添加属性 表示下载

#### 超链接范例

```html
网站链接：	 <a href="http://www.oldboy.cn">Python专家</a>
电子邮件链接： <a href="mailto:fuming@oldboy.com">写信给我</a>
电话 		    <a href="tel:10086">10086</a>
短信          <a href="sms:10086">发短息给我</a>
```

#### 路径

* 文档相对路径（例如 adver/contents.html）
* 绝对路径（例如 http://www.sohu.com/index.html）
* 站点根目录相对路径（例如 /support/app/customer.html，其中“/”表示根目录）

####  鼠标光标设置 （CSS属性）

- cursort

  ```
  text  文字选择器
  crosshair   十字架
  wait  等待
  help  帮助
  pointer 小手
  ```



### 2.2 锚点

```
用<a name=“”>定义，例如：<a name=“here1”>第一部分</a>，
使用<a href=“#here1”>跳转到第一部分</a>超链接就可以定位到网页中的“第一部分”这个位置。
```

```
锚点的跳转
使用#  <a href="#锚点名">跳转</a>
跳转到指定页面指定锚点  http://www.lampuser.com/index.html#section2
```

### 2.3 URL

URL(Uniform Resoure Locator)，统一资源定位符是对可以从互联网上得到的资源的位置和访问方法的一种简洁的表示，是互联网上标准资源的地址。互联网上的每个文件都有一个唯一的URL，它包含的信息指出文件的位置以及浏览器应该怎么处理它。

#### URL的组成

```
http://www.fuming.com/product/news/add?name=xiaolili&age=10#section1
```

- protocol 协议，常用的协议是http
- hostname 主机地址，可以是域名，也可以是IP地址
- port 端口 http协议默认端口是：80端口，如果不写默认就是:80端口
- path 路径 网络资源在服务器中的指定路径
- query 查询字符串 如果需要从服务器那里查询内容，在这里编辑
- hash  锚点部分，指向页面中的某个位置



## 3 图片

### 3.1 img 标签

```html
<img src="图片地址" title="" alt="">
```

#### 属性

* alt -- 代表图像的替代文字 
* src -- 代表一个图像源(就是图像的位置)
* title 提示信息
* border – 代表图片边框的宽度 
* height -- 代表一个图像的高度 
* width -- 代表一个图像的宽度 
* usemap 将图像定义为客户器端图像映射。

#### 常见图片格式

* GIF -- 最多支持256色,支持透明,支持多帧动画显示效果.
* JPEG -- 支持多种颜色,可以有很高的压缩比,使用了有损压缩,不支持透明,不支持动画效果.
* PNG -- 是一种新的图片技术,可以表现品质比较高的图片,使用了无损压缩,支持透明,不支持动画. 



### 3.2 图像映射

```html
<img src="planets.gif" alt="Planets" usemap="#planetmap" />

<map name="planetmap">
  <area href="sun.htm" shape="rect" coords="0,0,110,260">Sun</a>
  <area href="mercur.htm" shape="circle" coords="129,161,10">Mercury</a>
  <area href="venus.htm" shape="circle" coords="180,139,14">Venus</a>
</map>
```

#### map标签

```
<map> 标签用于客户端图像映射。图像映射指带有可点击区域的一幅图像。
<img>中的 usemap 属性可引用 <map> 中的 id 或 name 属性（取决于浏览器），所以我们应同时向 <map> 添加 id 和 name 属性。
area 元素永远嵌套在 map 元素内部。area 元素可定义图像映射中的区域。
```

### area标签

* alt  规定区域的替代文本。如果使用 href 属性，则该属性是必需的。

   href	URL	规定区域的目标 URL。

    coords	规定区域的坐标。

* shape 规定区域的形状

  ```
  rect  矩形
  circle 圆形
  poly  多边形
  ```

* target -- 用来指出哪个窗口或框架应该被此链接打开 



## 4 列表

### 4.1 HTML列表标签

* `<ul></ul>`	 代表HTML无序列表 ，里面每一列表项使用`<li>`标签定义

* `<ol></ol>`	代表HTML有序列表 ，里面每一列表项使用<li>标签定义

  ```
  属性
  start 规定有序列表的起始值。
  type   规定在列表中使用的标记类型。(1 a A  i  I)
  reversed  H5新添加 降序
  ```

* `<li></li>` 代表HTML列表项目，每个列表项使用一对`<li></li>`标记

* `<dl></dl>`  定义了定义列表（definition list）

* `<dt></dt>` 标签定义了定义列表中的项目（即术语部分）

* `<dd></dd>` 在定义列表中定义条目的定义部分。

### 4.2 CSS列表属性

* list-style-type

  ```
  disc         实心点
  circle       圆圈
  square       小方框
  decimal      数字
  lower-roman  小写罗马字
  upper-roman  大写罗马字
  lower-alpha  小写字母
  upper-alpha  大写字母		
  ```

* list-style-position	 位置

  ```
  inside   标示在li里面
  outside  标示在li外面
  ```

* list-style-image	 使用图片 url(./123.gif)

