---
title:  Javascript -语法
categories: ['笔记']
tags: ['web']
date: ['2019-03-05']
---
## 介绍
Javascript是最流行的脚本语言：是一种轻量级的编程语言；可以插入html的编程代码；插入html页面之后可以由任何浏览器打开。
## 准备工作
用Javascript编写代码必须要通过HTML和XHTML文档才能执行，有三种方法可以做到这一点：
第一种方法是把Javascript放到head中script标签中：
<!-- more -->
```JS
<!DOCTYPE html>
<html lang="en">
  <head>
  <meta charset="utf-8"/>
  <title>element</title>
  <script> javascript</script>
</head>
<body>
</body>
第二种方法是将Javascript代码存为一个扩展名为.js的独立文件，然后在script中src属性中引用
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8"/>
  <title>element</title>
  <script src="lw03.js"> </script>
</head>
<body>
</body>
第三种方法，也是最好的一种方法是联合第二种方法将script标签放在body之前，这样可以更快的加载页面。
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="utf-8"/>
  <title>element</title>
</head>
<body>
<script src="lw03.js"`></script>
</body>
```
程序语言分为编译型和解释型。java和C++等语言需要一个编译器，编译器是一种程序，能够把java等高级语言编写出来的源代码翻译为可以直接在计算机上执行的文件。解释型程序设计语言不需要编译器，它们仅需要解释器。对于javascript语言，web浏览器负责完成有关的解释和和执行工作。浏览器中的javascript解释器将直接读入源代码并执行。浏览器中没有编译器，将无法执行。
用编译型语言编写的代码有错误，在编译阶段就可以发现。而解释型语言代码中的错误只能呢个等到解释器执行到有关代码才可以被发现。
编译型语言比解释型语言速度更快，可移植性更好，但是比较难学。
## 语法
### 语句(statement)
用JavaScript编写脚本，与其他语言编写出来的脚本一样，都由一系列指令构成，这些指令叫语句。
JavaScript只需要简单的把各条语句放在不同行上就可以分隔它们，或者在同一行的花用逗号分隔，最后要加上分号结尾。
### 注释(comment)
//单行注释  <`!--/**/多行注释
### 变量（variable)
var 是变量的关键字
var mood="happy"   //声明+赋值  var 是变量的关键字  mood是变量名  happy是值
var age=20,mood="happy" //最有效的做法
JavaScript语法不允许变量名中包含空格或标点符号，但美元符号$除外；
javascript变量名可以含有字母，下划线，数字和美元符号，但第一个字谜不能是数字
驼峰格式的myMood通常是函数名，方法名和对象属性命名的首选格式
### 数据类型
在声明变量名的同时还要声明变量名的类型称为强类型
1. 字符串
字符串由零个或多个字符组成。字符包括（但不限于）字母，数字，标点符号和空格，字符串必须包含在引号里，单引号和双引号都可以。选择引号的时候最好根据字符串所包含的字符来选择。最好和字符串中的引号区别使用，要不然就要字符串中的引号进行转义，通过反斜杠\。例如：var ="don\'t  ask".另外最好保持一个脚本中的引号是一致的。
2. 数值
数值不限制，可以是整数也可以是小数（浮点数），可以是正数也可以是负数。
3. 布尔值（Boolean）
布尔数据只有两个可选值-----true或false，重要的是两个中只能取一个。布尔值不是字符串，千万不能加引号。
### 数组（array）
字符串，数值和布尔值都是标量（scalar）。如果想用一个变量来储存一组值，就需要数组，数组可以用Arrary来声明，声明的同时还可以指定数组初始元素个数，也就是这个数组的长度（length）。
var Beatles = Arrary(length);
向数组中添加元素的操作称为填充（populating），在填充时不仅要各处新元素的值，还需要给出新元素在数组中存放的位置，这个位置就是这个元素的下标（index），下标必须用方括号括起来：
Arrary[index]=element;

数组的各种写法：
这是一个相当强大的储存方式
var Beatles = Arrary(4);
Beatles[0]="John";
Beatles[1]="Gaul";
Beatles[2]="George";
Beatles[3]="George";

```JS
var Beatles = Arrary("John","Gaul","George","George");
//声明的同时填充
var lennon = ["John",1940,fales];
//数组里面可以放字符串，数字，布尔值
var name = "John";
beatles[0]=name;
//数组可以是一个变量
var names = Arrary("John","Gaul","George","George");
beatles[1] = names[3];
//数组元素的值还可以是另一个数组的元素
var lennon = ["John",1940,fales];
var beatles =[];
beatles[0] = lennon;
//beatles数组的一个元素就是一个数组
```
4. 关联数组
Beatles是一个传统的数组，关联数组则不是一个传统的数组。区别在于，传统的数组下标是整数，而关联数组下标则可以是其他，比如字符串。这样使代码更有可读性。
```JS
var lennon = Arrary();
lennon["name"] = "John";
lennon["year"] = 1940;
lennon["living"] = fales;
```
### 对象
与数组类似，对象也是使用一个名字来表示一组值。对象的每个值都是对象的属性。用点来获取
```JS
var lennon = object();
lennon.name = "name";
lennon.year = 1940;
lennon.living = fales;
```
创建对象的各种方法：
{propertyName:value,propertyName:value}
var lennon = {name:"John",year:1940,living:fales};

