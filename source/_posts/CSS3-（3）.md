---
title: CSS3-（3）
tags: ['web']
categories: ['笔记']
date: ['2019-03-29']
---
# 对齐操作

1.  使用margin属性进行水平对齐
```html
 <!DOCTYPE html >
<html lang="en" >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
     <div class="div" ></div >
</body >
</html >
```
```css
 *{
    margin: 0px;
}
.div{
    width: 70%;
    height: 1000px;
    background-color: cadetblue;
    margin-left:auto;
    margin-right: auto;    <!--也可以这样写margin:"0px auto";-- >
}
```
<!-- more -->
2.使用position属性进行左右对齐
```css

 *{
    margin: 0px;
}
.div{
    width: 70%;
    height: 1000px;
    background-color: cadetblue;
    position: absolute;
    left: 0px;
}

```
3.使用float属性进行左右对齐
```css
*{
    margin: 0px;
}
.div{
    width: 70%;
    height: 1000px;
    background-color: cadetblue;
    float: left;
}
```

# 尺寸操作

heigh                          设置元素高度                            
line-height                  设置行高
max-hright                  设置元素最大高度 
max-width                   设置元素最大宽度
min-width                   设置元素最小宽度
min-height                  设置元素最小高度 
width                          设置元素宽度

例如
```css
 .p1{
    width:400px;
    line-height: normal;
}
.p2
{
    width: 400px;
    line-height: 200%;
}
.p3{
    width: 400px;
    line-height:50% ;
}
```


# 分类操作
clear                    设置一个元素的侧面是否允许其他的浮动元素
cursor                  规定当只想某元素之上时显示的指针类型
display                设置是否及如何显示元素
float                    定义元素在那个方向浮动
position               把元素放置到一个静态的，相对的，绝对的，固定的位置
visibility               设置元素是否可见或不可见
```css
p{
    cursor:cell;          <!--还有其他样式-- >
    visibility：hidden;  <!--可见visible-- >
}
```
# 导航栏

1. 垂直导航栏
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
    <ul >
        <li ><a href="#" >导航栏1</a ></li >
        <li ><a href="#" >导航栏2</a ></li >
        <li ><a href="#" >导航栏3</a ></li >
    </ul >
</body >
```
```css
</html >

 ul{
    list-style-type: none;   <!--去掉点-- >
    margin: 0px;
    padding: 0px;
}
a:link,a:visited{
    text-decoration: none;      <!--去掉下划线-- >
    display: block;             <!--摆放方式-- >
    background-color: #fff067;
    color: #ff4060;
    width: 50px;
    text-align: center;
}
a:active,a:hover{
    background-color: #3285ff;  <!--鼠标点击时颜色变化-- >
}
```
2.水平导航栏
```css
 ul{
    list-style-type: none;
    margin: 0px;
    padding: 0px;
    width: 250px;
    text-align: center;
}
a:link,a:visited{
    font-weight: bold;      <!--文字加粗-- >
    text-decoration: none;
    background-color: #fff067;
    color: #ff4060;
    width: 50px;
    text-align: center;
}
a:active,a:hover{
    background-color: #3285ff;
}
li{
    display: inline;
    padding: 3px;
    padding-right: 5px;
    padding-left: 5px;
}
```

# 图片操作
```html
 <!DOCTYPE html >
<head >
    <meta charset="UTF-8" >
    <title >对齐</title >
    <link rel="stylesheet" type="text/css" href="style.css" >
</head >
<body >
    <div class="container" >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
        <div class="image" >
            <a href="#" target="_self" ></a >
            <img src="01.jpg" alt="风景" width="200px" height="200px" >
        </div >
        <div class="黑暗" ></div >
    </div >
</body >
```
```css
</html >

 body{
    margin: 10px auto;
    width: 70%;
    height: auto;
    background-color: #fffcb6;
}
.image{
    border: 1px solid #824b99;
    width: auto;
    height: auto;
    float: left;
    text-align: center;
    margin: 5px;
}
img{
    margin: 5px;
    opacity:0.8;   <!--透明度-- >
}
.text{
    font-size: 12px;
    margin-bottom: 5px;
}
```
