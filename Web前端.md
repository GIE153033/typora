# Web前端开发

## HTML

Hypertext markup language

（超文本标记语言）
结构层：搭建结构，放置部件，描述语义

### html的语义化

​		语义化是指根据内容的结构化（内容语义化），选择合适的标签（代码语义化）。通俗来讲就是用正确的标签做正确的事情。

语义化的优点如下：

* 对机器友好，带有语义的文字表现力丰富，更适合搜索引擎的爬虫爬取有效信息，有利于SEO。除此之外，语义类还支持读屏软件，根据文章可以自动生成目录；
* 对机器友好，带有语义的文字表现力丰富，更适合搜索引擎的爬虫爬取有效信息，有利于SEO。除此之外，语义类还支持读屏软件，根据文章可以自动生成目录；

 常见的语义化标签：header、nav、section、main、article、aside、footer。



### 元素列表

[<u>*各类标签的语义以火狐的MDN文档为准*</u>](https://developer.mozilla.org/zh-CN/docs/Web/HTML/Element)

#### 块级元素

块级元素（区块标签）在浏览器显示时，通常会以新行来开始（和结束）。

实例: *<u><div></u>*,<h1>, <p>, <ul>, <table>

##### div

- （division）用来将相关内容组合到一起，以和其他内容分割，业内一般称‘盒子’

##### h1

```html
<h1>这是标题 1</h1>
<h2>这是标题 2</h2>
<h3>这是标题 3</h3>
<h4>这是标题 4</h4>
<h5>这是标题 5</h5>
<h6>这是标题 6</h6>
```

##### ul、ol

```html
<ol>				<!--有序列表-->
   <li>Coffee</li>
   <li>Tea</li>
   <li>Milk</li>
</ol>

<ul>				<!--无序列表-->
   <li>Coffee</li>
   <li>Tea</li>
   <li>Milk</li>
</ul>
```

- <li>标签定义列表项目
- 里面只可以包含li标签
- li标签作为容器可以在内部放任何标签

  - 标签默认首行缩进

##### dl

```html
<dl>	<!--定义列表-->
   <dt>计算机</dt>		<!--定义列表中的项目-->
   <dd>用来计算的仪器 ... ...</dd>		<!--描述列表中的项目-->
   <dt>显示器</dt>
   <dd>以视觉方式显示信息的装置 ... ...</dd>
</dl>
```

- 用于解释说明
- 子级为dt（数据项）和dd（数据定义）

  - 1个dt后面可以跟多个dd

##### img

```html
<img src="/i/eg_tulip.jpg"  alt="上海鲜花港 - 郁金香" />
```

- scr（路径）

  - 相对路径/绝对路径
    - 路径中不可有中文
    - 相对路径中若需要回退层级，需要使用../
    - 工作中绝对路径一般只用于超链接

  - 自H5之后可以在末尾不写/

- alt

  - 对图片的文本描述，当图片无法加载时显示
  - 有助于搜索引擎优化

- 宽度width，高度height

  - 不用写单位，默认单位像素
  - 若只写一个属性，则按原比例缩放

- imges文件需随同网页文件一起移动，否则无法显示

- img用于插入有意义的图片，装饰性图片以背景图（bgc）插入

##### section

- 文档的区域，一般来说会有包含一个标题

article

- 文档的核心文章内容

##### aside

- 文档的非必要相关内容，比如广告、侧边栏等

##### nav

- 导航条

##### header

- 页头

##### main

- 网页核心部分![新浪网手机版标签使用](学习笔记img\新浪网手机版标签使用.jpg)


##### footer

- 页脚

##### input

- 文本框

#### 内联元素

文本标签/内联元素在显示时通常不会以新行开始。

实例: *<u><span></u>*,<b>, <td>, <a>, <img>

##### span

- 英文直译为‘跨度’，无任何样式

##### a

a超级链接的伪类

```css
<a href="baidu.com" target="_blank" title="点击打开百度“>百度</a>
a:link{}	/*没有访问过的链接样式*/
a:visited{}	/*已经访问过的链接样式*/
a:hover{}	/*鼠标触碰时的链接样式*/
a:active{}	/*鼠标按下未抬起时的样式*/
```



| **属性**                                                     | **值**                                                       | **描述**                                                     |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ |
| [download](https://www.w3school.com.cn/tags/att_a_download.asp) | *filename*                                                   | 规定被下载的超链接目标。                                     |
| [href](https://www.w3school.com.cn/tags/att_a_href.asp)      | *URL*                                                        | 规定链接指向的页面的 URL。                                   |
| [hreflang](https://www.w3school.com.cn/tags/att_a_hreflang.asp) | *language_code*                                              | 规定被链接文档的语言。                                       |
| [media](https://www.w3school.com.cn/tags/att_a_media.asp)    | *media_query*                                                | 规定被链接文档是为何种媒介/设备优化的。                      |
| [rel](https://www.w3school.com.cn/tags/att_a_rel.asp)        | *text*                                                       | 规定当前文档与被链接文档之间的关系。                         |
| [target](https://www.w3school.com.cn/tags/att_a_target.asp)  | \_blank <br />\_parent <br />\_self<br />\_top <br />*framename* | 新窗口打开<br />默认。在相同的框架中打开被链接文档。<br />在父框架集中打开被链接文档。<br />在整个窗口中打开被链接文档。<br />在指定的框架中打开被链接文档。<br /> |
| [type](https://www.w3school.com.cn/tags/att_a_type.asp)      | *MIME type*                                                  | 规定被链接文档的的 MIME 类型。                               |

- href超文本引用
- target

  - H5之后取消下划线
- 增加title可显示悬浮文本

- 若想点击图片后跳转链接，可以将img标签包含在a标签内

##### b

- 加粗

##### u

- 下划线

##### i

- 斜体

##### strong

- 加粗，表示特别重要的文字


##### em

- 斜体，代表强调文字

##### pre

- 保留代码样式，可以阻止Html的空白折叠现象

##### code

- 表示代码程序，一般结合<pre>标签使用

#### 元素转换

```css
div{
	display:inline;	/*可将块级元素转为行内元素*/
    /*通常用于导航条及按钮形式的超级链接a元素的转换*/
}
em{
	display:block;	/*可将行内元素转为块级元素*/
}
em{
    display:inline-block;	/*可将元素转为行内块元素*/
    /*像img、表单元素天生就是行内块元素，既能并排，又能设置宽高*/
    /*只有小的地方可以用行内块，大的布局严禁使用*/
}
```



#### 转义字符/字符实体

##### \&lt;	&lt;

​		less than

##### \&gt;	&gt;

​		greater than

##### \&nbsp;	&nbsp;

​		none-breaking space

##### \&copy;	&copy;

​		copyright

#### 浏览器兼容

##### [相关网站](html5test.com)

- 为当前使用的浏览器打分

##### [caniuse.com](caniuse.com)

- 查询某个技术的兼容程度

##### [MDN](https://developer.mozilla.org/zh-CN/)

##### [百度流量研究院](https://tongji.baidu.com/research/app)

- 统计各个浏览器的使用份额

## CSS

Cascading style sheets
层叠样式表
样式层：美化页面，实现布局

### 外链样式表

```html
<link href="styles/style.css" rel="stylesheet">
```

### 选择器的分类

#### CSS2传统选择器

##### 标签选择器

又称元素选择器，类型选择器，通常用于标签的初始化

```css
/*通配符，去除所有内外边距*/
* {
    padding: 0;
    margin: 0;
}
/*去除标签圆点*/
ul {
    list-style: none;
}
/*去除链接下划线*/
a {
    text-decoration: none;
}
/*将网页背景调为白色*/
body {
    background-color: #fff;
}
/*去掉em斜体*/
em {
    font-style: normal;
}
```

##### id选择器

* css代码


```css
#header{}
```

* html代码


```html
<div id="header"></div>
```

* id是标签的唯一标识，不可重复

* 只能由字母、数字、短横、下划线构成，且不能以数字开头，字母区分大小写（一般为小写）

- 缺点

  - 实际网页开发中使用较少
  - 较为“笨拙”，一次只能选择一个标签，不灵活
  - JavaScript为操作标签，也会经常给标签添加id，为标签增加大量id势必会造成混乱

##### 类选择器

* css代码


```css
.spec{}
.nav{}
```

* html代码


```css
<div class="spec nav">我有两个类名</div>
```

- 同一标签可以同时属于多个类，类名用空格隔开

- 只能由字母、数字、短横、下划线构成，且不能以数字开头，字母区分大小写（一般为小写）


###### ***原子类***

- 将所有的常用属性都设置为单独的类，用的时候很方便

```css
.fs-12 {
    font-size: 12px;
}
.fs-14 {
    font-size: 14px;
}
.fs-16 {
    font-size: 16px;
}
.fs-18 {
    font-size: 18px;
}
.fs-20 {
    font-size: 20px;
}
```



##### 复合选择器

* 复合选择器可以任意搭配

###### 后代选择器

```css
.box p{}	/*选择的所有后代，包括子代孙代*/
```

- 由两个选择器连接构成，中间需加空格

- 只要是后代都可以选择，并不单指儿子，也包括孙子

- 多层级后代

  ```css
  <div class="box">
  	<p>
  		<ul>
  			<li>文字</li>
  		</ul>
  	</p>
  </div>
  ```

###### 交集选择器

由两个选择器直接连接构成，第一选择器必须为标签选择器，第二选择器为类选择器或id选择器

```css
p.box{}			/*类名为box的p标签*/
div#content		/*id为content的div标签*/
```

###### 并集选择器（分组选择器）

```css
.box,#content{}	/*同时选择类名为box和id为content的元素*/
```

#### CSS3新增选择器

##### 元素关系选择器

###### 子选择器

```css
.box>p {}	/*选择类名为box的所有子元素p*/
```

###### 相邻兄弟选择器

```css
h3+p {}		/*只能选择同级相邻的选择器*/
```

###### 序号选择器

```css
ul li:first-child{}		/*表示ul中的第一个li标签*/
li:last-child{}			/*表示最后一个li标签*/
li:nth-child(3n+2){}	/*表示第3n+2个li标签*/
li:nth-child(odd){}		/*奇数行li标签*/
li:nth-child(even){}	/*偶数行li标签*/
/*若连续相同子元素内掺杂其他元素，则后续相同的元素无法继续进行*/

/*以下工作不用*/
li:nth-last-child(3){}	/*倒数第(3)个子元素*/
li:nth-of-tybe(3){}		/*第三个某类型子元素*/
li:nth-last-of-child(3){} /*倒数第(3)个某类型子元素*/
```

###### 属性选择器

```css
img[alt]		/*选择有alt属性的img标签*/
img[alt="aa"]	/*选择alt属性是aa的img标签*/
img[alt^="aa"]	/*选择alt属性开头是aa的img标签*/

/*以下工作不用*/
img[alt$="aa"]	/*选择alt属性以aa结尾的img标签*/
img[alt|="aa"]	/*选择alt属性中含有aa的img标签*/
img[alt~="aa"]	/*选择alt属性中有空格隔开的aa的img标签*/
img[alt^="aa"]	/*选择alt属性以aa-开头的img标签*/
```

### 属性分类

#### background

定义背景样式

```css
.div{
    background:url(images/aaa.jpg) no-repeat 10px 5px;
    background-color:#575757;		/*背景颜色*/
    background-repeat:repeat;		/*平铺*/
    background-repeat:no-repeat;	/*不平铺*/
    background-repeat:repeat-x;		/*水平平铺*/
   	background-repeat:repeat-y;		/*垂直平铺*/
    background-attachment:fixed;	/*背景固定*/
    background-image:url();			/*背景图片*/
    background-size: cover;			/*背景图覆盖*/
    background-image:-webkit-linear-gtadient(0deg,red 20%,blue)
        /*背景渐变*/
}
```



| 私有前缀 | 内核                   |
| -------- | ---------------------- |
| -webkit- | Chrome内核、Safari内核 |
| -ms-     | 微软IE                 |
| -moz-    | 火狐                   |
| -o-      | 欧朋                   |
| 无前缀   | 方向从下向上           |

------

| 背景定位            | x方向  | y方向  | 对齐位置           |
| ------------------- | ------ | ------ | ------------------ |
| background-position | left   | top    | 左上               |
|                     | center | center | 正中               |
|                     | right  | bottom | 右下               |
|                     | 15px   | 0      | 右移15px           |
|                     | 0      | 20px   | 下移20px           |
|                     | -10px  | -10px  | 向左，向上各移10px |

#### font

定义字体样式

```css
.div{
	font-weight:bold;		/*加粗*/
	font-weight:normal;		/*正常*/
	font-style:italic;		/*斜体*/
	font-style:normal;		/*正常*/
	font-size:16px;			/*字号16px*/
	font-family:'宋体';	   /*宋体*/
    font:bold italic 20px/30px '楷体';
    /*字体加粗，斜体，字号20px，行高30px，楷体*/
    /*	行高前必须加'/'	*/
}
```

#### color

定义文本颜色

```css
.div{
	color:red;				/*颜色红色*/
	color:rgb(25,16,75);	 /*rgb颜色*/
    color:rgb(25,16,75,0.5);  /*颜色透明度0.5*/
	color:#4f768c;			 /*16进制*/
	color:#fff;				 /*等效于#ffffff*/
}
```

#### text

定义文本样式

```css
.div{
	text:indent 2em;				/*首行缩进2字符*/
	text-align:left;				/*文本左对齐*/
	text-align:center;				/*文本居中对齐*/
	text-align:right;				/*文本右对齐*/
	text-decoration:underline;		 /*下划线*/
	text-decoration:line-through;	 /*删除线*/
	text-decoration:overline;		 /*上划线*/
	text-decoration:none;			 /*去除所有样式*/
    letter-spacing:2px；				/*单词间距*/
    word-spacing:2em；				/*文本间距*/
}
```

#### `ling-height:`

- 文字行高设置为盒子高则默认上下居中

#### `width:`

- 若不写宽度，则默认撑满父级盒子
- 大框架都要写宽高，浮动元素默认撑满可以不写

#### `height:`

#### border

* 同一元素两条边框相交处为斜线,可用此特性做倒三角图标

```css
.div{
	border-width:2px;	/*边框宽度2px*/
	border-style:solid;
    border-top-style:dashed;
    /*solid实线、dashed虚线、dotted点线、double双实线*/
    border-color:#000;	/*边框颜色黑色*/
    border-top-color:#000;
}
```

#### `border-radius:`

```css
border-radius:20px 30px 40px 50px;	/*左上、右上、右下、左下*/
border-top-left-radius:20px;
border-top-right-radius:30px;
border-bottom-right-radius:40px;
border-bottom-left-radius:50px;
border-radius:50%;	/*正圆*/
```



#### padding

* 加padding时需要同时调整内容宽度
* padding在元素的边框以内，内容之外，padding不影响元素的背景图片

```css
.div{
	padding:10px 20px 50px 30px;	/*上10px，右20px，下50px，左30px*/
	padding:10px 20px;	/*上下10px，左右20px*/
	padding:10px;	/*上下左右各10px*/
    padding-top:5px;	/*上内边距5px*/
}
```

#### margin

- margin元素在边框之外，不显示元素背景

- 盒子水平居中，margin:0 auto;
- 两相邻同级元素的外边框重叠
- 子级外边距会传给父元素

#### float

- 添加了float属性的盒子会有“贴靠”特性，从而实现元素并排
- 若要设置浮动，同级的亲兄弟都要设置浮动，这是不可撼动的CSS硬性规则
- 父盒子必须要设置高度，或者添加ovh属性
- 浮动元素未设置宽高时，元素宽高会被内容撑满（橡皮筋法则）

#### `z-index:`

- 设置堆叠顺序

#### animation

设置动画效果

#### transition

设置动画效果

### <u>*盒模型*</u>

* 初始化元素需要先清楚默认样式（常用有通配符*、a标签下划线、ul列表圆点）
* 盒子宽度=width内容宽度+padding两侧内边距宽度+border两侧边框宽度+margin两侧外边距宽度

```
.div{
	width:400px;			/*宽400px*/
	height:300px;			/*高300px*/
	border:1px solid #000;	 /*边框宽1px，实线，黑色*/
	padding:5px 10px;		 /*内边框上下5px，左右10px*/
	margin:20px 30px 10px;	 /*外边框上20px，左右30px，下10px*/
	
}
```



### 特性

可以通过谷歌内核浏览器的检查功能查看层叠、继承情况

#### 层叠性

多个选择器可以同时作用于同一个标签，效果叠加，若有冲突，有严密的计算方法

* 距子元素相同距离：id=100，类名=10，标签=1，!important为同级最高；相加比大小

* 距子元素不同距离，距离近的权重高

#### 继承性

- 文本相关的属性普遍具有继承性

	- color
	- font-
	- list-
	- text-
	- line-

### 相对定位/绝对定位

#### 相对定位（形影分离）

```css
.div{
	position:relative;
	top:50px;
	left:50px;
    /*相对于原来的位置下移50px，右移50px*/
}
```



#### 绝对定位（移形换影）

- 绝对定位后该元素必须写宽度，否则不会自动撑满
- 绝对定位的元素不能使用margin:0 atuo;进行居中
- 绝对定位垂直水平居中
  1. `position:absolute;	top:50%;left:50%;margin-left:(-1/2宽度px)；margin-top:(-1/2高度px)；`
  2. `display:flex;justify-content:center;align-items:center;`


#### 子绝父相

- 子元素若要设置绝对定位，父元素必须设置相对定位

### *<u>标准文档流和脱标</u>*

- 脱标手段

	- 浮动（float:）
	- 绝对定位（position:absolute）
	- 固定定位

- 脱标之后都可以设置宽高，不在区分块级元素、行内元素和行内块元素，未写宽度时会收缩
- 相对定位不脱标

### BFC

BFC（Box Formatting Context，块级格式化上下文）是独立渲染容器，是独立的区域，它内部的元素不影响区域外的其他元素，也不会被区域外的其他元素影响

#### 形成方式

- 设置（溢出隐藏ovh）样式
`overflow:hidden;`
- 脱标
- display的值是inline-block或者是flex

#### 存在的意义

- <u>让内部浮动的元素可以撑出高</u>
- 实现左固定宽度，右自动撑满的布局

	- 为右侧盒子设置ovh

- 阻止margin塌陷

### 清除浮动

清除浮动对后面正常处于标准文档流中的元素带来的影响

- BFC

	- 父元素添加ovh

- clear属性

  - `clear:left`不允许左侧有浮动
  - `clear:right`不允许右侧有浮动
  - `clear:both`不允许两侧有浮动(给后方元素加)

- ::伪元素

  ```
  .clearfix::after{
  	content:'';
  	clear:both;
  	display:block;
  }
  ```

  - after内必须有content属性
  - after默认为行内元素

- 隔墙

	- 在相邻元素间插入公共类名且带有高度的块元素

### CSS精灵(sprites)

- 精灵图都是背景图（bgc）

- 用背景位置（bgp）来定位需要图片的位置

	`background-position: -右px -下px;`

- 用div制作三角形，宽高为0，边框设置为透明，改变单个边框颜色

## JavaScript

行为层：实现交互效果，数据收发，表单验证
ECMAScript 是JS的标准

### 函数/功能

#### 内置函数

- alert

  ```js
  alert('你好');
  //弹出‘你好’
  //圆括号表示运行
  //字符串得用单引号/双引号包裹
  //通常语句末尾加分号
  ```

- console.log

  ```js
  console.log('你好');
  //在浏览器控制台输出‘你好’
  ```

- prompt

  ```js
  //弹框，让用户输入数字
  prompt('请输入···')
  //用户输入文字默认为字符串，若需要数值需要用Number包裹
  var a = Number(prompt('请输入数字'))
  ```

- typeof

  ```js
  //用于检测变量类型
  console.log(typeof x)
  //若x为数字则输出number，若为字符串则输出string
  ```

- parseInt
  
  ```js
  //用于取整，不四舍五入
  parseInt(3.8)	//结果为3
  ```

#### 自定义函数

- 定义函数function

  ```js
  // 使用function这个词语定义函数。函数就是功能，就是语句的封装。
  // function后面是函数的名字。函数的命名要符合标识符命名规范。
  // 函数的名字后面加一对儿圆括号，这个圆括号有用，后面例子告诉你干嘛的。
  function haha() {
      // 里面放语句
      console.log('就离谱~~~');
  }
  
  // 函数必须被调用，。调用非常简单，加圆括号即可。圆括号表示调用。
  // 看，函数我们只定义了1次，但是调用了3次。
  haha();
  haha();
  haha();
  ```


#### 函数的参数

* 一个参数

  ```js
  // 爱情函数，接受一个参数n表示多少天
  function love(n) {
      console.log('我爱你' + n + '天');
  }
  
  // 调用要传入多少天
  love(333);
  love(5);
  love(365);
  love(365 * 2);
  ```

  

* 两个参数

  ```js
  // 表白函数，传入name表示名字，n表示多少天
  function biaobai(name, n) {
      console.log(name + '我爱你' + n + '天');
  }
  // 调用按顺序传入名字、天
  biaobai('小红', 10);
  biaobai('小明', 365);
  ```

#### 函数的返回值

```js
// 注意，这个sum有return了。此时立刻想到老师说的：
// 有return的函数就是一个“机器”。有原料、有产出。
// sum这个函数的功能，就是接受a、b，返回a+b。
function sum(a, b) {
    // 返回a+b的和
    return a + b;
}

console.log(sum(3, 6));	//9
```

#### 重点案例：计算阶乘

```js
// 阿里巴巴面试题，计算1!+2!+3!+……9!
// 编程第一步，写一个机器，这个机器就是用来算阶乘的。
// 接受一个参数n，返回n的阶乘。
function jiecheng(n) {
    // 累乘器初始值是1
    var jieguo = 1;
    for (var i = 1; i <= n; i++) {
        jieguo *= i;
    }
    // 返回结果
    return jieguo;
}

// 主程序，初始值是0
var sum = 0;
// 遍历1到7，分别调用jiecheng()函数，把阶乘值累加
// 到sum中
for (var j = 1; j <= 7; j++) {
    sum += jiecheng(j);
}
console.log(sum);
```

* 案例：阶乘相加

  1. 普通方法

     ```js
     // 自定义函数
     function jiecheng(n) {
         var jc = 1;
         for (var i = 1; i <= n; i++) {
             jc *= i;
         }
         // 告诉JS哪个值是最重要。是我们的函数的总结果。
         return jc;
     }
     
     var sum = 0;
     for (var i = 1; i <= 7; i++) {
         sum += jiecheng(i);
     }
     console.log(sum);
     ```

  2. 车厢法

     ```js
     // 累加器
     var sum = 0;
     // 车厢
     var chexiang = 1;
     
     for(var i = 1; i <= 7; i++) {
         // 每循环一次，就会让车厢上一个车厢基础乘以i
         chexiang = chexiang * i;
         // 累加车厢
         sum += chexiang;
     }
     
     console.log(sum);
     
     
     
     // // 计算2 + 22 + 222 + 2222 + 22222 + 222222 + 2222222
     // // 后面一项是前面一项，乘10加2。
     // var sum = 0;
     // var chexiang = 0;
     
     // for(var i = 1; i <= 7; i++) {
     //     chexiang = chexiang * 10 + 2;
     //     sum += chexiang;
     // }
     // console.log(sum);
     ```

#### 匿名函数

```js
var fun = function () {
	console.log('我是匿名函数')
}
```



#### ***函数声明提升***

* 函数优先提升，所以执行期间不重刷函数

```js
fn();	//B

var fn = function () {
    console.log('A');
}

fn();	//A

function fn() {
    console.log('B');
}

fn();	//A
```



#### 闭包

JavaScript中函数会产生闭包（closure）。闭包是函数本身和该函数声明时所处的环境状态的组合。

##### 闭包的特性

* 记忆性：当闭包产生时，函数所处环境的状态会始终保持在内存中，不会在外层函数调用后被自动清除。这就是闭包的记忆性。

* 模拟私有变量：在Java、C++等语言中，有私有属性的概念，在JavaScript中，私有特性通常用闭包来模拟。

```js
function fun() {
    var m = 3;
    return function () {
        console.log(m);
    }
}

var inner = fun();

var m = 8;

// 输出自己诞生时候认识的那个m就是3。
// 因为自己诞生的时候，那个环境，已经加入了自己的闭包。
// 执行的时候，和执行的环境没关系，只看定义时候的环境。
inner(); 
```

##### 闭包的作用

闭包很有用，因为它允许我们将数据与操作该数据的函数关联起来。

```js
// 可以利用闭包，做“记忆”功能，你看这个a就被记忆住了。
// 每次调用inner都会从上一个值继续累加。因为a是闭包中的变量。（类比遮蔽效应）
// a现在就被“私有化”了，外部只能让它增加，无法让它减少。
function fun() {
    var a = 0;
    return function() {
        a++;
        console.log(a);
    }
}

var inner = fun();
inner();        // 1
inner();        // 2
inner();        // 3
inner();        // 4
inner();        // 5
```

##### 闭包的缺点

不能滥用闭包，否则会造成网页的性能问题，严重时可能导致内存泄露。所谓内存泄漏是指程序中己动态分配的内存由于某种原因未释放或无法释放。。

#### 递归

* 函数的内部语句可以调用这个函数自身，从而发起对函数的一次迭代。在新的迭代中，又会执行调用函数自身的语句，从而又产生一次迭代。当函数执行到某一次时，不再进行新的迭代，函数被一层一层返回，函数被递归。

* 递归是一种较为高级的编程技巧，它把一个大型复杂的问题层层转化为一个与原问题相似的规模较小的问题来求解。

##### 递归的要素

* 边界条件：确定递归到何时终止，也称为递归出口

* 递归模式：大问题是如何分解为小问题的，也称为递归体

```js
var a = 0;

// 函数内部自己调用自己，就是递归
function fun() {
    a++;
    console.log(a);

    // 如果a小于10的时候，自己再调用自己一遍
    if (a < 10) {
        fun();
    }
}

fun();
```

*使用递归计算阶乘*

```js
// 使用递归计算阶乘
function jiecheng(n) {
    // 三元运算符。看n是不是1，如果问1的阶乘是几，直接告诉人家是1。
    // 问的不是1的阶乘，那么就递归。
    return n == 1 ? 1 : n * jiecheng(n - 1);
}

console.log(jiecheng(4));
```

#### 层叠函数的作用域链

普通形态

```js
// 术语：作用域链。就是老师之前说的“遮蔽”效应。
// 我们在fun3里面输出a，那么JS引擎就会从最内层向最外层寻找a的定义
// 以先找到的a的定义为准。

function fun1() {
    var a = 23333;
    function fun2() {
        var a = 8888;
        function fun3() {
            var a = 6666;
            console.log(a);
        }
        fun3();
    }
    fun2();
}

fun1();


```

变形形态

```js
var a = '虎虎生威';

// 函数的作用域链，定义的时候就决定了。
// 你看这个fun1定义在全局，所以它里面的那个a就是全局的a。
// 如果你把这个fun1放到了fun2中去执行，那么它依然认识a是全局的a。
// 结论：一句话，函数定义在了哪里，它就认识哪里的a。
function fun1() {
    console.log(a);
}

function fun2() {
    var a = '金虎送福';
    fun1();
}

fun2();
```



#### 函数的其他知识

##### *聊聊垃圾回收机制*

```js
function sum(a, b) {
    // 实际参数3传给了形式参数a，实际参数4传给了形式参数b。
    // 内存条会给a、b开辟一个空间。
    return a + b;

    // 随着函数执行完毕，a、b这两个内存空间就被清空了。
    // 就被当做垃圾进行了回收。
}
console.log(sum(3, 4));
```

##### *高阶函数及柯里化*

```js
// 记住，一个函数返回函数，那么这个函数就是“高阶函数”
// 高阶函数非常有用，我们的闭包是高阶函数的一个体现。
// 这里可以介绍柯里化函数比较浅显的定义。因为高级的定义，需要我们学习面向对象。
// 柯里化函数：我们可以让一个函数返回另一个函数，多次圆括号调用实现当初那个功能。还有另一个表述：一个函数可以返回接受剩下的参数的函数。
// 我们将在面向对象学习过程中，讲“完全柯里化”

function curryAdd(x) {
    return function (y) {
        return x + y;
    }
}

var a = curryAdd(3)(5)
console.log(a)	//8

// addingThree的闭包中存储了x是3；addingFive的比包中存储了x是5。所以说，只要你调用一次外部函数，返回的内部函数都是全新的，拥有井水不犯河水的闭包值。
var addingThree = curryAdd(3);
var addingFive = curryAdd(5);

console.log(addingThree(9));        // 12
console.log(addingThree(1));        // 4
console.log(addingFive(4));         // 9
console.log(addingThree(2));        // 5
console.log(addingFive(6));         // 11
```



### 变量

#### 创建及赋值var

```js
//（variable可变的）定义变量a并将5赋值给a
var a = 5;
var b = 3;
----------
var a,b;
a = 5;
b = 5;
----------
var a = 5,b = 3;
```

#### 命名

- 只能由字母abc、数字123、下划线_、美元$组成，且不能以数字开头
- 建议只用驼峰命名法（例：mathTestScore）

#### 默认值

```js
// 看这个变量a只var了，但是没有赋值
var a;

// 此时a的默认值就是undefined。
// undefined是一个特殊值。是JS创始人定的。没啥理由。
console.log(a);     // undefined


console.log(typeof 234);        // number
console.log(typeof '哈哈');     // string
console.log(typeof true);       // boolean
console.log(typeof undefined);  // undefined
console.log(typeof null);  		// object
```

#### ***变量声明提升***

1. ````js
   // JS在执行所有代码之前，会进行一个“预读”过程。
   // 好比我们要预习整片课文，把课文中的陌生字提前用字典查好。
   // JS也会进行预读。它会预读所有的变量定义。
   // 仿佛变量定义被“提升”了。所有用var定义的变量，都会被提升。
   // 提升，只提升定义，不提升值
   
   console.log(a);     // undefined。不会报错。
   var a = 10;
   ````

2. 函数中的变量声明提升情况

   ```js
   var a = 1;
   
   function fun() {
       // 注意，这里是JS经典面试题。
       // 我们这里一定要记住，变量声明有提升！
       // 所以，这里这个a是局部的。提升只提升定义，不提升值。
       console.log(a);     // undefined
       var a = 2;
   }
   
   fun();
   ```

3. 变量提升无视if语句

   ```js
   var a = 1;
   
   function fun() {
       // 局部变量。因为a提升了
       console.log(a);     // undefined
       // 变量提升无视if语句
       if (3 > 8) {
           // var a照样提升！
           var a = 2;
       }
       console.log(a);		// 2
   }
   
   fun();
   ```
   
   

#### 变量的作用域

##### 局部变量

```js
function haha() {
    // 你看，这个变量m它定义在了haha函数内部，所以
    // 这个m只在haha函数里面有定义。m被称为“局部变量”。
    var m = 123;
    // 这里能输出123，因为这是函数内部
    console.log(m);
}
// 调用函数
haha();

// 这条语句会报错，因为m只在haha函数里面有定义。在外面没有定义。
console.log(m);
```

##### 全局变量

```js
// 这个a被定义在了函数的外面。
// 它就是“全局变量”
var a = 4;

function fun() {
    // 所以，这里将全局的a进行了加1
    a++;
    console.log(a);     // 输出全局a的值，就是5
}

fun();
console.log(a);     // 5
```

##### 遮蔽效应

```js
var a = 3;

function fun() {
    // 如果局部变量和全局变量名字一样，那么局部变量就把全局变量“遮蔽”了。
    var a = 8;
    console.log(a);     // 输出局部变量a，就是8。
}

fun();
console.log(a);     // 3
```



### 运算符

#### 赋值运算符

- 赋予=

#### 数学运算符

* 加+

  ````js
  // prompt功能是弹出一个输入框。并且将用户输入的数字存入变量a
  // 注意，prompt它有一个毛病，就是它接受的值是字符串！哪怕用户输入的是数字，也会被当做字符串处理。
  // 解决这个毛病，就要用Number()转为数字。N必须大写。
  var a = Number(prompt('请输入第一个数字啊'));
  // 弹出另一个输入框，并且将用户输入的数字存入变量b
  var b = Number(prompt('请输入第二个数字啊'));
  
  alert(a + b);
  ````

* 减-

* 乘*

  ```js
  // 请用户输入圆的半径
  var r = Number(prompt('请输入圆的半径'));
  
  // 计算
  var s = 3.1415 * r * r;
  
  // 弹出结果。这里的.toFixed(2)是我们百度查来的。表示四舍五入到两位小数。
  alert(s.toFixed(2));
  ```

  

* 除/

  ```js
  // 让用户输入华氏温度
  var h = Number(prompt('请输入华氏温度'));
  
  // 进行转换
  var s = (h - 32) / 1.8;
  
  // 弹出结果
  alert('摄氏度是' + s);
  ```

  

* 余数%

  ```js
  // 取余运算就是%。只看余数，不关心商。
  console.log(21 % 7);    // 0
  console.log(8 % 5);     // 3
  console.log(13 % 5);    // 3
  ```

  



```js
// 比如现在还剩总秒数
var totalS = 135;
// 计算相当于几分钟
var m = parseInt(totalS / 60);
// 零头多少秒
var s = totalS % 60;
// 输出。这里面的加号有点多，看清楚，自己多写几遍！
console.log('秒杀结束还剩' + m + '分钟' + s + '秒');

```



#### 关系运算符

- 大于>

- 小于<

- 大于等于>=

- 小于等于<=

- 等于==

  - 两个=不比较类型：5 == '5'

- 全等于===

  ```js
  // ==符号，是“相等”判断，不比较类型。
  console.log(5 == '5');      // true
  
  // ===符号，是“全等”判断，比较类型。
  console.log(5 === '5');     // false
  
  // !=就是不等于，5就是不等于6呀
  console.log(5 != 6);        // true
  ```

  

- 不等!=

- 不全等!==

#### 逻辑运算符

- 非!
- 与&&

	- 都真为真
- 或||

	- 有真为真

### if语句

```js
// 请用户输入自己的年龄
var age = Number(prompt('请输入自己的年龄'));
// 判断年龄是否介于18到70之间。我们这里用到了新的运算符&&。
// &&表示“且”，就是老百姓说的“而且”
if (age >= 18 && age <= 70) {
    alert('能打');
} else {
    alert('不能打');
}

//JS不能连笔，若要写(age大于等于18且小于等于70)必须写为(age >= 18 && age <= 70),不可写为(18 <= age <= 70)
```

#### 三元运算符

```js
//三元运算符
var a = 3 > 8 ? 6 : 9;
console.log(a);			//9

var b = 3 < 8 ? 6 : 9;
console.log(b);			//6

var age = 45;
var chenghu = age >= 18 ? '成年人' : '小孩';

console.log(chenghu);	//'成年人'
```



* 计算BMI数值(else if 语句)

````js
// 请输入身高
var h = Number(prompt('请输入身高'));
// 请输入体重
var w = Number(prompt('请输入体重'));
// 计算BMI
var bmi = w / (h * h);
// 多分支的if语句。注意跳楼现象，不用写&&另一边儿。
if (bmi <= 18.4) {
    alert('偏瘦~多吃点吧，健康生活。');
} else if (bmi < 24) {
    alert('正常~~继续保持。');
} else if (bmi < 28) {
    alert('过重。管住嘴，迈开腿。减肥吧。');
} else {
    alert('肥胖。请咨询健身教练。');
}

//*注意if语句跳楼现象，需要从小范围依次向大范围扩大
````



### for循环（定范围循环）

```js
// 题目，计算1+2+3+4+……+99+100等于多少。

// 定义一个累加器。sum是英语总和的意思。名字可以随便起，但是一般都叫sum。
var sum = 0;
// 循环1到100
for (var i = 1; i <= 100; i++) {
    // += 是一个新的运算符，表示在原有基础上累加
    sum += i;
}

console.log(sum);
//定义变量i赋值为1，若i小于100，则sum自增i且i自增1
```

### while循环（不定范围循环）

案例：加到几就能突破50

```js
// 【方法1】就是老师推荐的while(true)写法。
var sum = 0;
var n = 0;
while (true) {
    n++;
    sum += n;
    if (sum > 50) {
        console.log(n);
        // 找到复合条件的项，就打断
        break;
    }
}

// 【方法2】比较正统
var sum = 0;
var n = 0;

while (sum <= 50) {
    n++;
    sum += n;
}
console.log(n);
```



### switch-case语句

```js
// case穿透。下面程序，BCDE都会输出。F不会输出，因为break了，停掉了。
var a = 2;
switch (a) {
    case 1:
        console.log('A');
    case 2:
        console.log('B');
    case 3:
        console.log('C');
    case 4:
        console.log('D');
    case 5:
        console.log('E');
        break;
    case 6:
        console.log('F');
};
```



### 数组

```js
var arr = ['A','B','C','D','E'];
```

- 地标从0开始

  ```js
  console.log(arr[0])					//'A'
  console.log(arr[arr.length - 1])	 //'E'
  console.log(arr[5])					//undefined
  ```

  数组的长度（arr.length）

#### *数组的方法汇总*

| 方法       | 功能                           | 是否为变异方法 |
| ---------- | ------------------------------ | -------------- |
| push()     | 在尾部插入新项                 | 是             |
| pop()      | 在尾部删除                     | 是             |
| unshift()  | 在头部插入新项                 | 是             |
| shift()    | 在头部删除                     | 是             |
| splice()   | 替换（也能任意插入、任意删除） | 是             |
| reverse()  | 逆序                           | 是             |
| slice()    | 子数组                         |                |
| indexOf()  | 寻找某项的下标                 |                |
| includes() | 某项是否在数组中               |                |
| join()     | 合并数组为字符串               |                |

##### splice()方法

```js
//本职工作是替换项 
//从下标为3的项开始，删除两项，插入'X','Y','Z'
arr.splice(3, 2, 'X', 'Y', 'Z');	
//可以用来删除任意项
arr.splice(3, 2);
//可以用来任意插入项
arr.splice(3, 0, 'X', 'Y', 'Z');
```

##### slice()方法

slice(a, b)用于截取子数组，截取的子数组从下标为a的项开始，到下标为b（但不包括下标为b的项）结束

* slice(a, b)方法不会更改原有数组，它不是变异方法

* slice()如果不提供第二个参数，则表示从指定项开始，提取所有后续所有项作为子数组

* slice()方法的参数允许为负数，表示数组的倒数第几项

##### indexOf()和includes()

indexOf()方法的功能是搜索数组中的元素，并返回它所在的位置，如果元素不存在，则返回-1

```js
arr.indexOf('B')	//1
arr.indexOf(1)		//-1
```

includes()方法的功能是判断一个数组是否包含一个指定的值，返回布尔值

```js
arr.includes('C')	//true
arr.includes('F')	//false
```

##### join()和split()

• 数组的join()方法可以使数组转为字符串；字符串的split()方法可以使字符串转为数组

• join()的参数表示以什么字符作为连接符，如果留空则默认以逗号分隔，如同调用toString()
方法

• split()的参数表示以什么字符拆分字符串，一般不能留空;留空时默认以逗号分隔，无逗号则视为整体

```js
var arr = ['A', 'B', 'C', 'D', 'E'];
console.log(arr.join());		//A,B,C,D,E
console.log(arr.join(''));		//ABCDE
console.log(arr.join('2'));		//A2B2C2D2E

var str1 = arr.join();  		//A,B,C,D,E

console.log(str1.split());		//['A','B','C','D','E']
console.log(str1.split(''));	//['A', ',', 'B', ',', 'C', ',', 'D', ',', 'E']

var str2 = arr.join('');		//ABCDE

console.log(str2.split());		//['ABCDE']
console.log(str2.split(''));	//['A','B','C','D','E']

//总结：join加引号会将数组所有项和为一个字符串，不加引号会按逗号分开；split加引号会将每个字符分为不同的项，不加引号会将字符串作为整体变为数组。综上，一般join和split都要加引号
```

##### reverse()逆序数组

```js
console.log(arr.reverse());		//['E', 'D', 'C', 'B', 'A']
```

##### 字符串逆序

```js
// var str = 'ABCDEF';

// // 将字符串切割为数组
// var arr = str.split('');

// // 将数组逆序。reverse表示逆序，只有数组能逆序。reverse()是一个变异方法。
// arr.reverse();

// // 把数组合并为字符串
// var result_str = arr.join('');

// // 输出结果字符串
// console.log(result_str);


// ********************************
var str = '我爱JS';

console.log(str.split('').reverse().join(''));
```



#### 数组常见算法

##### 数组去重

```js
var arr = [1, 1, 1, 1, 2, 2, 2, 2, 1, 1, 1];

var result = [];

for (var i = 0; i < arr.length; i++) {
    // 如果不在结果数组中，就推入
    if (!result.includes(arr[i])) {
        result.push(arr[i]);
    }
}

console.log(result);
```

##### 数组交集

```js
var arr1 = [3, 2, 5, 6, 1];
var arr2 = [2, 6, 9, 3, 1, 4];
var arr3 = [7, 3, 4, 2];
// 准备一个结果数组
var resultArr = [];
// 遍历1号数组，看这项是不是在arr2中，且在arr3中
for (vari = 0; i < arr1.length; i++) {
    // 下面的语句要练一下！够你喝一壶的。
    // 是不是在arr2中，且在arr3中
    if (arr2.includes(arr1[i]) &&
        arr3.includes(arr1[i])) {
        resultArr.push(arr1[i]);
    }
}
// for (var i = 0; i < arr1.length; i++) {
//     var item = arr1[i];
//     if (arr2.includes(item) && arr3.includes(item)) {
//         result.push(item);
//     }
// }
console.log(resultArr);
```

##### *求数组连续重复出现最长的项*

```js
var arr = ['A', 'A', 'B', 'B', 'B', 'C', 'C', 'A'];

// 当前正在连续出现谁
var temp = arr[0];
// 当前这个值连续了了几次
var count = 1;
// 当前状元值
var zy = arr[0];
// 当前状元重复次数
var zy_c = 1;


// 遍历数组。如果当前遍历的项和temp相同，那么让count加1；
// 如果遍历的项和temp不同，那么热闹了：
//      判断count是否大于zy_c，如果大，就让这项成为新状元；
//      让temp设置为当前遍历这项，count复位为1。
// （注意，今天必须用纸笔，画一次这个算法了！画出来，你就懂了。）

for (var i = 1; i <= arr.length; i++) {
    if (arr[i] == temp) {
        count++;
    } else {
        if (count > zy_c) {
            zy_c = count;
            zy = temp;
        }

        temp = arr[i];
        count = 1;
    }
}

console.log(zy, zy_c);
```

#### 字符串与数组的关系

字符串每一位都有序号，序号从0开始

字符串直接加方括号，即可得到该位的字符

```js
var str = '我爱JS';
console.log(str[0]); 	// 我
console.log(str[1]); 	// 爱
console.log(str[2]); 	// J
console.log(str[3]); 	// S

function nx(str) {
    return str.split('').reverse().join('');
}

console.log(nx('我爱你'));
console.log(nx('abcdefg'));
```

字符串“打点儿”访问length属性，即可得到字符串的长度

```js
console.log(str.length); 	// 4
```



### 对象

```js
// 对象用来描述事物。

// 下面这个对象描述小明
var xiaoming = {
    name: '小明',
    englishName: 'Tom',
    age: 12,
    sex: '男',
    shuxue: 88,
    yingyu: 77,
    yuwen: 100,
    hobbies: ['打农药', '编程', '吃饭', '睡觉']
};

// 对象打点跟上属性名，就能得到这个属性的值了
console.log(xiaoming.sex);	//男
console.log(xiaoming.age);	//12
console.log(xiaoming.yuwen);	//100
console.log(xiaoming.englishName);	//Tom
console.log(xiaoming.hobbies);	//['打农药', '编程', '吃饭', '睡觉']
```





### 类型值

#### 基本类型值

| 类型名    | typeof检测结果             | 值举例                          |
| :-------- | :------------------------- | ------------------------------- |
| 数字      | number                     | 6、-33、6.5、3e6、NaN、Infinity |
| 字符串    | string                     | '直课堂'、'123'、''             |
| 布尔      | boolean                    | true、false(就这两个)           |
| undefined | undefined                  | undefined(就这一个)             |
| null      | object(人们认为是nvll类型) | null(就这一个)                  |

##### NaN

````js
// Not a Number，不是一个数。
// 自己确是数字类型值
console.log(typeof NaN);	//Number

// 0除以0等于NaN
console.log(0 / 0);		//NaN

// 数学运算中，实在算不出来
console.log(3 * '哈哈');
console.log('我' - '你');

// 谁都不爱，自己的都不认识自己
console.log(NaN == NaN);         // false
console.log(NaN === NaN);        // false

// 判断值是不是NaN
var a = NaN;
if (isNaN(a)) {
    alert('抓到啦！');
}
````

##### 字符转换

###### 其他值→数字	方法1：Number()

|                   | 举例                                                         |                                                        | 结论                                                         |
| :---------------- | ------------------------------------------------------------ | ------------------------------------------------------ | ------------------------------------------------------------ |
| 字符串 → 数字     | Number('123');<br/> Number('123.4'); <br/>Number('123年'); <br/>Number('3e6');<br/> Number(''); <br/> | // 123<br/>// 123.4<br/>// NaN<br/>// 3000000<br/>// 0 | 纯数字字符串能变为<br/>数字，不是纯数字的<br/>字符串将转为NaN |
| 布尔 → 数字       | Number(true); <br/>Number(false);                            | // 1<br/>// 0                                          | true变为1，false变<br/>为0                                   |
| undefined  → 数字 | Number(undefined);                                           | // NaN                                                 | undefined变为NaN                                             |
| null → 数字       | Number(null);                                                | // 0                                                   | null变为0                                                    |

###### 其他值→数字	方法2：parseInt()

```js
parseInt('3.14');			 // 3
parseInt('3.14是圆周率'); 		// 3
parseInt('10年'); 			// 10
parseInt('圆周率是3.14');	 // NaN
parseInt('3.99'); 			// 3

结论：
1、parseInt()将自动截掉第一个非数字字符之后的所有字符。parseInt有净化
功能。比Number强大一点。
2、如果字符串不是以数字开头，则转为NaN。只能净化后面，不能净化前面。
3、parseInt()函数不四舍五入。
```

###### 其他值→字符串	方法1：String()

|                    | 举例                                                         |                                                        | 结论                        |
| ------------------ | ------------------------------------------------------------ | ------------------------------------------------------ | --------------------------- |
| 数字→字符串        | String(123); <br/>String(123.4); <br/>String(NaN); <br/>String(Infinity); | // '123'<br/>// '123.4'<br/>// 'NaN'<br/>// 'Infinity' | 变为“长得相同”<br/>的字符串 |
| 布尔 → 字符串      | String(true);<br/>String(false);<br />                       | // 'true'<br/> // 'false'                              | 变为“长得相同”<br/>的字符串 |
| undefined → 字符串 | String(undefined);                                           | // 'undefined'                                         | 变为“长得相同”<br/>的字符串 |
| null → 字符串      | String(null);                                                | // 'null'                                              | 变为“长得相同”<br/>的字符串 |

###### 使用toString()方法 方法2：toString()

除undefined、null之外，其他所有值（数字、布尔、数组、对象）都有toString()方法，用来转为字符串。

###### 其他值→布尔	方法：Boolean()

|                | 举例                                                         |                                                            | 结论                                |
| -------------- | ------------------------------------------------------------ | ---------------------------------------------------------- | ----------------------------------- |
| 数字→布尔      | Boolean(123); <br/>Boolean(Infinity); <br/>Boolean(-Infinity); <br/>Boolean(0); <br/>Boolean(NaN); | // true<br/>// true<br/>// true<br/>// false<br/> // false | 0和NaN转为false，其他数字都转为true |
| 字符串→布尔    | Boolean(''); <br/>Boolean('abc'); <br/>Boolean('false');     | // false<br/>// true<br/>// true                           | 空字符串变为false，其他都转为true   |
| undefined→布尔 | Boolean(undefined);                                          | // false                                                   | undefined转为false                  |
| null→布尔      | Boolean(null);                                               | // false                                                   | null转为false                       |

###### 隐式转换

1. 数学运算中，非数字值都会被自动用Number()转为数字

   ```js
   console.log('7' - '3'); 		// 数字4
   console.log('3' * '6'); 		// 数字18
   console.log('3年' * 6);			// NaN
   console.log('8' * null); 		// 0
   console.log(5 * undefined); 	// NaN
   ```

2. if条件中，非布尔值会被自动用Boolean()转为布尔值

   ```js
   if (8) 			// 视为true
   if ('abc') 		// 视为true
   if ('') 		// 视为false
   if (0) 			// 视为false
   if (NaN) 		// 视为false
   if (undefined) 	// 视为false
   if (null) 		// 视为false
   ```

###### 判等时的类型转换规则

1. 布尔 == 数字

   JS引擎会把布尔值转为数字，即true变为1，false变为0

2. 字符串 == 数字

   JS引擎会把字符串用Number()转为数字，即纯数字字

   符串能变为数字，不是纯数字的字符串将转为NaN

3. 字符串 == 布尔

   '1' == true

   '0' == false

4. undefined == 数字 undefined == 布尔

   记住，undefined一律不等于任何数字，包括不等于NaN。

   undefiend也不等于任何布尔值！

5. null == 数字 null == 布尔

   记住，null一律不等于任何数字，包括不等于NaN。你说，

   老师！Number(null)明明就是0，为啥null == 0还是false呢？

   你问Brendan Eich。

   null 也不等于任何布尔值！

###### null和undefined相等

```js
null == undefined 		// true
```

#### 引用类型值：函数

### a++ 和 ++a 的区别

a++是先用再加

```js
var a = 6;
var b = a++;	//a先赋值给b，再自增1
console.log(a); // 7
console.log(b); // 6
```

++a是先加再用

```js
var a = 6;
var b = ++a;	//a先自增1，再赋值给b
console.log(a); // 7
console.log(b); // 7
```

*工作严禁++写在前面，只有面试题的意义*

### 短路计算公式

a && b
如果a是真，则表达式结果是b
如果a是假，则表达式结果是a

a || b
如果a是真，则表达式结果是a
如果a是假，则表达式结果是b

*借假钱，花真钱*

### 有关IEEE754

现象：

在JavaScript中，有些小数的数学运算不是很精准

原因：

JavaScript使用了IEEE754二进制浮点数算术标准，这会使一些小数运算产生“丢失精度”问题

解决办法：

在进行小数运算时，要调用数字的toFixed()方法进行四舍五入，保留指定小数位数。

```js
console.log(0.1 + 0.2); // 0.30000000000000004
```

## DOM

### DOM简介

* DOM 是英文Document Object Model的缩写，即文档对象模型。它是一种跨平台的、独立于编程语言的API，它把HTML、XHTML或XML文档当作一个树结构，而每个节点视为一个对象，这些对象可以被编程语言操作，进而改变文档的结构，映射到文档的显示。

* DOM就是我们为了方便操作HTML，把HTML文档中的节点全部视为一个个的对象，然后这些对象依照层级关系形成一棵树
* DOM是节点思维，不是字符串思维

### 访问（得到）元素节点

#### document对象

* 访问元素节点主要依靠document对象	<!--DOM = document object model。-->

1. document对象是DOM中最重要的东西，几乎所有DOM的功能都封装在了document对象中
2. document对象表示整个HTML文档，它是DOM节点树的根
3. document对象的nodeType属性值是9

#### 得到元素节点的常用方法

| 方法                              | 功能                                | 兼容性           |
| --------------------------------- | ----------------------------------- | ---------------- |
| document.getElementById()         | 通过***id***得到<u>元素</u>         | IE6              |
| document.getElementsByTagName()   | 通过***标签名***得到元素<u>数组</u> | IE6              |
| document.getElementsByClassName() | 通过***类名***得到元素<u>数组</u>   | IE6              |
| document.querySelector()          | 通过***选择器***得到<u>元素</u>     | IE8部分、IE9完全 |
| document.querySelectorAll()       | 通过***选择器***得到元素<u>数组</u> | IE8部分、IE9完全 |

```js
/*
    我们学习得到元素的方法
    ● 通过id：     document.getElementById();
    ● 通过标签（得到数组）：document.getElementsByTagName();
    ● 通过选择器：   document.querySelector();
    ● 通过选择器得到所有（得到数组）：document.querySelectorAll();
*/


// 【通过id得到元素】注意不要写成#box1。
var box1 = document.getElementById('box1');
// 设置box1的内部文字。innerText表示内部文字
box1.innerText = '你好';


// 【通过标签名得到p元素数组】
var ps = document.getElementsByTagName('p');
for (var i = 0; i < ps.length; i++) {
    ps[i].innerText = '我是第' + i + '个p';
}


// 【通过标签名得到元素，可以限定范围】，即在某个盒子中找它们。
var box2 = document.getElementById('box2');
var lis = box2.getElementsByTagName('li');      // 注意这里是box2打点，表示让box2去寻找元素
for (var i = 0; i < lis.length; i++) {
    lis[i].innerText = '我是第' + i + '个li';
}


// 【通过选择器得到元素】只能选一个，如果有多个，只选最上面的那个
// var myspan = document.querySelector('#box3 .danger span.myspan');
// myspan.innerText = '哈哈哈新年好';


// 【通过选择器得到所有元素】能够得到页面上的多个元素，得到数组。
var myspans = document.querySelectorAll('#box3 .danger span.myspan');
for (var i = 0; i < myspans.length; i++) {
    myspans[i].innerText = '新年好！'
}
```



##### getElementById()

document.getElementById()功能是通过id得到元素节点

HTML代码：

```html
<div id="box">我是一个盒子</div>
<p id="para">我是一个段落</p>
```

JS代码：

```JS
var oBox = document.getElementById('box');
var oPara = document.getElementById('para');
//参数就是元素节点的id，注意不要写#号
```

* 
  如果页面上有相同id的元素，则只能得到第一个，所以id不要相同！！

* 不管元素藏的位置有多深，都能通过id把它找到

##### getElement<u>*s*</u>ByTagName()

 getElementsByTagName()方法的功能是通过标签名得到节点<u>数组</u>

HTML代码：

```html
<p>我是段落</p>
<p>我是段落</p>
<p>我是段落</p>
<p>我是段落</p>
```

JS代码：

```js
var ps = document.getElementsByTagName('p');
```

* 数组方便遍历，从而可以批量操控元素节点
* 即使页面上只有一个指定标签名的节点，也将得到长度为1的<u>数组</u>
* <u>任何一个节点元素也可以调用getElementsByTagName()方法，从而得到其内部的某种类的元素节点</u>

##### querySelector()

querySelector()方法的功能是通过选择器得到元素

HTML代码：

```html
<div id="box1">
<p>我是段落</p>
<p class="spec">我是段落</p>
<p>我是段落</p>
</div>
```

JS代码：

```js
var the_p = document.querySelector('#box1 .spec');
```

* querySelector()方法只能得到页面上一个元素，如果有多个元素符合条件，则只能得到第一个元素
* querySelector()方法从IE8开始兼容，但从IE9开始支持CSS3的选择器，如:nth-child()、:[src^='dog']等CSS3选择器形式都支持良好

##### querySelectorAll()

* querySelectorAll()方法的功能是通过选择器得到元素数组
* 即使页面上只有一个符合选择器的节点，也将得到长度为1的数组
* 兼容情况和querySelector相同

### 节点的关系

* 从IE9开始支持一些“<u>只考虑元素节点</u>”的属性

  | 关系           | 考虑所有节点    | 只考虑元素节点                |
  | -------------- | --------------- | ----------------------------- |
  | 子节点         | childNodes      | children                      |
  | 父节点         | parentNode      | parentNode                    |
  | 第一个子节点   | firstChild      | first<u>Element</u>Child      |
  | 最后一个子节点 | lastChild       | last<u>Element</u>Child       |
  | 前一个兄弟节点 | previousSibling | previous<u>Element</u>Sibling |
  | 后一个兄弟节点 | nextSibling     | next<u>Element</u>Sibling     |

### 节点操作

#### 改变元素节点中的内容

改变元素节点中的内容可以使用两个相关属性：

1. innerHTML
2. innerText

innerHTML属性能以HTML语法设置节点中的内容

* *虎年快乐*

  ```js
  box.innerHTML = '<i>虎年快乐</i>';
  ```

  

* \<i>虎年快乐\</i>

  ```js
  box.innerText = '<i>虎年快乐</i>';
  ```

#### 改变元素节点的CSS样式

改变元素节点的CSS样式需要使用这样的语句：

```js
oBox.style.backgroundColor = 'red';
//background-color	→	backgroundColor
//CSS属性要写成“驼峰”形式
oBox.style.backgroundImage = 'url(images/1.jpg)';
//CSS属性值要设置成完整形式
oBox.style.fontSize = '32px';
//注意写单位
```



#### 改变元素节点的HTML属性

* 标准W3C属性，如src、href等等，只需要直接打点进行更改即可

  ```js
  // 用JS设置图片的src，直接.src改就行了。极其好用！
  myimg.src = 'images/yangmi.png'
  // 用JS设置a标签的href
  mya.href = 'http://www.zhipin.com';
  // 在新窗口中打开超级链接
  mya.target = 'blank';
  // 自己编的属性，就不能直接打点，比如不能box.mmmm 
  = '虎虎生威';
  box.setAttribute('mmmm', '虎虎生威');
  // 读取自定义属性，用getAttribute
  console.log( box.getAttribute('mmmm') );
  
  ```

  

* 注意class要改为className

  ```js
  myh1.className = 'xian';
  ```


##### 自定义属性

* 不符合W3C标准的属性（自己编的属性），要使用setAttribute()和getAttribute()来设置、读取

  ```js
  // 自己编的属性，就不能直接打点，比如不能box.mmmm 
  = '虎虎生威';
  box.setAttribute('mmmm', '虎虎生威');
  // 读取自定义属性，用getAttribute
  console.log( box.getA ttribute('mmmm') );
  ```

* 自定义属性若以data-开头，则可直接打点调用

  ```
  
  ```

  



#### 创建节点

##### 创建孤儿节点

* document.createElement() 方法用于创建一个指定tag name的HTML元素

  `var oDiv = document.createElement('div');`

* 新创建出的节点是“孤儿节点”，这意味着它并没有被挂载到DOM树上，我们无法看见它

* 必须继续使用appendChild()或insertBefore()方法将孤儿节点插入到DOM树上

```js
/*
    创建节点，大概思路就是先创建孤儿节点，然后挂上去。
    
    第一步创建孤儿节点，用document.createElement();

    第二步挂上去，有两种手段：
        挂在内部现有元素之后：      爸爸.appendChild(新元素);
        挂在内部现有某元素之前：    爸爸.insertBefore(新元素, 标杆);
*/


var box = document.querySelector('#box');

// 创建孤儿节点
var p = document.createElement('p');
// 设置内容
p.innerText = '我是虎年新来的p';
```



##### 插入父节点后面

* 任何已经在DOM树上的元素节点，都可以调用appendChild()方法，它可以将孤儿节点挂载到它的内部，成为它的最后一个子节点

  `父节点.appendChild(孤儿节点);`

```js
//【挂孤儿节点方法1：追加到后面】
//appendChild表示新创建的孤儿p，会被添加到原有内容之后。
//公式:            爸爸.appendChild(新孩子);
box.appendChild(p);
```



##### 插到父节点之前

* 任何已经在DOM树上的元素节点，都可以调用insertBefore() 方法，它可以将孤儿节点挂载到它的内部，成为它的“标杆子节点”之前的节点

  `父节点.insertBefore(孤儿节点, 标杆节点);`

  ```js
  // 【挂孤儿节点方法2：添加到某元素前面】
  // insertBefore公式：  爸爸.insertBefore(新孩子, 标杆);
  // 你看，我们用第一个子元素当标杆，所以新p就被插入到了第一个子元素之前。
  box.insertBefore(p, box.firstElementChild);
  ```

  

#### 移动节点

如果将已经挂载到DOM树上的节点作为appendChild()或者insertBefore()的参数，这个节点将会被移动

`新父节点.appendChild(已经有父亲的节点);`
`新父节点.insertBefore(已经有父亲的节点, 标杆子节点);`

这意味着一个节点不能同时位于DOM树的两个位置

#### 删除节点

```html
<div id="box">
    <p>虎虎生威</p>
    <p>虎虎生威</p>
    <p id="aaa">霉运</p>
    <p>虎虎生威</p>
    <p>虎虎生威</p>
</div>

<script>
    /*
        节点不能自杀。“想死找爸爸”。
    */
    var box = document.getElementById('box');
    var aaa = document.getElementById('aaa');

    //公式：  爸爸.removeChild(儿子)
    box.removeChild(aaa);

       
</script>
```



### 事件监听

#### 什么是“事件监听”

* DOM允许我们书写JavaScript代码以让HTML元素对事件作出反应

  * 当鼠标点击元素时

  * 当鼠标移动到元素上时

  * 当文本框的内容被改变时

  * 当键盘在文本框中被按下时

  * 当网页已加载完毕时

  * ......

* “监听”，顾名思义，就是让计算机随时能够发现这个事件发生了，从而执行程序员预先编写的一些程序

* 设置事件监听的方法主要有onxxx和addEventListener()两种，二者的区别将在“事件传播”一课中介绍

#### 设置事件监听的方法

最简单的给元素设置事件监听的方法就是设置它们的onxxx属性，像这样：

```js
oBox.onclick = function () {
// 点击盒子时，将执行这里的语句
}
```

#### 常见的鼠标事件监听

| 事件名       | 事件描述                                           |
| ------------ | -------------------------------------------------- |
| onclick      | 当鼠标单击某个对象                                 |
| ondblclick   | 当鼠标双击某个对象                                 |
| onmousedown  | 当某个鼠标按键在某个对象上被按下                   |
| onmouseup    | 当某个鼠标按键在某个对象上被松开                   |
| onmousemove  | 当某个鼠标按键在某个对象上被移动（有小专题给你讲） |
| onmouseenter | 当鼠标进入某个对象（相似事件onmouseover）          |
| onmouseleave | 当鼠标离开某个对象（相似事件onmouseout）           |

```js
<div id="box" class="box"></div>
<img id="mypic" src="images/yangmi.png">

<script>
/*
    事件监听就是元素能够响应鼠标、键盘的行为。

    元素.on啥事 = function() {

    }
*/

// 得到元素
var box = document.querySelector('#box');
var mypic = document.querySelector('#mypic');

// on表示当，click表示“点击”
// onclick就是点击的意思
box.onclick = function () {
    alert('虎虎生威');
};

// 鼠标进入盒子时
box.onmouseenter = function () {
    box.style.backgroundColor = 'blue';
};

// 鼠标离开盒子时
box.onmouseleave = function () {
    box.style.backgroundColor = 'orange';
};

// 鼠标进入图片时
mypic.onmouseenter = function () {
    mypic.src = 'images/wangjunkai.png'
};

// 鼠标离开图片时
mypic.onmouseleave = function () {
    mypic.src = 'images/yangmi.png'
};
```



#### 常见的键盘事件监听

| 事件名     | 事件描述                                                     |
| ---------- | ------------------------------------------------------------ |
| onkeypress | 当某个键盘的键被按下（系统按钮如箭头键和功能键<u>无法</u>得到识别） |
| onkeydown  | 当某个键盘的键被按下（系统按钮<u>可以</u>识别，并且会先于onkeypress发生） |
| onkeyup    | 当某个键盘的键被松开                                         |

#### 常见的<u>*表单*</u>事件监听

| 事件名   | 事件描述                                |
| -------- | --------------------------------------- |
| onchange | 当用户改变域的内容                      |
| onfocus  | 当某元素获得焦点（比如tab键或鼠标点击） |
| onblur   | 当某元素失去焦点                        |
| onsubmit | 当表单被提交                            |
| onreset  | 当表单被重置                            |

```js
var kuang = document.getElementById('kuang');
var myh1 = document.getElementById('myh1');

var n = 0;

// 当文本框内容被更改时触发。当然，文本框必须失焦。
// kuang.onchange = function() {
//     n++;
//     myh1.innerText = n;
// }

// 当文本框聚焦的时候触发
// kuang.onfocus = function() {
//     n++;
//     myh1.innerText = n;
// }

// 当文本框失去焦点的时候触发
kuang.onblur = function() {
    n++;
    myh1.innerText = n;
```

 

* 得到表单的值

```js
// 得到元素
var btn = document.querySelector('#btn');
var kuang = document.querySelector('#kuang');
var list = document.querySelector('#list');

// 给按钮加监听
btn.onclick = function() {
    // 新知识点：文本框直接点儿value就是文本框的值。value这个词就是值的意思。
    // 这条语句一定要写在btn点击事件中，因为是用户点击按钮那一下子读值！！
    var content = kuang.value;
    
    // 创建新li标签。创建出来的是孤儿。
    var li = document.createElement('li');
    // 设置li的内容
    li.innerText = content;
    // 上树
    list.appendChild(li);

    // 让kuang的value清空
    kuang.value = '';
};
```

### 事件传播

#### 捕获阶段和冒泡阶段

实际上，事件的传播是：先从外到内，然后再从内到外

#### onclick方法

DOM0级：onclick，只能监听冒泡阶段

```js
box.onclick = function () {
};
```

#### addEventListener()方法

DOM2级：addEventListener，可以自由选择监听哪个阶段

```js
oBox.addEventListener('click', function () {
// 这是事件处理函数
}, true);
//true捕获，false冒泡
```



* 小知识点1：最内部元素不再区分捕获和冒泡阶段

* 小知识点2：同名事件DOM0级覆盖，DOM2级顺序执行

  * 如果给元素设置相同的两个或多个同名事件，则DOM0级写法后面写的会覆盖先写的；而D OM2级会按顺序执行

    ```js
    oBox2.onclick = function () {
    alert('A');
    };
    oBox2.onclick = function () {
    alert('B');
    };
    oBox2.addEventListener('click', function() {
    alert('C');
    }, false);
    oBox2.addEventListener('click', function() {
    alert('D');
    }, false);
    //弹出顺序：B→C→D	A被B覆盖，不会弹出
    ```

### 事件委托

#### *什么是事件委托呢？？*

*就是利用事件冒泡的机制，监听大盒子，而不是监听1000个按钮。因为你点击按钮的时候，事件会冒泡到大盒子上。通过e.target即可知道你点击的是具体哪个按钮。这样一来，就没有1000个事件监听了，不用写循环语句了。页面效率陡然增加。*

利用事件冒泡机制，将后代元素事件委托给祖先元素。

```js
var box = document.getElementById('box');

// 监听大盒子的点击事件。这里监听的是冒泡阶段，因为onclick就是监听冒泡阶段的。
box.onclick = function (e) {
    // e.target表示触发事件的那个元素
    // nodeName表示触发事件的元素是什么标签
    // toLowerCase()表示变为小写字母
    if (e.target.nodeName.toLowerCase() == 'button') {
        e.target.style.backgroundColor = 'orange';
    }
};

// 点击图片，能产生新按钮
var pic = document.getElementById('pic');

pic.onclick = function() {
    var button = document.createElement('button');
    button.innerText = '我是新来的';
    b
```

#### e.target属性

事件委托通常需要结合使用e.target属性，表示触发此事件的最早元素，即“事件源元素”

#### ***事件委托的使用场景***

1. 当有大量类似元素（比如1000个按钮）需要批量添加事件监听时，使用事件委托可以减少内存开销；
2. 当有动态元素节点上树时，使用事件委托可以让新上树的元素具有事件监听

#### 注意事项

* onmouseenter和onmouseover都表示“鼠标进入”，它们有什么区别呢？答：onmouseenter不冒泡，onmouseover冒泡。
* 使用事件委托时要注意：不能委托不冒泡的事件给祖先元素

### 延迟运行

* 在操作DOM时，JS代码一定要写到HTML节点的**后面**，否则JS无法找到相应HTML节点，这也是**最佳实践（企业中就是这么用）**

* （小知识）如果JS代码就是要写在HTML**前**，则监听**window的onload事件**，当页面DOM都加载完毕后，再执行指定的代码

  ```html
  window.onload = function () {
  <script></script>
  };
  ```

## 移动Web

### 视口

手机不是在用自己的真实物理设备像素在渲染网页（否则16px的字、300px宽度的盒子，都贼小），而是谦虚低调的认为自己没有那么宽，这个谦虚低调的自己认为自己的宽度，就叫做“视口。

### 用meta标签设置视口

设置布局视口宽度为800px：

```html
<meta name="viewport" content="width=800px">
```

由于手机屏幕有大有小，比如iPhone13、iPhone13 mini、iPhone13 pro不一样大。所以都设置为相同的数，不靠谱。
怎么办，就把视口设置权利给手机厂商了。就在手机内置一个合适的视口宽度。称为device-width

------

[不允许用户用双指捏合更改视口](http://m.taobao.com)

```html
<meta name="viewport" content="width=device-width,initial-scale=1,minimum-scale=1,maximum-scale=1,user-scalable=no,viewport-fit=cover">
```

### 流式布局

#### 百分比

##### 使用百分比设置width

使网页实现弹性布局，最简单的方法就是使用百分数设置每个盒子的width。比如，设置盒子的width属性值为“33.33%”，这样它的宽度将成为父盒子宽度的三分之一。如果它没有父盒子，而是<body>的子元素，这个盒子的宽度将为屏幕宽度的三分之一。

```css
.s1 .box1{
    float: left;
    width: 30%;
    height: 100px;
    background-color: #ffeb3b;
}
.s1 .box2{
    float: left;
    width: 70%;
    height: 100px;
    background-color: #1565c0;
    color: white;
}
```

##### 盒子的边框不能使用百分比进行设置

**CSS规定**：盒子的边框不能使用百分比进行设置，比如下面的语句是错误的：`border: 1% solid red;`

**解决方法**：
① calc()
② box-sizing: border-box;

###### calc()

calc()功能类似JavaScript的函数，可以在圆括号中书写简单的表达式进行计算。这里的“calc(30% - 2px) ”表示将盒子的宽度设置为父盒子宽度的30%再减去2px。这样即可让盒子成功实现并排。

```css
erzi1 {
    float: left;
    width: calc(30% - 2px); //注意减号前后要加空格
    height: 100px;
    border: 1px solid black;
}
```

###### box-sizing属性

默认情况下，盒模型padding、border外扩
即，**width不含padding、borderz**

加上box-sizing: border-box;之后，那么padding、border内减
即，**width已含padding、border**

##### padding用百分比设置一律参考父亲的宽

无论是水平方向还是竖直方向的padding，都是相对于父元素的width值的，而不是height值。

```css
.box {
    width: 800px;
    height: 500px;
    border: 10px solid #000;
}
.box .erzi {
    width: 400px;
    height: 200px;
    background-color: orange;
    /* 注意，这个儿子盒子，设置了一个上padding为10% */
    /* 就要知道它是谁的10%。 */
    /* CSS做了一个特别诡异的规定：无论是上下左右哪个方向的padding，一律参考父亲的width。 */
    /* 即，这个padding-top是80px。 */
    padding-top: 10%;
}
```

#### flex

- 为父级添加`display:flex;`属性后，父盒子就是弹性盒容器，自己的子元素就能够自动并排了
- 所有的子元素就能够用flex:数字;来进行比例的分配了，俗称‘分份儿’
- 同时设置flex和width，flex权重高，width不生效
- **若子盒子若要两栏布局可以使用`margin-left:auto;`来操作**

##### 三神之一

所有子元素的padding、border、margin被减去后再将剩余空间按比例分给所有子元素，不需要calc、box-sizing属性

##### 三神之二

允许子元素不分配flex份数，而是定死宽高，其他子元素按比例分剩余宽度

##### 三神之三

- 父元素需同时设置`display:flex;`和`justify-content`属性
- 若要用justify-content，那么所有的子元素都不能用flex分份儿，一定都必须是用px定死宽高
- 交换主副轴时给父元素设置`flex-direction: column;`
- 设置副轴用`align-items`属性：默认居左，`center`居中,`flex-end`靠右
- 主轴逆序用`flex-direction:row-reverse;`
- **以上属性不支持伪类元素**

###### <img src="F:\Web前端\BOSS直聘课程\学习资料\学习笔记img\justify-content.png" alt="justify-content" style="zoom:100%;" />

#### rem

CSS3的新增rem单位，表示相对于根节点（即<html>标签）字号的倍数

```html
<html>  → 设置了font-size: 20px;
    <body>
    	<div></div> → 设置了width: 5rem;
    </body>
</html>
5rem就是html标签字号的5倍
盒子此时宽度为100px
```

##### 写JS驱动rem

```js
// 实现一个事儿：让html标签的字号，是屏幕此时宽度的1/10。
// 想清楚：屏幕的总宽度是10rem。除几，屏幕总宽度就是几rem。
// 当屏幕尺寸改变的时候
window.onresize = function() {
    document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';
};
// 页面打开那一瞬间，也设一下
document.documentElement.style.fontSize = document.documentElement.clientWidth / 10 + 'px';
```

##### 媒体查询驱动rem

```css
@media screen and (min-width: 320px) {
    html {
    font-size: 21.33px
    }
}
@media screen and (min-width: 360px) {
    html {
    font-size: 24px
    }
}
@media screen and (min-width: 375px) {
    html {
    font-size: 25px
    }
}
@media screen and (min-width: 384px) {
    html {
    font-size: 25.6px
    }
}
//@表示设置
```

**什么叫驱动rem？？**
**答**：我们说，必须让<html>标签的字号能够实时和浏览器宽度等比例变化。浏览器变宽，那么<html>的字号要变大；浏览器变窄，那么<html>的字号要变小。我们在课间之前，学习了用JS驱动rem。就是用js让<html>标签的字号能够实时和浏览器宽度等比例变化。

#### 什么时候用rem？什么时候用flex

- 当需要等比例高度变化的时候，用rem，别无他选。
- 布局，用flex。
- 同一宽度下若要用rem则必须都要用rem

#### 认识DPR

DPR (Device Pixel Ratio) 是：𝐷𝑃𝑅 = 设备物理像素/加上meta之后它自己认为自己的宽度(*使用window.devicePixelRatio可以得到
设备的DPR值*)

- CSS一律基于逻辑像素
- 写CSS时不需要关心DPR、不需关心逻辑像素和物理像素的转换，备会帮你处理

### [不允许用户缩放页面](https://www.cnblogs.com/xiaoyaoxingchen/p/10519513.html)

```js
window.onload = function () {
            document.addEventListener('touchstart', function (event) {
                if (event.touches.length > 1) {
                    event.preventDefault();
                }
            });
            var lastTouchEnd = 0;
            document.addEventListener('touchend', function (event) {
                var now = (new Date()).getTime();
                if (now - lastTouchEnd <= 300) {
                    event.preventDefault();
                }
                lastTouchEnd = now;
            }, false);
            document.addEventListener('gesturestart', function (event) {
                event.preventDefault();
            });
        }
```



## JQuery快速学习

### JQuery简介

jQuery是一个DOM库，极大简化了对DOM的操作。

```html
<script src="3.6.0.jquery.min.js" ></script>	//引用jQuery库
```



### 认识$()函数和jQuery对象

* $('选择器')可以选择元素，得到jQuery对象。选择器支持所有CSS2.1、3选择器。
* jQuery对象并不是原生DOM对象，而是蕴含了很多DOM对象。用[0]、[1]、[2]等枚举它内部的项，就得到了原生DOM对象。即，jQuery对象是一个[类数组对象 - 知乎 ](https://zhuanlan.zhihu.com/p/50146642)。
* jQuery对象能够调用jQuery对象的方法，比如.text()、.css()，这些操作都是批量的，不需要写循环语句；原生DOM对象能调用原生DOM对象的属性，比.innerText、.style.color等，如果要批量，必须自己写循环语句;
* jQuery对象可以和DOM对象相互转化：
* 

### 节点操作

### 节点关系

### 类名操作

### 事件监听

### 常用快捷动画

### 自定义动画 



## ESNext

### ESNext是什么？

ES6/7/8/9···新特性统称ESNext

### 手册

•[阮一峰ES6入门教程](https://es6.ruanyifeng.com/)

•[MDN检索](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript/Referenc) 

### let 和 const

#### let用来定义作用域变量

复习一波：**var是定义函数级作用域变量**

```js
function fun() {
    var a = 10;
}

fun();
console.log(a);     // 报错
```



今天我们学习一个东西，叫做`let`。let定义的是“块级作用域”变量。

```js
// let能够定义变量。
let a = 10;
console.log(a);  // 10
```



**定义的是“块级作用域”变量**。大括号就是块。

```
{
	let a = 10;
}
console.log(a);     // 报错
```



**除了{}之外，if判断、switch判断、for循环、while循环、函数都是块。**

```js
if (8 > 3) {
    let a = 10
}
console.log(a);     // 报错
```

因为if语句是块。所以8 > 3成立，但是a出不来啊！a被限制在{}里面了。

但是记住，var能够出{}

```js
if (8 > 3) {
    var a = 10
}
console.log(a);     // 输出10。因为var能够走出{}。var走不出函数。
```



**函数也是块，**因为函数有一个{}

```js
function fun() {
	let a = 10;
}
fun();
console.log(a);     // 报错。a被限制在函数{}中了
```



#### let没有变量声明提升

```js
console.log(m);		// 报错
let m = 9;
```



#### let有暂时性死区

暂时性死区（TDZ）：只要是在{}中你let了一个变量，那么这个变量就绑死了这个块级作用域。这个变量不能在let之前使用。即便外部有更大作用域的变量。

```js
let a = 3;
{
    console.log(a);		// 报错。因为不能在定义前使用变量。
    let a = 8;
}
```

老师给你一个特别简单、老百姓能看懂的理解：**不能在定义前使用变量**。

其实就是变量没有提升，是一回事。



#### let不能重复定义变量

```js
let a = 3;
let a = 4;		// 报错
```



#### const 定义常量

const用来定义常量，一旦定义，值不能改。

```js
const a = 9;        // 一旦被定义不能改
console.log(a);     // 9
console.log(a + 8); // 17

a = 18;     // 报错，因为a是常量
a++;        // 报错，因为a是常量
```



它的所有性质，和let一样：

- const也是块级{}作用域
- const没有变量声明提升
- const有暂时性死区
- const也不能重复定义变量

```js
{
    const a = 3;
}
console.log(a);     //报错。const也是块级作用域。
```



#### for循环用let，出奇的好用！

比如页面上有10个按钮，现在用for循环添加监听：

```js
// 得到按钮数组
var buttons = document.querySelectorAll('button');
for(var i = 0; i < buttons.length; i++) {
    buttons[i].onclick = function() {
        alert(i);
    };
}
```

点击任何一个按钮，都弹出10。

这是因为，i是全局变量。内存中只有一个i，它的值被循环语句改为了0、1、2、……10。所以，点击任何按钮，都是去内存中使用这唯一的i，都弹出10。

![image-20220226151534675](assets/image-20220226151534675.png)



解决方法就是for循环的这个循环变量，用i来定义。JS规定，这个i将是每次循环、每次迭代时，那个大括号中的局部块级作用域变量。就是说，i=0时，在{}中创建了一个块级作用域的i，是0；i=1时，在{}中创建了一个块级作用域的i，是1；i=2时，在{}中创建了一个块级作用域的i，是2；……不冲突，不共用。

```js
// 得到按钮数组
var buttons = document.querySelectorAll('button');
for (let i = 0; i < buttons.length; i++) {
    buttons[i].onclick = function () {
        alert(i);
    };
}
```

效果就是点谁，弹谁。

![image-20220226151512990](assets/image-20220226151512990.png)

#### 小知识：let、const定义的变量/常量，不是window的属性

var定义的全局变量，是window的属性

let、const不是







### 箭头函数

#### 复习一波传统函数

函数是语句的封装

```js
function fun() {
    console.log('哈哈哈');
}
fun();
```



可能有参数、返回值

```js
function sum(a, b) {
    return a + b;
}
let a = sum(3, 4);
console.log(a);
```



#### 函数，今天有了新的写法

JS现在有了“箭头函数”，箭头是两个符号，是等号和大于号组成的，`>=`。

```js
const fun = () => {
    console.log('哈哈哈哈哈哈');
};

fun();		// 输出'哈哈哈哈哈哈'
```



圆括号中，用来写形式参数

```js
const fun = (a, b) => {
    console.log('我收到了' + a + '和' + b);
};
fun(6, 9);
```

![image-20220226153555232](assets/image-20220226153555232.png)



如果只有一个参数，那么圆括号可以省略。如果参数是2个、3个……就不能省略()。

```js
const fun = a => {
    console.log('我收到了' + a);
};
fun(3);
```

![image-20220226153704561](assets/image-20220226153704561.png)





箭头函数的返回值，同样用return来，没毛病。返回值就是函数吐出来的东西。

```js
const fun = (a, b) => {
    return a + b;
};
let result = fun(3, 4);
console.log(result);
```

![image-20220226153940831](assets/image-20220226153940831.png)



**如果箭头函数只有一条语句，并且这一条语句就是return语句**（比如上例），那么箭头函数将达到最美的写法。它可以省略大括号、省略return、省略换行。

```js
const sum = (a, b) => a + b;
```

sum函数太美了！！表示接受a、b，返回a + b的值。



箭头函数能够达到单行、最美状态，挺不容易的。如果函数贼复杂，还是要写全：

```js
const qiuhe = arr => {
    let sum = 0;
    for (let i = 0; i < arr.length; i++) {
        sum += arr[i];
    }
    return sum;
};
console.log(qiuhe([4, 5, 6]));		// 15
```

qiuhe的功能是计算数组的和。

###### 

#### 欣赏几个，美丽的单行箭头函数

##### 翻倍：

```js
let double = a => 2 * a;

console.log(double(4));
console.log(double(9));
```

![image-20220226154725748](assets/image-20220226154725748.png)



##### 返回大的：

```js
let da = (a, b) => a > b ? a : b;

console.log(da(3, 4));      // 4
console.log(da(4, 8));      // 8
console.log(da(8, 4));      // 8
```



##### 计算圆的面积：

```js
const size = r => 3.14 * r * r;

console.log(size(3));   // 28.259999999999998
```



##### 字符串逆序：

```js
const fan = str => str.split('').reverse().join('');

console.log(fan('我爱你'));     // 你爱我
```



所以记住，如果函数只有一条语句，并且这条语句就是返回值，那么可以写成最美单行。





#### 箭头函数不是运行时上下文，而是定义时上下文

复习一波，之前学习的function函数，它的上下文由如何调用决定，而不是如何定义。

```js
var obj = {
    a: 10,
    fun: function () {
        console.log(this.a);
    }
};

var a = 8;
var f = obj.fun;
f();		// 输出8。因为函数是“规则1”那种调用，上下文是window。
```



注意，之前学习的规则1、规则2、规则3、规则4、规则5、规则6，在箭头函数中，全不适用。



<mark style="color: red">箭头函数不管你如何调用，而是看定义时，所处的大环境！</mark>



我们直接看一个例子：

```js
var obj1 = {
    a: 10,
    fun: () => {
        console.log(this.a);
    }
};
```

我们说箭头函数的this，要看箭头函数定义时所处的大环境。

**这个箭头函数，外围没有任何的function，所以这样的箭头函数内部的this，一定等于window。**初学者，会错误的认为，箭头函数是定义在obj1中的，所以this是obj1。这是错误的！

并且，我们没有任何办法，改变它的上下文。简称：海枯石烂。

**箭头函数的上下文，具有不可变性。**

```js
const arr = [3, 4, () => {
    console.log(this);
}];

arr[2]();       // window。因为箭头函数定义的时候，外围没有function，这样的箭头函数，我们规定this永远是window。
```



```js
var a = {
    m: 3,
    b: {
        m: 4,
        c: {
            m: 5,
            d: {
                m: 6,
                fun: () => {
                    console.log(this.m);
                }
            }
        }
    }
};
var m = 1;
a.b.c.d.fun();		// 输出1，因为箭头函数定义的时候，外围没有function，这样的箭头函数，我们规定this永远是window。
```



重点看看这道题：

```js
// 你看，这里有一个outer函数。这个outer函数被
// outer.call(obj2)调用了，所以outer函数里面的上下文是obj2。
// 箭头函数，就出生在outer里面。所以箭头函数的“大环境”就是obj2。
function outer() {
    var obj1 = {
        a: 3,
        fun: () => {
            console.log(this.a);
        }
    };

    // 你用obj1调用箭头函数，没用！！
    // 因为箭头函数的上下文，由出生时候的大环境定义，而不是调用形式。
    // 并且，不可变。海枯石烂！
    obj1.fun();

    // 我们尝试提出来，然后用规则1调用，对不起没用！！！
    // 因为箭头函数的上下文，由出生时候的大环境定义，而不是调用形式！！！
    // 并且，不可变。海枯石烂！！！！！！！
    var f = obj1.fun;
    f();
}


var obj2 = {
    a: 2
};
outer.call(obj2);
```

![image-20220226162812397](assets/image-20220226162812397.png)

outer运行时，上下文是obj2。所以箭头函数的“大环境”就是obj2，箭头函数的this终身不变，是obj2。



#### 箭头函数不能当做构造函数，即，箭头函数不能被new调用

```
const fun = () => {};

new fun();	// 报错给你看
```

![image-20220226162440715](assets/image-20220226162440715.png)

### 数组的新方法
之前学习过的数组的方法：push、pop、shift、unshift、splice、slice、reverse、join



#### map方法
##### map表示映射

```js
var arr1 = [3, 4, 9, 2];
// map表示映射。数组中的每一项都将根据我们制定的方案，进行一一映射，产生一个新数组。
// 映射的方案，要写在map的参数中，map的参数是一个函数。
// 产生的新数组，一定和原数组长度相同。因为它是一一映射的。
var arr2 = arr1.map(function(item) {
    return item * 2;
});

console.log(arr2);      // [6, 8, 18, 4]
```



map通常里面的函数，都是单行的、直接就是return语句的，所以可以改为箭头函数，并且是单行箭头函数，最美的形态：

```js
var arr1 = [3, 4, 9, 2];
var arr2 = arr1.map(item => item * 2);
console.log(arr2);      // [6, 8, 18, 4]
```



##### 多举几个例子

**取整每一项：**

```js
var arr1 = [3.6, 4.7, 5.9, 6.6];
var arr2 = arr1.map(item => parseInt(item));
console.log(arr2);      // [3, 4, 5, 6]
```



**让数组中的每一项，变为“202X年”:**

```js
var arr1 = [3, 4, 5, 6];
var arr2 = arr1.map(item => (2020 + item) + '年');
console.log(arr2);		
```

![image-20220227143357793](assets/image-20220227143357793.png)



**克隆原数组：**

```
var arr1 = ['虎', '虎', '虎', '虎', '虎', '虎'];
var arr2 = arr1.map(item => item);
console.log(arr2);
```

![image-20220227143403476](assets/image-20220227143403476.png)



**将数组中的“狗”变“牛”：**

```js
var arr1 = ['虎', '狗', '虎', '狗', '虎', '虎'];
var arr2 = arr1.map(item => item == '狗' ? '牛' : item);
console.log(arr2);
```

map参数这个箭头函数，表示将item映射成什么呢？？要看三元运算符的结果。

就是说，item如果是狗，就变为牛；如果不是狗，就不变。

![image-20220227143728364](assets/image-20220227143728364.png)



##### map有改项的能力

<mark>现在，你就发现了，map有一种能力，将数组中的某些复合条件的项，进行替换。</mark>

改项的能力是通过三元运算符体现的！



比如，把数组中的所有B变为X：

```js
var arr1 = ['A', 'B', 'C', 'B', 'C', 'A', 'B', 'C'];
// 可以将数组中的所有B变为X。
var arr2 = arr1.map(item => item == 'B' ? 'X' : item);
console.log(arr2);
```

![image-20220227144051389](assets/image-20220227144051389.png)





#### filter方法

##### filter表示过滤

```js
var arr1 = [3, 4, 9, 2, 6, 10];
// filter表示过滤，顾名思义，就是从原数组中挑选一些项，进入新数组
// 挑选策略用函数来表示。
// 只有函数的返回值是true的，才被挑选进入新数组。
// 得到的新数组的长度，一定小于等于原数组。
var arr2 = arr1.filter(item => item % 2 == 0);
console.log(arr2);      //  [4, 2, 6, 10]
```



##### 多举几个例子

筛查大于100的数字

```js
var arr1 = [140, 55, 60, 120, 133];
var arr2 = arr1.filter(item => item > 100);
console.log(arr2);  // [140, 120, 133]
```



都留下来了：

```js
var arr1 = [140, 55, 60, 120, 133];
var arr2 = arr1.filter(item => true);
console.log(arr2);
```



##### filter有删除项的能力

比如，删除数组中所有的狗：

```js
var arr1 = ['虎', '狗', '虎', '狗', '兔', '牛'];
var arr2 = arr1.filter(item => item != '狗');
console.log(arr2);  // ['虎', '虎', '兔', '牛']
```

![image-20220227150114879](assets/image-20220227150114879.png)

怎么理解呢？？就是要给所有的动物发true通行证。false表示拒绝证。

什么样的动物能发true通行证呢？？不是狗的。





再比如，删除数组中所有的B：

```js
var arr1 = ['A', 'B', 'B', 'C', 'A', 'B'];
// 现在我想删除数组中所有的B
var arr2 = arr1.filter(item => item != 'B');
console.log(arr2);      // ['A', 'C', 'A']
```



```js
var arr1 = [
    { id: 1, name: '小明', age: 12, sex: '男' },
    { id: 2, name: '小红', age: 11, sex: '女' },
    { id: 3, name: '小绿', age: 13, sex: '女' }
];
// 现在想删除id为2的小红
var arr2 = arr1.filter(item => item.id != 2);

console.log(arr2);
```



![image-20220227150623285](assets/image-20220227150623285.png)



<mark>以后题目是删除数组中的某个东西，那么，直接用filter即可！绝对不要用splice了。</mark>



比如，原来想删除D，用的是splice：

```js
var arr1 = ['A', 'B', 'C', 'D', 'E', 'F'];
arr1.splice(3, 1);		// 下标为3的项开始，删除1项
console.log(arr1);		// ['A', 'B', 'C', 'E', 'F']
```



今天，不要用splice了，splice这个词语，终身不打了！！一律用filter代替！！

工作也是一样的！！

```js
var arr1 = ['A', 'B', 'C', 'D', 'E', 'F'];
var arr2 = arr1.filter((item, index) => index != 3);
console.log(arr2);      //  ['A', 'B', 'C', 'E', 'F']
```



```js
var arr1 = ['A', 'B', 'C', 'D', 'E', 'F'];
var arr2 = arr1.filter(item => index != 'D');
console.log(arr2);      //  ['A', 'B', 'C', 'E', 'F']
```



##### 总结：删filter改map

- 你想删除项，用filter，肯定有一个`!=`符号
- 你想改变项，用map，肯定有一个三元运算符



课间练习这个题目：

题目1： 请将数组中所有的B变为X：

```js
var arr1 = ['A', 'B', 'B', 'C'];
var arr2 = arr1.map(item => item == 'B' ? 'X' : item);
console.log(arr2);
```



题目2： 请将数组中所有的B删除：

['A', 'B', 'B', 'C']

```js
var arr1 = ['A', 'B', 'B', 'C'];
var arr2 = arr1.filter(item => item != 'B');
console.log(arr2);
```



#### reduce方法

##### reduce表示数组中所有项参与，最后得出一个数字结论

```js
// 刚才学习的map是得到一个新数组；
// 刚才学习的filter也是得到一个新数组；
// reduce得到一个数字。

// 比如下面这个例子，进行了数组求和
var arr1 = [1, 3, 2, 1];
var result = arr1.reduce((a, b) => a + b);
console.log(result);      // 7
```

宏观的看，就是把数组中4个数字，减少成为了1个数字。



##### reduce的运作机理 - reduce就是传纸片儿

reduce就是班主任老师，让“传纸片儿”



![image-20220227154210790](assets/image-20220227154210790.png)





![image-20220227154931324](assets/image-20220227154931324.png)



##### reduce使用举例

reduce颠覆了我们之前的一些算法

**数组求和**

```js
var sum = arr.reduce((a, b) => a + b);
```



**数组最大值**

```js
var max = arr.reduce((a, b) => b > a ? b : a);
```



特别的，如果数组中是对象，我们相对某个属性进行求和，那么就要加一个”,0“，还要注意”.money"

```js
var arr1 = [
    {'name': '小明', age: 12, money: 3},
    {'name': '小红', age: 11, money: 1},
    {'name': '小强', age: 13, money: 2},
    {'name': '小绿', age: 10, money: 3}
];

// 注意，如果数组中是对象，那么就要加一个“,0"，表示小纸片上的默认值是0。然后要注意，每位同学改把自己的money加上去，所以要“.money”就行。
var result = arr1.reduce((a, b) => a + b.money, 0);

console.log(result);
```



#### forEach方法

##### forEach表示遍历每一项

- map得到一个新数组，新数组长度一定等于原数组，因为是映射呀
- filter得到一个新数组，新数组长度一定小于等于原数组，因为是过滤呀
- reduce得到一个数字，因为是传纸片
- forEach啥也得不到，纯遍历的意思



```js
var arr = [1, 3, 4, 2];

// forEach表示遍历数组中的每一项，每一项会依次成为item
arr.forEach(item => {
	console.log(item);
});
```



![image-20220227160705379](assets/image-20220227160705379.png)



以后如果想遍历数组，那么就可以写forEach，不用写for循环了。即：

```js
for (let i = 0; i < arr.length; i++) {
	// 使用arr[i]
}
```

变为：

```js
arr.forEach(item => {
	console.log(item);
});
```



### ESNext中的零散语法糖

#### 接收对象中的属性值 （非常有用）

```js
var obj = {
    a: 6,
    b: 8
};

// 我们现在要定义两个变量：a和b
// 将obj的a属性存入a变量，b属性存入b变量
var {a, b} = obj;

console.log(a);     // 6
console.log(b);     // 8
```

Ajax课程你就知道了，obj可能是服务端返回的数据对象，我们用{}进行拆。



#### 接收数组的值

```js
var [a, b, c] = [11, 33, 22];

console.log(b);     // 33
```



#### kv一致省略v

比如，我们现在让obj的a属性值就是a变量、b属性值就是b变量、c属性值就是c变量。

原来这样写：

```js
var a = 3;
var b = 5;
var c = 9;

var obj = {
    a: a,
    b: b,
    c: c
};

console.log(obj);
```

![image-20220227161634268](assets/image-20220227161634268.png)



现在：

```js
var a = 3;
var b = 5;
var c = 9;

// k-v一致省略v
var obj = {
    a,
    b,
    c
};

console.log(obj);
```

![image-20220227161809723](assets/image-20220227161809723.png)



#### 方法的简写

在对象中，如果有一个属性值是函数，这个函数被称为“方法”。

现在，方法可以不写“:function”了

比如：

```js
var obj = {
    a: 3,
    fun() {
        console.log(this.a);
    }
};

obj.fun();
```

等价于：

```js
var obj = {
    a: 3,
    fun: function() {
        console.log(this.a);
    }
};

obj.fun();
```

注意，省略的是function，而不是箭头！



#### 解构

点点点运算符表示“解构”，解除它的结构。将数组打开、打散。

```js
var arr1 = [3, 4, 5, 6];

// 点点点表示将arr1“打开”、“打散”放到新数组中
var arr2 = [1, 2, ...arr1, 7, 8];

console.log(arr2);      // [1, 2, 3, 4, 5, 6, 7, 8]
```

![image-20220227162614018](./assets/image-20220227162614018.png)



对象也可以解构：

```js
var obj1 = {
    a: 1,
    b: 2,
    c: 3
};

var obj2 = {
    ...obj1,
    d: 4,
};

console.log(obj2);
```

![image-20220227162802454](assets/image-20220227162802454.png)

## 面向对象





## flex高级特性

### flex子项的性质

1. 能设置宽高，不设置默认收缩
2. 子元素间margin不再塌陷
3. 浮动失效（float属性无效）
4. z-index属性可以使用
5. 绝对定位会自动脱离弹性布局，不会分份数

### [flex的CSS属性](https://developer.mozilla.org/zh-CN/docs/Web/CSS/flex-direction)

````css
;//flex-direction:column;			//改变主轴方向为向下
flex-direction:column-reverse;	 //改变主轴方向为向上
flex-direction:row;				//主轴方向为默认向右
flex-direction:row-reverse;		 //主轴方向为向左


flex-wrap:nowrap;	//默认不换行
flex-wrap:wrap;		//换行

flex-flow:column wrap;//以上两个属性合并

justify-content:flex-start;//主轴靠头
justify-content:flex-end;//主轴靠尾
justify-content:center;//主轴居中
justify-content:space-between;//	子00子00子
justify-content:space-around;//		0子00子0
justify-content:space-evenly;//		0子0子0

align-items:stretch;//副轴默认拉伸铺满
align-items:center;//副轴收缩居中
align-items:flex-start;//副轴靠头
align-items:flex-end;//副轴靠尾
align-items:baseline;//副轴靠头且底线平齐
align-self://给子元素使用

align-content:如下图
````

![image-20220501215625116](https://gitee.com/zqx153033/typora/raw/master/Typora-images/image-20220501214533811.png)

### grow/shrink/basis属性

`flex:grow shrink basis;`

1. 若子元素basis总和未超过父元素，则每个子元素宽度占比为各子元素的grow
2. 若子元素basis总和超过父元素，则每个子元素宽度为basis-(grow\*basis)/sum(grow\*basish)*溢出宽度
