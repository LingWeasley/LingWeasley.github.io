---
title: CSS3-（1）
tags: ['web']
categories: ['笔记']
date: ['2019-03-20']
---
# 介绍
CSS指层叠样式表。层叠样式表极大地提高了工作效率。
# CSS基础语法

```css
selector {
    property：value
}
h1 {
    color:red;
    font-size:14px;
} 
```
<!-- more -->
属性大于1个之后，属性之间用分号隔开，写完用分号结尾
如果值大于1个单词，则需要加上引号：

```css
p {
    font-family:"sans serif"
}
```

# CSS高级语法
1. 选择器分组
     h1,h2,h3,h4,h5,h6{color：red}  给多个元素加标签
2. 继承（如果有单独的定义样式，则会用单独定义的；如果没有单独定义，则会引用body里的样式）
```css
body{
    color:blue;
}
```
   
# CSS派生选择器
通过依据元素在其位置的上下文关系来定义样式。strong加粗 
```html
<html >
<body ><strong >
    <p ><strong >标签hello css</strong ></p >
    <ul >
    <li ><strong >li标签：hello css</strong ></li >
    </ul >
    </strong ></body >
</html >
```
要求只在li strong 标签的文字加样式，其他的不加样式
用派生选择器 
```css
css
  li  strong{
          color:red;
          }
          ```
此时就只有li  strong里的文字加了样式
 如果派生strong{color：blue}时，已经加过样式的li strong 不会覆盖，只有 p  strong更改了样式

# CSS id选择器
1. ID选择器可以为标有ID的HTML元素指定特定的样式  ID选择器用"#"来定义
2.ID选择器和派生选择器:目前比较常用的方式ID选择器常常用于建立派生选择器
 ```html
<html >
<body >
  <p  id="pid" >hello css<a  href="http://www/jikexuanyuan.com" >学院</a ></p >
  <div id="divid" >这是一个div标签</div >
</body >
</html >
```
CSS
```css
#p a{ color:red}  <!-- id选择器和派生选择器同时用-- >
#divid{color:blue}
```
# CSS类选择器
1.类选择器以一个点显示
2.class也可以用作派生选择器
```html
 <html >
<head ></head >
<body >
<p class="pclass" >这是一个class效果 <a href="www.jikexueyuan.com >极客学院</a ></p >
<div class="divclass" >hello<p >标签</p ></div >
</body ></html >
```
CSS样式表
.pclass a{ color:red}
.divclass p{color:green}  类选择器和派生选择器的结合应用

# CSS属性选择器
1.对带有指定属性的HTML元素设置样式
2.属性和值选择器

```html
<html >
<head><meta charset="UTF-8" >
      <title ></title >
      <stype type="test/css" >
      [title]{               <!--如果属性选择器不指定值是多少，那么写任何值都生效-- >
           color:blue;}
      [title=te]{             <!--如果属性选择器指定值是什么，那么只有写指定的值才会生效，更改值则不生效-- >
           color:red
           }
      </stype` ></head >
<body >
<p title="t"` >属性选择器</p >
<p title="te"` >属性和值选择器</p >
</body >
</html >
```

属性选择器在IE6或者更低的版本是不支持的

# CSS3样式
## CSS背景
1.css允许应用纯色作为背景，也允许使用背景图像创建相当复杂的效果
   background-attachment         背景图像是否固定或者随着页面的其余部分滚动
   background-color                  设置元素的背景颜色
   background-image                 把图片设置为背景
   background-position              设置背景图片的起始位置
   background-repeat                 设置背景图片是否及如何重复
   background-size                     规定背景图片的尺寸
   background-origin                  规定背景图片的定位区域
   background-clip                      对顶背景的绘制区域
```html  
<html >
<head` ><meta charset="UTF-8" >
      <title` ></title >
      <link  rel="stylesheet" type="test/css" href="style.css" >
