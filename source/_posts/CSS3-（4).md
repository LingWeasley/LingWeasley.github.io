---
title: CSS3-（4）
tags: ['web']
categories: ['笔记']
date: ['2019-04-02']
---
# 选择器详解
## 元素选择器
最常见的选择器就是元素选择器，文档的元素就是最基本的选择器 例如：h1{ } a{ }
<!-- more -->
```css
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <p >hello</p >
</body >
</html >
```
```css
 p{
    color: cadetblue;     <!--根据HTML中P标签 在CSS中选择P选择器-- >
}
```
## 选择器分组
1.例子  h1{ } h2{ }
2.通配符*{ }
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <h1 >标题1</h1 >
   <h2 >标题2</h2 >
   <p >hello</p >
</body >
</html >
```
```css
 *{
   color: #ffb5f5;       <!-- 除了自己定义外，全都要用这个样式-- >
    margin: 0px;
    padding: 0px;
}
h1,h2{                  <!--h1,h2一起改-- >
    color: #3659ff;
}
```

## 类选择器详解
类选择器允许以一种独立与文档元素的方式来指定样式  例如 .class{ }
结合元素选择器：例如 a.class{ }
多类选择器 例如：.class.class{ }
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <p class="p1" >this is hello</p >
   <p class="p1" >this is hello</p >
   <p class="p1 p2" >this is hello</p >
</body >
</html >
```
```css
 .p1{
    color: #0000FF;
}
.P2{
    font-size: medium;
}
.p1.p2{
    font-weight: revert;   <!--多类选择器-- >
}
```

## ID选择器详解
ID选择器类似于类选择器，不过也有一些重要差别   例如#id{ }
类选择器和id选择器区别：
1.id只能在文档中使用一次，而类可以多次使用;
2.id选择器不能结合使用;
3.当使用js时候，需要用到id;
## 属性选择器详解
简单属性选择：例如[title]{}
根据具体属性值选择：除了选择拥有某些的元素，还可以进一步缩小选择范围，只选择有特定属性值的元素。例如：a[ herf="http//www,jikexueyuan.com"]{}
属性和属性值必须完全匹配
根据部分属性值选择
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
    <style >
        [title]{
            color: #ff475b;
        }
        [href="http://www.jikexueyuan.com"]{
            font-size: 30px;
        }
        [title~=title]{     <!--模糊-- >
            font-size: 50px;
        }
    </style >
</head >
<body >
   <p title="tit" >this is hello</p >
   <p title="title" >this is hello</p >
   <p title="t" >this is hello</p >
   <p title="title hello" >this is hello</p >
   <a href="http://www.jikexueyuan.com" >极客学院</a >
</body >
</html >
```
## 后代选择器
 后代选择器可以选择作为某元素后代的元素
 ```css
 <p >this is my<strong >web<i >hello</i ></strong > page</p >

 p strong i{
    color: #ff475b;
}
```
## 子元素选择器
与后代选择器相比，子元素选择器只能选择作为某元素子元素的元素  h1 >strong{ };
```css
 <p >this is my<strong >web<i >hello</i ></strong > page</p >

 p >strong >i{          <!--不可以隔代-- >
    color: #ffb731;
    font-size: 20px;
}
```
## 相邻兄弟选择器
可选择紧接在另一个元素后的元素，而且二者有相同的父元素  例如h1+p{}
```html
 <div >
    <ul >
        <li >111</li >
        <li >222</li >
        <li >333</li >
    </ul >
    <ol >
        <li >444</li >
        <li >555</li >
        <li >666</li >
    </ol >
