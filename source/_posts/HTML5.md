---
title: HTML5
tags: ['web']
categories: ['笔记']
date: ['2019-03-15']
---
HTML是用来描述网页的语言，是一种标记语言。HTML5适用与2G内存双核处理器的计算机，对于Mac，Windows，Linux都可以用。
HTML的特性
1. 用于绘画的canvas标签
2. 用于媒介回放的video和audio元素
3. 对本地离线储存的更好支持
4. 新的内容元素  如：article，footer，header，nav,section.
5. 新的表单控件  如：calendar，date，time，email，URL
6. 支持IE，chrome
7. <!-- more -->
常用的开发工具
● Webstorm
● notepad
● eclipse
● tsxt sublime
● dreamweaver
● interllij  IDEA
# HTML元素
1.元素指的是从开始标签到结束标签的所有代码。

 ```html 
  <p>  开始标签
  this is my web page    元素内容
  </p>   结束标签
  <br/> 换行 
```

2.元素语法
元素的内容是开始标签与结束标签之间的内容，空元素在开始标签中进行关闭。（大多数HTML元素拥有属性）
3.嵌套的HTML元素 
大多数的HTML元素都可以嵌套使用
HTML标签
1.声明<!DOCTYPE  html>
2.标签
```html
<h1>    </h1>  标题
<p>    </p>   段落
<a>     </a>   链接
<img>   </img> 图像
<head>  </head> 基础标签
<body>  </body>
```
HTML属性
● 标签可以拥有属性为元素提供更多的信息
● 属性一键/值对的形式出现  如：
 `href="www.jikexueyuan.com"`

● 常用标签属性    <`h1>:align  对齐方式     <`body>:bgcolor  背景颜色 
<`a>:target 规定在何处打开连接
● 通用属性： class：规定元素的类名 `id`：规定元素唯一ID   
 style：规定元素的样式    title：规定元素的额外信息
 
# HTML格式化
```html
<b>        定义粗体字
<big>      定义大号字
<em>       定义着重文字
<i>        定义斜体字
<small>    定义小号字
<strong>   定义加重语气
<sub>      定义下标字
<sup>      定义上标字
<ins>      定义插入字
<del>      定义删除字
```
# HTML样式

1.标签  <`style>-样式定义      
<`link>-资源引用  
<`link rel="stylesheet"  type="test/css"  href="资源地址“>
2.属性
```html
- rel="stylesheet"  外部样式表
- type="test/css"  引入文档的类型
- margin-left ：边距
```
3.三种样式表插入方法
- 外部样式表：
- ```html
<link rel="stylesheet"  type="test/css"  href="资源地址“>
```
- 内部样式表
```html
<style type="text/css">
body{backgrond-color:red}
p{margin-left:20px}
</style>```
- 内联样式表
```html
<p style="color:red>
```
# HTML链接
1.链接数据   （文本链接和图片连接）
2.属性 
- href属性：指向另一个文档的链接        
- name属性：创建文档内的链接（回到顶部）
3.img标签属性   
-  alt：替换文本属性
-  width：宽
- height：高

# HTML表格

```html
<table cellpadding=”边距“  cellspacing="间距”  bgcolor="颜色“ >-定义表格
<caption>-表格标题
<th>-表头
<tr>-表格的一行
<td>-表格的单元
<thead>-页眉
<tbody>-主体
<tfoot>-页脚
<col>-列属性
```           
动手：
1. 没有边框的表格
2. 表格中的表头
3. 空单元格
4. 带有标题的表格
5. 表格内的标签
6. 单元格边距
7. 单元格间距
8. 表格内的背景，颜色和图像
9. 单元格内容排列
10. 跨行和跨列单元格S

# HTML列表
```html
<ol>  有序列表
<ul>  无序列表
<li>  列表项
<dl>  列表
<dt>  列表项
<dd>  描述
```
1.无序列表   
```html
- 使用标签 :<ul>  <li>
- 属性:  disc (实体圆)   circle（空心圆） square（实体方块）
- <`ul type="disc">
2.有序列表（默认是数字）
- 使用标签：<ol>  <li>
- 属性:  A  a I  i
- <ol  type="A">
3.嵌套列表
- 使用标签：<ul>  <ol>  <li>
3.自定义列表
- 使用标签：<dl>  <dt> <dd>
```

# HTML块
```html
1.HTML块元素 <！--   -->注释
块元素在显示时，通常会以新的行开始  如：<h1>  <p>  <ul>
2.HTML内联元素
      内联元素通常不会以新行开始  如：<b>  <a>  <img>
