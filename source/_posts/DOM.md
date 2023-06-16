---
title:  DOM
categories: ['笔记']
tags: ['web']
date: ['2019-03-18']
---
### CSS
DOM并不是与网页结构打交道的唯一技术。我们还可以通过css告诉浏览器应该如何显示一份文档。
继承（inheritance）是CSS技术中的一项强大功能。类似于DOM，CSS也把文档的内容视为一颗节点树。节点树上的各个元素将继承其父元素的样式属性。
为了把某一个或某几个元素与其他内院区别开来，需要使用class和ID属性。
<!-- more -->
1. class
可以在所有元素上任意应用class属性
2. ID
ID属性的用途是给网页里的某个元素加上一个独一无二的标识符
### 获取元素
有3种DOM方法可获取元素节点，分别是通过元素ID，通过标签名字和通过类名字来获取。
1. getElementById
这个将返回一个与那个有着给定ID属性值的元素节点对应的对象。
docunment.getElementById(id)
//通用
```JS
<!DOCTYPE html>
<html lang="en">
<head>
 <meta charset="utf-8"/>
 <title>Shopping list</title>
</head>
<body>
 <h1>What to buy</h1>
 <p title="a gentle reminder">Don't forget to buy this stuff.</p>
 <ul>
  <li>A tin of beans</li>
  <li class="sale">Cheese</li>
  <li class="sale">Milk</li>
 </ul>
 <script>
  alert(typeof document.getElementById("purchass"))
 </script>
</body>
</html>
```
2. getElementByTagName
返回一个对象数组，每个对象分别对应着文档里有着给定标签的一个元素
document.getElementByTagName("li")
3. getElementByClassName
返回一个数组
document.getElementByClassName("class")

```JS
<script>
   function getElementsClassName (node,classname){
       if(node.getElementsByClassName){
           //使用现有方法
           return node.getElementsByClassName(classname);<
       }else{
           var results = new Arrary();
           var elems = node.getElementsByClassName("*");
             for (var i=0;i<elems.length;i++ ){
                 if(elems[i].className.indexOf(classname) != -1){
                     results[results.length]=elems[i];
                 }
             }
             return results;
       }
   }
```
## 获取和设置属性
### getAttribute
只有一个参数----你打算查询的属性的名字
```JS
object.getAttribute(attribute)

var paras = document.getElementsByTagName("p");
for(var i=0;i<paras.length;i++ ){
  var title_text = paras[i].getAttribute("title");
  if (title_text !=null) {
    alert(title_text);
  }
}
```
### setAttrubute
允许我们对属性节点的值做出修改
```JS
object.setAttribute(attribute,value)

var shopping = document.getElementById("purchases");
alert(shopping.getAttribute("title"));
shopping.setAttribute("title","a list of goods");
alert(shopping.getAttribute("title"));
```
## 图片库
完整的代码块
```JS
function showPic(whichpic) {
    var source = whichpic.getAttribute("href");
    var placeholder = document.getElementById("placeholder");
    placeholder.setAttribute("src",source);
    var text = whichpic.getAttribute("title");
    var description = document.getElementById("description");
    description.firstChild.nodeValue = text;
}
function countBodyChildren() {
    var body_elelment = document.getElementsByTagName("body")[0];
    alert(body_elelment.nodeType);
}
window.onload = countBodyChildren;
### 如何插入一个占位符？
<img id="placeholder" src="图片的路径" alt="图片的显示">
```
问题1：alt和title的区别？

alt属性将在图片无法显示时，替代图片显示文本。
title属性规定标签元素以外的信息。
### 如何让图片代替占位符并且显示在当页？
```JS
function showPic(whichpic) {
    var source = whichpic.getAttribute("href");
    var placeholder = document.getElementById("placeholder");
    placeholder.setAttribute("src",source);
}
```
1. 事件处理函数(作用是在特定事件发生时调用特定的JavaScript代码）
onmouseover：鼠标指正悬停在某个元素上市触发一个动作。
onmouseout：鼠标指针离开某个元素时触发一个动作。
onclick：鼠标点击某个链接是触发一个动作。
```JS
<li>
  <a href="lw/d.jpg" onclick="showPic(this); return false" title = "Family portraits">全家福</a>
</li>
```
此处的this指待<a>
2. childNodes属性
是用来获取某个元素的所有子元素的属性。但首先要确定这个元素。
element.childNodes
3. nodeType属性
是用来确定当前打交道的节点是哪一种节点。但是nodeType属性是用数值来显示的，共有12种，常用为以下三种：
元素节点的nodeType属性值是1；
属性节点的nodeType属性值是2；
文本节点的nodeType属性值是3.
4. nodeValue属性
是用来改变文本节点的值，也就是本次案例中改变图片的描述值。
```JS
alert（description.childNodes[0].nodeValue）; //打印description的文本。
var text = whichpic.getAttribute("title");//改变文本值
    var description = document.getElementById("description");
    description.firstChild.nodeValue = text;
```
childNodes[0]的同义词firstchild
lastchild是childNodes的最后一个子元素