</div >
```
```css
 li+li{
    color: #ff78f4;
    font-size: 50px;
} 只有222  333    444   555 有效果
```
# CSS动画
## 2D,3D转换

1. 通过css3转换，我们能够对元素进行移动，缩放，转动，拉长或拉伸转换时使元素改变形状，尺寸和位置的一种效果。可以使用2D,3D来转换元素
2. 2D转换方法：translate(), rotate(),scale(),skew(),matrix()
3. 3D转换方法：rotateX（）,rotateY()
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >动画</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div >这是一个初始效果</div >
   <br/ >
   <div class="div2" >改变后的效果</div >
</body >
</html >
```
```css
 div{
    width: 100px;
    height: 100px;
    background-color: #daffc6;
}
.div2{
    transform:translate(200px,100px);  <!--移动-- >
    -webkit-transform: translate(200px,100px);/*safari chrome*/
    -ms-transform:translate(200px,100px);/*ie*/
    -o-transform: translate(200px,100px);/*opera*/
    -moz-transform: translate(200px,100px);/*Firefox*/

}
.div2{
    transform: rotate(200deg);  <!--旋转-- >
    -webkit-transform: rotate(200deg);
    -ms-transform:rotate(200deg);
    -o-transform: rotate(200deg);
    -moz-transform: rotate(200deg);
}
.div2{
    margin-top: 200px;   
    transform: scale(1,2); <!--缩放-- >
    -webkit-transform: scale(1,2);
    -ms-transform:scale(1,2);
    -o-transform: scale(1,2);
    -moz-transform: scale(1,2);
}
.div2{
    transform:skew(50deg,50deg);  <!--偏移-- >
    -webkit-transform:skew(50deg,50deg);
    -ms-transform:skew(50deg,50deg);
    -o-transform: skew(50deg,50deg);
    -moz-transform: skew(50deg,50deg);
}
.div2{
    transform:rotateX(120deg);  <!--3D-- >
    -webkit-transform:rotateY(120deg);
}
```
## 过渡
1. 通过使用css3，可以给元素添加一些效果
2. css3过渡是元素从一种样式转换成另一种样式  动画效果的css 和动画执行的时间
3. 属性    transition                                 设置四个过渡属性
               transition-property                  过渡的名称
               transition-duration                  过渡效果花费的时间                  
               transition-timing-function        过渡效果的时间曲线         
               transition-delay                        过渡效果开始时间
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >动画</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div >效果展示</div >
</body >
</html >
```
```css
 div{
    width: 100px;
    height: 100px;
    background-color: #ff836b;
    -webkit-transition: width 2s,height 2s,-webkit-transform 2s;
    transition: width 2s,height 2s,transform 2s;
    transition-delay: 2s;    <!--延迟-- >

}
div:hover{
    width: 200px;
    height: 200px;
    transform: rotate(360deg);
    -webkit-transform: rotate(360deg);
}
```
## 动画

1. 通过css3，也可以进行创建动画
2. css3的动画需要遵循@keyframes规则     规定动画的时长和规定动画的名称
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >动画</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div >动画效果</div >
</body >
</html >
```
```css
 div{
    width: 100px;
    height: 100px;
    background-color: #ff836b;
    position: relative;
    animation: anim 5s;
    -webkit-animation: anim 5s;
}
@keyframes anim {
    0%{background: #0f00f0;left:0px;top: 0px;}
    25%{background: #000f0f;left:200px;top: 0px;}
    50%{background: #0ffff0;left:200px;top: 200px;}
    75%{background: #f00f00;left:0px;top: 200px;}
    100%{background:#000ff0;left:0px;top: 0px;}
}
@-webkit-keyframes anim {
            0%{background: #0f00f0;left:0px;top: 0px;}
            25%{background: #000f0f;left:200px;top: 0px;}
            50%{background: #0ffff0;left:200px;top: 200px;}
            75%{background: #f00f00;left:0px;top: 200px;}
            100%{background:#000ff0;left:0px;top: 0px;}
        }
```
## 多列

