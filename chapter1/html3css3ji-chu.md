# HTML5/CSS3基础

## 1. HTML

### 1.1 什么是HTML

* HTML是用来制作网页的标记语言 
* HTML是Hypertext Markup Language的英文缩写,即超文本标记语言 
* HTML语言是一种标记语言,不需要编译,直接由浏览器执行 
* HTML文件是一个文本文件,包含了一些HTML元素,标签等
* HTML文件必须使用.html或.htm为文件名后缀 
* HTML是大小写不敏感的,HTML与html是一样的 
* HTML是由W3C的维护的 
* HTML 是通向 WEB 技术世界的钥匙。

### 1.2 发展历史

* HTML是从2.0版本开始的，实际上没有1.0的官方规范,在1993年6月作为互联网工程工作小组（IETF）工作草案发布（并非标准）
  HTML 2.0——1995年11月作为RFC 1866发布，在RFC 2854于2000年6月发布之后被宣布已经过时
* HTML 3.2——1997年1月14日，W3C推荐标准
* HTML 4.0——1997年12月18日，W3C推荐标准
* HTML 4.01（微小改进）——1999年12月24日，W3C推荐标准
* HTML 5——2014年10月28日，W3C推荐标准

### 1.3 HTML5的由来

* HTML5草案的前身名为 Web Applications 1.0，于2004年被WHATWG提出，于2007年被W3C接纳，并成立了新的 HTML 工作团队。
* HTML 5 的第一份正式草案已于2008年1月22日公布。HTML5 仍处于完善之中。然而，大部分现代浏览器已经具备了某些 HTML5 支持。
* 2012年12月17日，万维网联盟（W3C）正式宣布凝结了大量网络工作者心血的HTML5规范已经正式定稿。根据W3C的发言稿称：“HTML5是开放的Web网络平台的奠基石。”
* 2013年5月6日， HTML 5.1正式草案公布。该规范定义了第五次重大版本，第一次要修订万维网的核心语言：超文本标记语言（HTML）。在这个版本中，新功能不断推出，以帮助Web应用程序的作者，努力提高新元素互操作性。
* 2014年10月29日，万维网联盟宣布，经过接近8年的艰苦努力，该标准规范终于制定完成。

### 1.4 HTML5的优点

* 1、提高可用性和改进用户的友好体验；
* 2、有几个新的标签，这将有助于开发人员定义重要的内容；
* 3、可以给站点带来更多的多媒体元素\(视频和音频\)；
* 4、可以很好的替代FLASH和Silverlight；
* 5、当涉及到网站的抓取和索引的时候，对于SEO很友好；
* 6、将被大量应用于移动应用程序和游戏；
* 7、可移植性好。

### 1.5 HTML5的兼容性

* Internet Explorer 9 以及 以上版本
* chrome、Safari、opera、Firefox和各种以wekkit为内核的国产浏览器

### 附：相关组织

#### IETF\(The Internet Engineering Task Force\)

国际互联网工程任务组（The Internet Engineering Task Force，简称 IETF）  
互联网工程任务组，成立于1985年底，是全球互联网最具权威的技术标准化组织，主要任务是负责互联网相关技术规范的研发和制定，当前绝大多数国际互联网技术标准出自IETF。

#### W3C\(World Wide Web Consortium\)

万维网联盟\(World Wide Web Consortium\)  
万维网联盟创建于1994年，是Web技术领域最具权威和影响力的国际中立性技术标准机构。到目前为止，W3C已发布了200多项影响深远的Web技术标准及实施指南，如广为业界采用的超文本标记语言（标准通用标记语言下的一个应用）、可扩展标记语言（标准通用标记语言下的一个子集）以及帮助残障人士有效获得Web内容的信息无障碍指南（WCAG）等，有效促进了Web技术的互相兼容，对互联网技术的发展和应用起到了基础性和根本性的支撑作用。

### WHATWG\(Web Hypertext Application Technology Working Group\)

网页超文本应用技术工作小组是一个以推动网络HTML 5 标准为目的而成立的组织。  
在2004年，由Opera、Mozilla基金会和苹果这些浏览器厂商组成。

## 2 HTML基本语法

### 2.1 HTML标签

* 标签是HTML中最基本单位,也是最重要组成部分
* 通常要用两个角括号括起来:`<`和`>`
* 标签都是闭合的（两种形式：成对与不成对） 
* 双标签（成对）: `<标签名>内容</标签名>` 如：`<table></table>` 即分起始和结束
* 单标签（不成对）: `<标签名 />`;  如： `<br/>`、`<hr/>`
* 标签是大小写无关的,`<body>`;跟`<BODY>`表示意思是一样的，标准推荐使用小写，这样符合XHTML标准。
* 对于HTML标签来讲，最重要的是语义

### 2.2 HTML标签属性

* HTML属性一般都出现在HTML的开始标签中, 是HTML标签的一部分。
* 标签可以有属性,它包含了额外的信息.属性的值一定要在双引号中。
* 标签可以拥有多个属性。
* 属性由属性名和值成对出现。
* 语法格式如下：
  ```html
  <标签名 属性名1="属性值" 属性名2="属性值" ... 属性名N="属性值">
    <!– 输出内容…  -->
  </标签名>
  ```

### 2.3 HTML代码格式

任何回车或空格在源代码中都是不起作用，  
所以在编写HTML代码时，都可以使用回车或者空格进行代码排版，  
这样可以使代码清晰，也便于团队合作。必须保持严格的缩进规则，以`Tab`键为准。

### 2.4 HTML 注释

```html
<!-- 注释内容 -->
<!--
    这里全是注释
    都是注释
-->
```

### 2.5 HTML 实体 \(特殊字符\)

