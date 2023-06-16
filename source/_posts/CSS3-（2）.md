---
title: CSS3-（2）
tags: ['web']
categories: ['笔记']
date: ['2019-03-23']
---
## CSS轮廓
轮廓主要是用来突出显示元素的作用

outline                           设置轮廓属性
outline-color                  设置轮廓的颜色
outline-style                   设置轮廓的样式
outline-width                  设置轮廓的宽度
<!-- more -->
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >Title</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <p >突出的效果文字</p >
</body >
```
```css
</html >

 p{
    outline-width: 10px;
    outline-color: #f95cff;
    outline-style: groove;
}
```

# CSS定位
## 定位
1.  css定位 改变元素在页面上的位置
2. css定位机制：普通流：元素按照其在HTML中的位置顺序决定排布的过程
                         浮动
                         绝对布局
    
position               把元素放在一个静态的，相对的，绝对的，或固定的位置中
top                    元素向上的偏移量
left                   元素向左的偏移量
right                  元素向右的偏移量
bottom                 元素向下的偏移量
overflow               设置元素溢出其区域发生的事情
clip                   设置元素显示的形态
vertical-align         设置元素垂直对齐的方式
z-index                设置元素的堆叠顺序


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
   <div id="position1" ></div >
   <div id="position2" ></div >
   <script >
       for(var i=0;i<100;i++){
           document.write(i+"<br/ >")
       }
   </script >
</body >
```
```css
</html >

#position1{
    width: 100px;
    height: 100px;
    background-color: #d2b3ff;
    position: absolute; <!--position位置属性 relative相对的absolute绝对的fixed固定static静态 -- >
    left: 20px;
    top: 20px;
    z-index: 2; <!--谁的值大谁在前面-- >
}
#position2{
    width: 100px;
    height: 100px;
    background-color: #d2b3ff;
    position: absolute;
    left: 10px;
    top: 10px;
    z-index: 1;
}
```
## 浮动

1. 浮动  float属性可用的值： left:元素向左浮动     right元素向右浮动    none元素不浮动  inherit从父级继承浮动属性 
2. clear 属性值： left，right：去掉元素向左向右浮动   both：左右两侧均去掉浮动  inherit：从父级继承来clear的值
```html
 <body >
<div id="container" >
   <div id="sd" ></div >
   <div id="tk" ></div >
   <div id="tm" ></div >
   <div id="tsxt" >helloworld</div >
</div >
   </script >
</body >
```
```css
#sd{
    width:100px;
    height:100px;
    background-color: #e8ffa8;
    float: left;
}
#tk{
    width:150px;
    height:100px;
    background-color:cadetblue;
    float: left;
}
#tm{
    width:100px;
    height:100px;
    background-color:red;
    float: left;
}
#container{
    width: 300px;
    height:500px;
    background: gray;
}
#text{
    clear: both;
}
```
3.浮动应用
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >浮动</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
<div id="div1" >
    <ul >
        <li ><img src="01.jpg" ></li >
        <li ><img src="02.jpg" ></li >
        <li ><img src="03.jpg" ></li >
    </ul >
    <ul >
        <li ><img src="04.jpg" ></li >
        <li ><img src="05.jpg" ></li >
        <li ><img src="06.jpg" ></li >
    </ul >
    <ul >
        <li ><img src="07.jpg" ></li >
    </ul >
</div >
</body >
</html >
```
```css
*{
    margin: 0px;
    padding:0px;
}
li {
    list-style: none;
}
#div1{
    width:950px;
    height: auto;
    margin: 20px auto;
}
ul{
    width: 250px;
    float:left;
}
```


# CSS盒子模型
margin，border，padding，content部分组成
## css内边距
内边距在content外，边框内
padding                      设置所有边距
padding-bottom          设置底边距
padding-left                设置左边距
padding-right              设置右边距
padding-top                设置上边距
```html
 <!DOCTYPE html >
   <html lang="en" >
   <head >
     <meta charset="UTF-8" >
     <title >浮动</title >
     <link rel="stylesheet" type="text/css" href="style.css" >
   </head >
   <body >
     <table border="1"  >
      <tr >
          <td >内边距</td >
      </tr >
     </table >
   </body >
   </html >