1. 在css中，可以创建多列来对文本或者区域进行布局
2. 属性;column-count       column-gap          column-rule
```css
 .div1{
    column-count: 4;
    -webkit-column-count: 4;
    -webkit-column-gap: 30px;
    column-gap: 30px;
    column-rule: 5px outset #ff0000;
    -webkit-column-rule: 5px outset #ff0000;
}
```
## CSS瀑布流效果
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >动画</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
   <div   class="container" >
       <div ><img src="01.jpg" >
           <p >风景图</p ></div >
       <div ><img src="02.jpg" ></div >
       <div ><img src="03.jpg" >
           <p >风景图</p ></div >
       <div ><img src="04.jpg" ></div >
       <div ><img src="05.jpg" ></div >
       <div ><img src="06.jpg" ></div >
       <div ><img src="07.jpg" ></div >
       <div ><img src="01.jpg" >
           <p >风景图</p ></div >
       <div ><img src="02.jpg" ></div >
       <div ><img src="03.jpg" ></div >
       <div ><img src="04.jpg" ></div >
       <div ><img src="05.jpg" >
           <p >风景图</p ></div >
       <div ><img src="06.jpg" ></div >
       <div ><img src="07.jpg" ></div >
       <div ><img src="01.jpg" ></div >
       <div ><img src="02.jpg" >
           <p >风景图</p ></div >
       <div ><img src="03.jpg" ></div >
       <div ><img src="04.jpg" ></div >
       <div ><img src="05.jpg" ></div >
       <div ><img src="06.jpg" ></div >
       <div ><img src="07.jpg" ></div >
   </div >
</body >
</html >
```
```css
 .container{
    column-width: 250px;
    -webkit-column-width:250px;
    -webkit-column-gap: 5px;
    column-gap: 5px;
}
.container div{
   width:250px;
    margin: 5px 0;
}
.container p{
    text-align: center;
}
```
# HTML和CSS简单页面效果实例
# 补充内容
## inline和inline-block的区别
1. block和inline这两个概念是简略的说法，完整确切的说应该是 block-level elements (块级元素) 和 inline elements (内联元素)。block元素通常被现实为独立的一块，会单独换一行；inline元素则前后不会产生换行，一系列inline元素都在一行内显示，直到该行排满。
2. 大体来说HTML元素各有其自身的布局级别（block元素还是inline元素）：常见的块级元素有 DIV, FORM, TABLE, P, PRE, H1~H6, DL, OL, UL 等。常见的内联元素有 SPAN, A, STRONG, EM, LABEL, INPUT, SELECT, TEXTAREA, IMG, BR 等。
3. block元素可以包含block元素和inline元素；但inline元素只能包含inline元素。要注意的是这个是个大概的说法，每个特定的元素能包含的元素也是特定的，所以具体到个别元素上，这条规律是不适用的。比如 P 元素，只能包含inline元素，而不能包含block元素。一般来说，可以通过display:inline和display:block的设置，改变元素的布局级别。
## block，inline和inlinke-block细节对比
● display:block
  a. block元素会独占一行，多个block元素会各自新起一行。默认情况下，block元素宽度自动填满其父元素宽度。
  b. block元素可以设置width,height属性。块级元素即使设置了宽度,仍然是独占一行。
  c. block元素可以设置margin和padding属性。
● display:inline
  a. inline元素不会独占一行，多个相邻的行内元素会排列在同一行里，直到一行排列不下，才会新换一行，其宽度随元素的内容而变化。
  b. inline元素设置width,height属性无效。
  c. inline元素的margin和padding属性，水平方向的padding-left, padding-right, margin-left, margin-right都产生边距效果；但竖直方向的padding-top, padding-bottom, margin-top, margin-bottom不会产生边距效果。
● display:inline-block
  a. 简单来说就是将对象呈现为inline对象，但是对象的内容作为block对象呈现。之后的内联对象会被排列在同一行内。比如我们可以给一个link（a元素）inline-block属性值，使其既具有block的宽度高度特性又具有inline的同行特性。
## 补充说明
● 一般我们会用display:block，display:inline或者display:inline-block来调整元素的布局级别，其实display的参数远远不止这三种，仅仅是比较常用而已。
● IE（低版本IE）本来是不支持inline-block的，所以在IE中对内联元素使用display:inline-block，理论上IE是不识别的，但使用display:inline-block在IE下会触发layout，从而使内联元素拥有了display:inline-block属性的表象。
标签: CSS