## 操作 
+-*/ ++  === +=(加法和赋值)
++可以拼接字符串和数值
注意区别
## 条件语句
### if
条件必须放在if后面的圆括号中。条件的求职结果永远是一个布尔值，只能是true或fales。花括号中的语句，不管他们有多少条，只有在给定条件的求值结果是true的情况下才会执行。
```C
if(1>2){
  alert("The world has gone mad!")
} eles{
  alert("All is well with the world")
}
```
花括号并不是必不可少的
```C
if(1>2) alert("The world has gone mad!")
```
### 比较操作符
大于>，小于<，大于或等于>=，小于或等于 <=，等于 == ，不等于!= ，严格相等 ===，严格不等!== 
### 逻辑操作符
&&（逻辑与） 逻辑操作符的操作对象是布尔值，每个逻辑操作数返回一个布尔值true或者是fales。逻辑与操作只有在它的两个操作数都是true时才会是true。
||（逻辑或）只要他的操作数中有一个是true，逻辑或就将是true。如果它的两个操作数都是true，逻辑或操作也将是true，只有当它的两个操作数都是fales时，逻辑或才会是fales。
！（逻辑非）只能作用于单个操作数，其结果是把那个逻辑操作数所返回的布尔值取反。如果那个逻辑操作数所返回的值是true，那么逻辑非操作符将把它取反为fales。
## 循环语句
### while
1. while循环和if循环唯一的区别是：只要给定条件的求值结果是true，包含在花括号里的代码就讲反复地执行下去
```JS
var count = 1;
while (count<11){
  alert(count);
  count++;
}
```
1. do...while
对循环控制条件的求值发生在每次循环结束之后。因此花括号里的语句至少被执行一次
```JS
do{
  statement;
}while(cindition);
```
### for
类似于while，for循环只是while循环的一种变体，变得更紧凑。用for循环来重复执行一些代码的好处是循环控制结构更加清晰。最常见的用途之一是对某个数组里的全体元素进行遍历处理。
```JS
initionlize;
while (condition){
  statements;
  increment;
}

for(initial condition;test condition;alter condition){
  statement;
}
for（conut=1;count<11;count++）{
  alert(count);
}
```
## 函数（founction）
如果需要多次使用同一段代码，可以把它们封装成一个函数。函数就是一组允许在你的代码里随时调用的语句.
```JS
founction shout(){
  var Beatles = Arrary("John","Gaul","George","George");
  for(var count = 0;count<bearles.length;count++){
    alert(beatles[count]);
  }
} 
```
函数不仅能够（以参数的形式）接受数据，还能够返回数据。用到return语句
```JS
function multiply(num1,num2){
  var total = num1*num2;
  return total;
}
```
函数的真正价值体现在，我们可以把它们当做一种数据类型来使用，这意味着可以把一个函数的调用结果赋给一个变量：
```JS
var temp_fahrenheit = 95;
var temp_celsius = converToCelsius(temp_fahrenheit);
alert(temp_Celsius)；
```
驼峰命名法可以区分变量名和函数
### 变量的作用域
全局变量可以在脚本中的任何位置被引用。
局部变量只存在于声明它的那个函数内部。
如果在某个函数中使用了var，那个变量就讲被视为一个局部变量，它只存在于这个函数的上下文中；反之，如果没有使用var，那个变量就讲被视为一个全局变量，如果脚本里已经存在一个与同名的全局变量，这个函数就会改变那个全局变量的值。
在定义一个函数时，我们一定要把它内部的变量全都明确地声明为局部变量。
## 对象
对象是自包含的数据集合，包含在对象里的数据可以通过两种形式访问------属性（property）和方法（method）
属性是隶属于某个特定对象的变量。方法是只有某个特定对象才能调用的函数。对象就是由一些属性和方法构成的一个数据实体。
1. 内建对象
内建在JavaScript语言里的对象，如Arrary,Math,Date等。
2. 宿主对象
由流浪器提供的预定义对象被称为宿主对象
## DOM
文档DOM中D----document
对象DOM中O----object
模型DOM中M----Model
DOM代表着加载到浏览器窗口的当前网页。浏览器提供了网页的地图（或者说模型），而我们可以通过JavaScript去读取这张地图。
DOM把一份文档表示为一棵家谱树，并使用parent，child,sibling等记号来表明家族成员之间的关系。
## 节点（node）
使用节点比使用家谱树更为准确。它表示网络中的一个连接点，一个网络就是由一些节点构成的集合。
### 元素节点
标签的名字就是元素的名字。HTML是根元素
### 文本节点
在XHTML文档中，文本节点总是被包含在元素节点的内部。
### 属性节点
属性节点用来对元素做出更具体的描述。在DOM中，title = "a gentle reminder"是一个属性节点，属性节点总是被包含在起始标签内，所以属性节点总是被包含在元素节点中。并非所有的元素都包含着属性，但所有的属性都被元素包含着。