```
```css
td{
    padding-left:100px;
    padding-right: 50px;
    padding-bottom: 60px;
    padding-top: 70px;
}
```
## css边框
  我们可以创建出效果出色的边框，并且可以应用于任何元素
## 边框的样式
border-style：定义了10个不同的非继承样式，包括none
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >浮动</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
<p >css边框样式</p >
</body >
</html >
```
```css
p{
    border-style: dotted;
}
```
## 边框的单边样式
border-top-style
border-left-style
border-right-style
border-bottom-style
```css
p{
    border-style: dotted;
    border-top-style:double;
}
```
## 边框的宽度
border-width
## 边框的单边的宽度
border-top-width
border-left-width
border-right-width
border-bottom-width
## 边框的颜色
border-color
## 边框单边的颜色
border-top-color
border-left-color
border-right-color 
border-bottom-color
## css3边框
border-radius  圆角边框
box-shadow    边框阴影
border-image  边框图片
```css
p{
    border-radius:10px;
    width:200px;
    background-color: #ff7b86;
    text-align: center;
}
.cssid{
    background-color: #2b6cff;
    width: 100px;
    height: 100px;
    text-align: center;
    box-shadow: 向右移动像素  向下移动像素  阴影透明度设计  阴影颜色;
}
```
# css外边距
 围绕在内容边框的区域就是外边距，外边距默认为透明区域，外边距接受任何长度单位，百分数值。
## 外边距常用属性
margin                          设置所有边距  
margin-bottom              设置底边距 
margin-left                    设置左边距 
margin-right                  设置右边距 
margin-top                    设置上边距 
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >浮动</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div class="mg" >外边距</div >
</body >
</html >
```
```css
 body{
     margin: 0px;
 }
.mg{
    background-color: #42ff49;
    width: 100px;
    height: 100px;
    margin-top: 100px;
}
```css
## 盒子模型
```css
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >盒子模型</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div class="container" >
       <div class="ab" >
           <div class="cd" >
               <div class="content" >盒子模型</div >
           </div >
       </div >
   </div >
</body >
```
```css
</html >

 body{
     margin: 0px;
 }
.container{
    margin: 0px;
}
.ab{
    border-style:double;
}
.cd{
    padding:10px;
}
.content{
    background-color: #ff78f4;
    text-align: center;
}
```
# css外边距合并
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >盒子模型</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div class="container" >
       <div class="ab" >
           <div class="cd" >
               <div class="content" >盒子模型</div >
           </div >
       </div >
   </div >
  <div class="container1" >
       <div class="ab1" >
           <div class="cd1" >
               <div class="content1" >盒子模型</div >
           </div >
       </div >
   </div >
</body >
```
```css
</html >

 body{
     margin: 0px;
 }
.container{
    margin: 0px;
}
.ab{
    border-style:double;
}
.cd{
    padding:10px;
}
.content{
    background-color: #ff78f4;
    text-align: center;
}
.container1{
    margin: 0px;
}
.ab1{
    border-style:double;
}
.cd1{
    padding:10px;
}
.content1{
    background-color: #ff78f4;
    text-align: center;
}
```
# css盒子模型应用
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >盒子模型</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
 <body >
  <div class="top" >
      <div class="top-content" ></div >
  </div >
  <div class="content" >
      <div class="content-img" ></div >
      <div class="content-no" ></div >
      <div class="content-body" ></div >
  </div >
  <div class="foot" >
      <div class="foot-content" ></div >
      <div class="foot-subnav" ></div >
  </div >
</body >
```
```css
</html >

 *{
    margin: 0px;
    padding:0px;
}
.top{
    width: 100%;
    height: 50px;
    background-color:black;
}
.top-content{
    width: 70%;
    height: 50px;
  background-color: #ff4060;
    margin:0px auto;
}
.content{
    width: 70%;
    height: 1150px;
    background-color: #ffb731;
    margin: 20px auto;
}
.content-img{
    width:100%;
    height: 100px;
    background-color: #fff067;
}
.content-no{
    width:100%;
    height: 50px;
    background-color: #37ff53;
}
.content-body{
    width:100%;
    height: 1000px;
    background-color: #46ffff;
}
.foot{
    width: 100%;
    height: 50px;
    background-color:black;
    margin: 0px auto;
}
.foot-content{
    width: 70%;
    height: 40px;
    background-color: #3659ff;
    margin: 0px auto;
}
.foot-subnav{
    width:70%;
    height:10px;
    background-color: #8839ff;
    margin: 0px auto;
}
```

