#页面组件

## 1 元素的尺寸/边框/背景

### 1.1 css尺寸相关属性

* height	高度
* min-height	最小高度
* max-height	最大高度
* width		宽度
* min-width	最小宽度
* max-width	最大宽度

### 1.2 css内边距

* padding	内边距
* padding-left	 左内边距
* padding-right 右内边距
* padding-top	  上内边距
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
* background-color	设置背景色，或设置为transparent（透明）
* background-image	背景图片 url  或者 none
* background-repeat	背景重复  repeat | repeat-x | repeat-y | no-repeat
* background-attachment	背景附件 scroll | fixed
* background-position		背景位置

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
* href	URL	规定区域的目标 URL。
* coords	规定区域的坐标。
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



## 5 表格

### 5.1 HTML列表标签

* `<table></table>`  
* `<caption></caption>`   定义表格标题
* `<thead></thead>`
* `<tfoot></tfoot>`
* `<tbody></tbody>`
* `<tr></tr>` 行
* `<th></th>` 表头单元格
* `<td></td>` 单元格



### 5.2 CSS列表属性

* table-layout 		表格布局方式		

  ```
  auto(默认)  布局将基于各单元格的内容，换言之，可能你给某个单元格定义宽度为100px，但结果可能并不是100px。表格在每一单元格读取计算之后才会显示出来，速度很慢 
  fixed       平布局是仅仅基于表格的宽度，表格边框的宽度，单元格间距，列的宽度，而和表格内容无关。也就是说，内容可能被裁切 
  
  ```

* border-collapse   	表格的行和单元格的边是合并还是独立

  ```
  separate (默认)  独立
  collapse  合并
  ```

* border-spacing   	当表格边框独立时，行和单元格的边框在横向和纵向上的间距

* caption-side caption	在table上面还是下面

  ```
  top	
  bottom
  ```

* empty-cells  		没有内容的单元格隐

* 藏还是显示

  ```
  show (默认)
  hide
  ```

### 5.3 合并单元格

给`<td>` 或者 `<th>` 设置属性 rowspan 和  colspan

```
rowspan  合并行
colspan  合并列
```



## 6 表单

### 6.1 表单相关标签

* `<form></from>`  定义一个 HTML 表单，用于用户输入。

  ```
  属性
  action
  method  
  	get   
  	post
  enctype
  	multipart/form-data(有文件表单时候，必须使用这个)
  	application/x-www-form-urlencoded
  target	
  ```

* `<input>` 定义一个输入控件

  ```
  属性
  name  必须有，否则数据无法传递
  type  text、password、radio、hidden、checkbox、submit、image、file、reset、button、submit、email、number、color等
  ```

* `<button></button>` 定义按钮

  ```
  属性
  type  submit、reset、submit
  name	
  ```

* `<select></select>` 定义选择列表（下拉列表）

  ```
  属性
  disabled  禁用
  name      必须有
  multiple  多选,默认会显示所有,名字要使用数组like[]
  size      显示几个下拉
  ```

* `<option></option>`   定义选择列表中的选项。

  ```
  属性
  value   提交的值，若没有，则提交内容
  selected  定义选中项
  disabled  选项禁用
  ```

* `<optgroup></optgroup>`   把相关的选项组合在一起

  ```
  属性
  disabled  规定禁用该选项组。
  label	为选项组规定描述。
  ```

* `<textarea></textarea>`

  ```
  属性
  cols  可见宽度
  rows  可见行数
  readonly  文本区只读
  name  必须有
  disabled  禁用	
  ```

* `<label>`  定义 fieldset 元素的标题。  

* `<fieldset></fidldset>`  定义围绕表单中元素的边框

* `<legend></legend>`  定义 fieldset 元素的标题。

### 6.2 表单组成控件

#### 文本输入框

```html
<input type="text" name="username">
<input type="text" name="username" placeholder="请输入用户名">
<input type="text" name="username" value="李大钊">
<input type="text" name="username" placeholder="请输入用户名" size="10" maxlength="15">
```

#### 密码框