3.HTML<div>元素 配合CSS样式
      <div>元素也被称为块元素，其主要是组合HTML元素的容器
4.HTML<span>元素
     <span>元素是内联元素，可作为文本的容器
```
# HTML布局
```html
● 使用<div>元素布局
<title>div布局<title>
<style type="text/css">
body{
      margin:0px //去掉周围留白
           }
  div#container｛
                width：100%;//充满全屏
                height:950px;
                background-color:颜色;
                ｝
  div#heading{
                width：100%;
                height:10%;
                background-color:颜色;
                }
  div#content-menu{
                width：30%;
                height:80%;
                background-color:颜色;
                floot:left;
                }
   div#content-body{
                width：70%;
                height:80%;
                background-color:颜色;
                floot:left;
                } 
  div#content-footing{
                width：100%;
                height:10%;
                background-color:颜色;
                clear:both;//清除浮动
                }
  <body>
             <div  id="container">
             <div  id="heading">头部</div>
             <div  id="content-menu">内容菜单
             </div>
             <div  id="content-body">内容菜单
             </div>
             <div  id="footing">底部</div>
             </div>
  </body> 
            可以删除div
```
```html
● 使用<table>元素布局
<tabl>布局
<title>  table 布局 </title>
<body  marginheight ="0px" marginwidth="0px">
    <table  width="100%"  height="950px"  style="background-color:颜色”>
    <tr>
        <td colspan="3"  width="100%"  height"10%"  style="background-color:颜色“>这是头部
        </td>
    </tr>
    <tr>
        <td  width="20%"  height"80%"  style="background-color:颜色“></td>
        <td  width="60%"  height"80%"  style="background-color:颜色“></td>
        <td  width="20%"  height"80%"  style="background-color:颜色“></td>
    </tr>
    <tr>
        <td colspan="3"  width="100%"  height"10%"  style="background-color:颜色“>这是底部
        </td>
    </tr>
   </table>
```

# HTML表单
● 复选框
     
你喜欢的水果有？
```html
<br/>
苹果<input  type="checkbox">
香蕉<input  type="checkbox">
橘子<input  type="checkbox">
<!-- CheckBox 是检查框的意思-->
```

● 单选按钮
<br/>
请选择您的性别：
```html
男<input type="radio" name="sex">
女<input type="radio" name="sex">
<!-- radio为单元框  同时写name=“sex”是让两个单选框属于同一个组-->
```

● 下拉列表
请选择您常用的网站：
```html
<select>
    <option>www.taobao.com</option>
    <option>www.baidu.com</option>
    <option>www.goolge.com</option>