|  | 描述 | 实体名称 | 实体编号 |
| :--- | :--- | :--- | :--- |
|  | 空格 |  | &\#160; |
| &lt; | 小于号 | &lt; | &\#60; |
| &gt; | 大于号 | &gt; | &\#62; |
| & | 和号 | & | &\#38; |
| " | 引号 | " | &\#34; |
| ' | 撇号 | ' \(IE不支持\) | &\#39; |
| ￠ | 分（cent） | ¢ | &\#162; |
| £ | 镑（pound） | £ | &\#163; |
| ¥ | 元（yen） | ¥ | &\#165; |
| € | 欧元（euro） | € | &\#8364; |
| § | 小节 | § | &\#167; |
| © | 版权（copyright） | © | &\#169; |
| ® | 注册商标 | ® | &\#174; |
| ™ | 商标 | ™ | &\#8482; |
| × | 乘号 | × | &\#215; |
| ÷ | 除号 | ÷ | &\#247; |

## 3 HTML常用标签

### 3.1 文档声明

你可使用此声明在 Internet Explorer 6 及以后版本中切换为严格的标准兼容模式。

```html
<!DOCTYPE HTML PUBLIC "-//W3C//DTD HTML 4.01//EN" "http://www.w3.org/TR/html4/strict.dtd">

<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">

<!DOCTYPE html>
```

### 3.2 HTML主体结构标签

* `<html></html>` 此元素可告知浏览器其自身是一个 HTML 文档。
* `<head></head>` 用于定义文档的头部，它是所有头部元素的容器。`<head>` 中的元素可以引用脚本、指示浏览器在哪里找到样式表、提供元信息等等。
* `<body></doby>` 定义文档的主体    

### 3.3 HEAD头部标签

* `<title></title>`  定义文档标题
* `<base />`  标签为页面上的所有链接规定默认地址或默认目标
* `<meta />`  元素可提供有关页面的元信息（meta-information），比如针对搜索引擎和更新频度的描述和关键词。`<meta>` 标签永远位于 head 元素内部。
  ```html
  <meta charset="utf-8">
  ```
* `<link></link>` 标签定义文档与外部资源的关系。

  ```html
  <link rel="stylesheet" type="text/css"  href="style.css"></link>
  <link rel="shortcut icon" type="images/x-icon" href="http://www.baidu.com/favicon.ico">
  ```

* `<style></style>`  签用于为 HTML 文档定义样式信息。

* `<script></script>`  标签用于定义客户端脚本，比如 JavaScript。script 元素既可以包含脚本语句，也可以通过 src 属性指向外部脚本文件。

  ```html
  <script type="text/javascript" src="script.js"></script>
  <script>
    alert('OK')
  </script>
  ```

### 3.4 meta元信息

* content  定义与 http-equiv 或 name 属性相关的元信息
* name 把content属性关联到一个名称

  ```
  author

  description

  keywords

  generator

  revised

  robots

  others
  ```

* http-equiv  把 content 属性关联到 HTTP 头部。

  ```
  content-type
  expires
  refresh
  set-cookie
  ```

* charset  字符集编码

```html
编码字符集
<meta charset="utf-8">  HTML5 支持 HTML5向下兼容
<meta http-equiv="content-type" content="text/html;charset=utf-8" /> HTML 4支持

网页关键字：
<meta name="keywords" content="8-12个以英文逗号隔开的单词/词语">

网页描述信息
<meta name="description" content="80字以内的一段话，与网站内容相关">

所有搜索引擎，抓取这个页面、爬行链接、禁止快照：  
<meta name="robots" content="index,follow,noarchive">
  all：文件将被检索，且页面上的链接可以被查询；
  none：文件将不被检索，且页面上的链接不可以被查询；
  index：文件将被检索；
  follow：页面上的链接可以被查询；
  noindex：文件将不被检索，但页面上的链接可以被查询；
  nofollow：文件将被检索，但页面上的链接不可以被查询；
  noarchive：文件将被检索，但禁止保存快照；

网页作者：
<meta name="author" content="obama">

网页网页生成工具 
<meta name="generator" content="Sublime Text3">

定义页面最新版本 
<meta name="revised" content="David, 2008/8/8/" />

网页版权信息：
<meta name="copyright" content="2009-2014©版权所有">

网页刷新信息：
<meta http-equiv="refresh" content="10;url=http://www.baidu.com">  10秒后跳转到百度页面
```

### 3.5 格式排版标签

* `<br/>`    换行标签，完成文字的紧凑显示。可以使用连续多个`<br/>`标签来换行

* `<hr/>`    水平分割线标签，用于段落与段落之间的分割

* `<p></p>`段落标签,里面可以加入文字,列表,表格等，可以&lt;p&gt;&lt;/p&gt;或&lt;p /&gt;使用

* `<pre></pre>`按原文显示标签，可以把原文件中的空格,回车,换行,tab键表现出来

* `<hn></hn>`    标题字标签，n为1-6，定义六级标题，而且会自动换行插入一个空行

* `<div></div>` 没有任何语义的标签

## 4 CSS基础语法

### 4.1 使用方法

* 写在标签内的style属性中	
```html
<p style="color:red;"</p>
```
* 写在&lt;style&gt; 元素中	
```html	
<style>
  p{color:red}
</style>

* 通过外部引入			
```html
<link rel="stylesheet" type="text/css" href="./style.css">
```

### 4.2 CSS格式组成

* 选择器	 负责圈定范围，要修改的元素集合
* 声明	由属性名和属性值组成，中间用冒号连接(属性名:属性值)，用于设定具体样式
* CSS由选择器和一或多个声明组成，多个声明之间用分号
```css
  选择器{
    属性名:属性值;
    属性名:属性值;
  }
```

### 4.3 CSS注释
```css
/*注释内容*/
```

### 4.4 CSS长度单位(基本)