```html
<input type="password" name="pwd">
<input type="password" name="pwd" placeholder="请输入密码">
<input type="password" name="pwd" placeholder="请输入密码" maxlength="12">
```

#### 单选按钮

```html
<input type="radio" name="sex" value="male" checked>男
<input type="radio" name="sex" value="female">男
```

#### 复选框

```html
<input type="checkbox" name="hobby" value="basketball"> 篮球
<input type="checkbox" name="hobby" value="football"> 足球
<input type="checkbox" name="hobby" value="ping-pong" checked> 乒乓球 
<input type="checkbox" name="hobby" value="baseball"> 棒球
```

#### 文件选择框

```html
<input type="file" name="pic">
<input type="file" name="pics" multiple>  <!--选择多个文件-->
```

#### 规定类型的文本输入框（HTML5新增）

```html
<!--邮箱-->
<input type="email" name="email" placeholder="请输入邮箱">

<!--url-->
<input type="url" name="url" placeholder="请输入网址">

<!--数字-->
<input type="number" name="num">
<input type="number" name="num" min='10' max='100' step='10'>

<!--搜索框-->
<input type="search" name="kw" placeholder="搜索">

<!--电话号码 同于text  但是用移动设备，会直接弹出数字键盘-->
<input type="tel" name="tel_num" placeholder="请输入电话号码">
```

#### 范围选择框(HTML5新增)

```html
<input type="range" name="range">
<input type="range" name="range" value="80">
<input type="range" name="range" value="80" max="100" min="0">
```

#### 颜色选择框(HTML5新增)

```html
<input type="color" name="color">
```

#### 时间日期选择框(HTML5新增)

```html
<input type="date" name="date">
<input type="month" name="month">
<input type="week" name="week">
<input type="time" name="time">
<input type="datetime" name="datetime">
<input type="datetime-local" name="datetime">
```

#### 下拉选项

```html
<select name="major">
	<option value="computer">计算机</option>
	<option value="archaeology">考古学</option>
	<option value="medicine" selected>医学</option>
	<option value="Architecture">建筑学</option>
	<option value="Biology">生物学</option>
</select>

<!--多选-->
<select name="major" multiple>
	<option value="computer">计算机</option>
	<option value="archaeology">考古学</option>
	<option value="medicine">医学</option>
	<option value="Architecture">建筑学</option>
	<option value="Biology">生物学</option>
</select>
```

#### 多行文本输入

```html
<textarea name="content"></textarea>
<textarea name="content" cols="30" rows="10"></textarea>
```

#### 按钮

```html
<!--提交按钮-->
<input type="submit" value="提交">
<button>提交</button>
<button type="submit">提交</button>

<!--重置按钮-->
<input type="reset" value="重置">
<button type="reset">重置</button>

<!--普通按钮-->
<input type="button" value="按钮">
<button type="button">按钮</button>
```

### 6.3 表单中其他标签

#### field/legend

```html
<form>
  <fieldset>
    <legend>health information</legend>
    height: <input type="text" />
    weight: <input type="text" />
  </fieldset>
</form>
```

#### datalist(新增)

```html
<input id="myCar" list="cars" />
<datalist id="cars">
  <option value="BMW">
  <option value="Ford">
  <option value="Volvo">
</datalist>
```



### 6.4 表单输入内容的智能验证(H5新增)

#### required 必填

给所有可输入的控件 添加 required属性，表示必填

####指定类型验证

Input:email 、input:url、input:number  会自动验证类型

#### pattern  正则 

```html
<input type="text" pattern="\w{4,6}">
<input type="text" pattern="\d{4,6}" title="必须是4~6位数字">
```

 

### 6.5 表单控件相关属性

* disabled   表示不可用 用于所有的表单控件

* enabled   表示可用  用于所有的表单控件

* readable   表示只读  用于可输入的表单控件

* autofocus  自动获取焦点 所有表单控件

* autocomplete  值on/off  用于可输入的控件  是否自动填充内容

* pattern  正则验证   可输入的控件

* required  必填



## 7 音频/视频 (HTML5新增)

### 7.1 HTML标签