<body >
      <p` >测试一下背景是否可以继承</p >
</body >
</html >
```
先找一张背景图片
```css
style.css
body{
    background:gray;}
 p{  width:150px;
     padding:10px; <!--内边距-- >
    background:blue;}
<!--引入背景图片-- >
  body{
    background-image:url("图片名字"); <!--引入背景图片-- >
    background-repeat：no-repeat;<!--背景图片不允许重复-- >
    background-attachment:fixed;<!--背景图片固定不随文字而滚动-- >
    background-size：100px 100px;<!--裁定大小-- >
    }
  p{    width:200px;                   <!--把图片应用到p标签上-- >  
  background-image:url（"图片名字"）}
```


## CSS文本
CSS文本属性可定义文本外观，通过文本属性，可以改变文本的颜色，字符间距，对齐文本，装饰文本，对文本缩进等。
 color                       文本颜色
dlirection                  文本方向
line-height                行高
letter-spacing            字符间距
text-align                   对齐元素中的文本
text-decoration           向文本添加修饰
text-indent                 缩进元素中文本的首行
text-transform             规范元素中的字母的格式
unicode-bidi                设置文本方向
white-space                 元素中空白的处理方式
word-spacing               字间距
text-shadow                 向文本添加阴影
word-wrap                    规定文本的换行规则


例如
```html
<!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >Title</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
    <p >hello 狗哥</p >
</body >
</html >

style.css
body{
    color:orangered;
    text-align: right;
}
```
## CSS字体
css字体属性定义文本的字体系列，大小，加粗，风格和变形
font-family                设置字体系列
font-size                    设置字体的尺寸
font-style                   设置字体风格
font-variant                以小型大写字体或正常字体显示文本
font-weight                设置字体的粗细
```css
style.css<`!--引用字体--` >
@font-face{
  font-family:mafont;
  src:url(当前下载好的字体);
}
```

## CSS链接

● a:link      普通的，未被访问的链接
● a:visited  用户已访问的链接
● a:hover   鼠标指针位于链接的上方
● a:active   链接被点击的时刻
```css
 a:link{
    color: #FF0000;
}
a:visited{
    color: #00FF00;
}
a:hover{
    color: #0000FF;
}
a:active{
    color: #0F0F00;
}
```
## CSS列表
css列表属性允许你放置，改变列表标志，或者将图像作为列表项标志
list-style                      简写列表项
list-style-image            列表项图像
list-style-position         列表标志位置
list-style-type               列表类型
例如
```html
<!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >Title</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
     <ul >
         <li >苹果</li >
         <li >苹果</li >
         <li >苹果</li >
         <li >苹果</li >
     </ul >
</body >
</html >
ul li{
    list-style-type:decimal;
}
```
class是可以重复的（姓名），ID是不可以重复的
## CSS表格
css表格属性可以帮助我们极大地改善表格的外观

1. 表格边框
2. 折叠边框
3. 表格宽高
4. 表格文本对齐
5. 表格内边距
6. 表格颜色
```html
 <body >
     <table  id="tb" >
         <tr >
             <th >姓名</th >
             <th >年龄</th >
             <th >性别</th >
         </tr >
         <tr >
             <td >小王</td >
             <td >20</td >
             <td >男</td >
         </tr >
             <td >小王</td >
             <td >20</td >
             <td >男</td >
         </tr >
             <td >小王</td >
             <td >20</td >
             <td >男</td >
         </tr >
             <td >小王</td >
             <td >20</td >
             <td >男</td >
         </tr >
     </table >
</body >
```
```css
</html >


 #tb,tr,th,td{
    border:1px solid  blue;
    text-align: center;
    background-color: orange;
}
#tb{
    width: 400px;
    height: 400px;
    border-collapse: collapse;
}
```


样式
```css
 #tb{
    border-collapse: collapse;
    width:500px;
}
#tb td,#tb th{
    border:1px solid bisque;
}
#tb th{
    text-align: right;
    background-color: aquamarine;
    color: cornsilk;
}
#tb tr.alt td{
    color: #000000;
    background-color: aquamarine;
}
```