</select>  
```

● 文本域
```html
<textarea cols="30"  rows="30">请在此填写个人信息</textarea>
可以写在form以外
```

● 创建按钮
```html
<input type="button" value="按钮">
<input type="submit" value="确定">
submit是提交按钮，更改名字用value
```
常用的表单标签
```html
<form>      表单
<input>     输入域
<textare>   文本域
<label>     控制标签
<fieldset>  定义域
<legend>    域的标题
<select>    选择列表
<optgroup>  选项组
<option>    下拉列表中的选项
<button>    按钮
```
表单和PHP交互
```html
<form>
用户名<input type="text" name="">
密码< input type="possword"  name="possword">
   <input type="submit" value="提交">
   </form>
   ```
   name的提交方法有两种： 
   1.get提交方式用户名和密码都显示在地址中，但是有时候地址不适合太长，有的浏览器太长了会不能解析
   2.post则不显示，因此更安全

# HTML框架
1. 框架标签（frame）框架对于页面设计有着很大作用（已过时）
2. 框架集标签（<iframesets>）框架集标签定义如何将窗口分割成框架，每一行frameset定义一系列行或列，rows、cols的值规定了每行或每列占据屏幕的面积
3. 常用标签   noresize：固定框架大小   cols:列   rows：行
4. 内联框架
```html     
<iframe  sre="引入内容" framebode="边框值"   width=""    heigSht="">
</iframe>
```
改变引用内容
```html
<a  链接   target="self">在自己所在页面打开
<a  链接   target="blank">在新的页面打开
<a  链接   target="parent">在父级（承载页面）页面打开
<a  链接   target="top">在顶级页面打开
```
# HTML背景
● 背景标签  Background （背景图片）
● 背景颜色  bgcolor（背景颜色）
● 颜色是由一个十进制符号来定义，这个符号由红色，绿色，蓝色组成(RGB)
● 颜色最小值：0（#00）
● 颜色最大值：255（#FF）
● 红色：#FF0000
● 绿色：#00FF00
● 蓝色：#0000FF
  
XHTML简介
● XHTNL指的是可扩展超文本标记语言，所有浏览器都支持，为了代码的完整性和良好性
● 声明：规定了使用通用标记语言的网页语法
● 三种XHTML文档  STRICT(严格)，TRANSITNAL（过度）， FRAMESET（框架）
HTML5
解决了：web浏览器之间的兼容问题
            文档结构不够明确
            web应用程序的功能受到了限制

全局属性
    contentEditable    编辑
    flag                     
    designMode         
    hidden                  可见，不可见
    spellcheck             检查
    tabindex               获取焦点

# HTML5新增主体结构元素
1. article元素代表文档，文章，是独立使用的可以嵌套，表示插件
2. section元素用于对网站或者应用程序中页面上的内容进行分块。一个section元素通常由内容及其标题组成。但section元素并非一个普通容器元素，当一个容器需要被直接定义样式或通过脚本定义进行时，推荐使用div而非section。
3. nav元素是一个可以用作页面导航的链接组，其中的导航元素链接到其他页面或当前页面的其他部分。并不是所有的链接组都要被放进nav元素，只需将主要的，基本的链接组放进nav元素即可。 nav元素应用场景：传统导航条，侧边栏，页内，翻页。
4. aside 元素是用来表示当前页面或文章的附属信息部分，它可以包含与当前页面或主要内容相关的引用，侧边栏，广告，导航条，以及其他类似的有区别于主要内容部分。
5. time元素 pubdate属性
HTML5非主体结构元素
1. header 是一种具有引导和导航作用的结构元素，通常用来放置整个页面或页面内的一个内容区块的标题，但是也已包含其他内容，例如数据表单，搜索表单或者相关logo图片可以出现多次。
2. footer元素可以作为其上层父级内容区块或是一个根区块的脚注。footer通常包括其相关区块的脚注信息，如作者相关阅读链接及版权信息等。
3. hgroup元素是将标题及其子标题进行分组的元素，hgroup元素通常会将h1-h6元素进行分组，譬如一个内容区块的标题及其子元素一组。
4. address元素用来在文档中呈现维护者的名字，他们的网站链接，电子邮箱，真实地址，电话号码等。address应该不止用来呈现电子邮箱或真实的地址，还用来跟文档相关的联系人的所有联系信息。
5. 网页编排。
# HTML5属性

1. form属性  在HTML4中，表单的从属元素必须写在表单内部，而在HTML5中，可以把他们书写在页面上任何地方，然后为该元素制定一个form属性，属性值为该表单的ID，这样就可以声明该元素从属于指定表单了。
```html
<form  id="testform>
<article>  </article>
</form>
也可以表示为
<textares  form="testform">
</textares> 这样方便以后添加
```

1. formaction   在HTML4 中，一个表单内所有元素只能通过表单的action属性被统一提交到另一个页面，而在HTML5中，可以为所有的提交按钮，增加不同的formaction属性，使单机不同的按钮是可以将表单提交到不用的页面。
2. formmethod  在HTML4中，一个表单只能有一个action属性用来对表单内所有元素统一指定提交页面，所以每个表单页面只有一个method属性来统一指定提交方法。在HTML5中，可以使用formmethod属性对每一个表单元素分别指定不同的提交方法。
3. formenctype   在HTML4中，表单元素具有一个enctype属性，该属性用于指定在表单发送到服务器之前应该如何对表单内的数据进行编码。在HTML5中，可以使用formenctype属性对该表单元素分别进行不同的编码方式。 taxt/pain  mutipart/form-date   application/x-www-form-urlencoded
4. formtarget   在HTML4 中表单元素具有一个target属性，该属性用于指定在何处打开表单提交后所需加载的页面。在HTML5中，可以对多个提交按钮分别使用formtarget来指定提交后在何处打开所需加载页面。
5. autofocus   为文本框，选择框或按钮控件加上autofocus属性，当画面打开时，该控件自动获取光标焦点。
6. required     属性可以应用在大多数输入元素上，如果元素中内容为空白，则不允许提交，同时浏览器中显示信息提交文字。
7. labels属性，在HTML5 中，为所有可以使用标签的表单元素，button，select等。定义一个label属性，属性值为一个nodelist对象，代表该元素所绑定的标签元素所构成的集合。（验证）
8. control  在HTML5 中，可以在标签内部放置一个表单元素，并且通过该标签的lontrol属性来访问该表单元素
9. placeholder 是指当文本框处于未输入状态是显示输入提示，当文本框处于未输入状态且未获取光标焦点是模糊显示输入提示文字。
10. list  在HTML5中，为单行文本框增加一个list属性，该属性的值为某个datelist元素的ID。datelist元素也是HTML5中新增元素，该元素类似于选择框，但是当用户想要设定的值不在选择列表之内时，允许自动输入，datelist元素本身并不现实而是当文本框获得焦点是已提示输入的方式显示。
11. autolomplete 帮助输入所用的自动完成功能，是一个既节省输入时间又十分方便的功能。在HTML5之前，因为谁都能看见输入值，所以在安全方面存在缺陷，只要使用autocompelte属性，安全性方面也可以得到很好地控制。
12. pattern  在HTML5中，对input元素使用pattern并且将属性值设为某个格式的正则表达式，在提交时会针对这些进行检查，格式不合格则不允许提交，同时在浏览器中显示信息提示文字，提示输入的内容必须符合格式。
13. selection Direction  这对input元素与textarea元素，HTML5增加了selection Directiorl属性。当用户在这两个元素中用鼠标选取部分文字时，可以使用该属性来获取选取方向。当用户正向选取文字时，该属性值为“forward”当用户反向选取文字时，该属性值为“backward”当用户没有选取任何文字时，该属性值为“forward”。
14. indeterminate对于复选框chckbox元素来说，过去只是选取与非选取这两种状态。在HTML5 中，可以在JavaScript脚本代码中对该元素使用inderminate属性，以说明复选框处于尚未明确是都选取状态。
15. image  针对类型为image的input元素，HTML5新增了两个属性，height，width分别用来指定图片按钮的高度和宽度。

# 补充
块级元素和行内元素
区别：
块级元素会霸占一整行，不与其他任何元素并排，可以设置宽度和高度，但如果不设置宽度就会100%继承父级的宽度。
行内元素可以与其他元素并排排列，但是不能设置宽和高，默认的宽度就是文字的宽度。
分类：
   文本级标签：p , span , a , b , i , u , em
   容器级标签：div , h系列 , li , dt ,dd
   p：里面只能放文字和图片和表单元素，p里面不能放h和ul，也不能放p。
 从CSS的角度讲，CSS的分类和上面的很像，就p不一样：
   行内元素：除了p之外，所有的文本级标签，都是行内元素。p是个文本级标签，但是是个块级元素。
   块级元素：所有的容器级标签，都是块级元素，以及p标签。
相互转换：
 我们可以通过display属性将块级元素(比如div)和行内元素进行相互转换。
 display：inline;
 那么这个标签将变为行内元素，即：
   1，此时这个div将不能设置宽度和高度了。
   2，此时这个div可以和其他行内元素并排了。
 同样的到了我们也可以用display将行内元素(比如span)转行成块级元素。
 display：block；
 那么这个span标签将变为块级标签，即：
   1，此时这个span能够设置宽度，高度。
   2，此时这个span必须独占一行，其他元素无法与之并排。
   3，如果不设置宽度，将占满父级。
 
标准流里面的限制非常多，导致很多页面效果无法实现，如果我们现在就要并排，并且就要设置宽度，就hi有：脱离标准流。
CSS一共有三种手段，是一个元素脱离标准流文档：
浮动
绝对定位
固定定位
浮动：
 浮动是CSS里面布局最多的一个属性。
 float：表示浮动的意思。
属性：
none：表示不浮动，默认。
left：表示左浮动。
rigth：表示右浮动。
例子
我们会发现，三个元素并排显示，.box1和span因为是左浮动，所有紧挨在一起，这种现象是贴边现象。
.box2盒子因为是右浮动，所以紧靠着右边。
浮动的四大特性：
 1，浮动的的元素脱标，
 2，浮动的元素互相贴靠。
 3，浮动的元素由"子围"效果。
 4，收缩的效果。
浮动元素的脱标：
 脱标：就是脱离了标准文档流。