* `<video></video>` 定义视频

  | 属性     | 值                 | 描述                                                         |
  | -------- | ------------------ | ------------------------------------------------------------ |
  | autoplay | autoplay           | 如果出现该属性，则视频在就绪后马上播放。                     |
  | controls | controls           | 如果出现该属性，则向用户显示控件，比如播放按钮。             |
  | height   | *pixels*           | 设置视频播放器的高度。                                       |
  | loop     | loop               | 如果出现该属性，则当媒介文件完成播放后再次开始播放。         |
  | muted    | muted              | 如果出现该属性，视频的音频输出为静音。                       |
  | poster   | *URL*              | 规定视频正在下载时显示的图像，直到用户点击播放按钮。         |
  | preload  | auto metadata none | 如果出现该属性，则视频在页面加载时进行加载，并预备播放。如果使用 "autoplay"，则忽略该属性。 |
  | src      | *URL*              | 要播放的视频的 URL。                                         |
  | width    | *pixels*           | 设置视频播放器的宽度。                                       |

* `<audio></audio>` 定义音频

  | 属性     | 值                 | 描述                                                        |
  | -------- | ------------------ | ----------------------------------------------------------- |
  | autoplay | autoplay           | 如果出现该属性，则音频在就绪后马上播放。                    |
  | controls | controls           | 如果出现该属性，则向用户显示音频控件（比如播放/暂停按钮）。 |
  | loop     | loop               | 如果出现该属性，则每当音频结束时重新开始播放。              |
  | muted    | muted              | 如果出现该属性，则音频输出为静音。                          |
  | preload  | auto metadata none | 规定当网页加载时，音频是否默认被加载以及如何被加载。        |
  | src      | *URL*              | 规定音频文件的 URL。                                        |

* `<source></source> `为媒体元素（比如 `<video>` 和 `<audio>`）定义媒体资源

  | 属性  | 值            | 描述                                       |
  | ----- | ------------- | ------------------------------------------ |
  | media | *media_query* | 规定媒体资源的类型，供浏览器决定是否下载。 |
  | src   | *URL*         | 规定媒体文件的 URL。                       |
  | type  | *MIME_type*   | 规定媒体资源的 MIME 类型。                 |



### 7.2 视频

#### 支持的视频类型

| 浏览器            | MP4                                                     | WebM | Ogg  |
| ----------------- | ------------------------------------------------------- | ---- | ---- |
| Internet Explorer | YES                                                     | NO   | NO   |
| Chrome            | YES                                                     | YES  | YES  |
| Firefox           | YES 从 Firefox 21 版本开始 Linux 系统从 Firefox 30 开始 | YES  | YES  |
| Safari            | YES                                                     | NO   | NO   |
| Opera             | YES 从 Opera 25 版本开始                                | YES  | YES  |

- MP4 = MPEG 4文件使用 H264 视频编解码器和AAC音频编解码器
- WebM = WebM 文件使用 VP8 视频编解码器和 Vorbis 音频编解码器
- Ogg = Ogg 文件使用 Theora 视频编解码器和 Vorbis音频编解码器

#### 视频格式的MIME类型

| 格式 | MIME-type  |
| ---- | ---------- |
| MP4  | video/mp4  |
| WebM | video/webm |
| Ogg  | video/ogg  |

MIME(Multipurpose Internet Mail Extensions)多用途互联网邮件扩展类型。是设定某种扩展名的文件用一种应用程序来打开的方式类型，当该扩展名文件被访问的时候，浏览器会自动使用指定应用程序来打开

### 7.3 音频

#### 支持的音频格式

| 浏览器            | MP3  | Wav  | Ogg  |
| ----------------- | ---- | ---- | ---- |
| Internet Explorer | YES  | NO   | NO   |
| Chrome            | YES  | YES  | YES  |
| Firefox           | YES  | YES  | YES  |
| Safari            | YES  | YES  | NO   |
| Opera             | YES  | YES  | YES  |

#### 音频格式MIME类型

| 格式 | MIME-type |
| ---- | --------- |
| MP3  | audio/mp3 |
| Wav  | audio/wav |
| Ogg  | audio/ogg |



​     







