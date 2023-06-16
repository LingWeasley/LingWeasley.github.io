---
title:  web基础知识 
categories: ['笔记']
tags: ['web']
date: ['2019-03-01']
---
HTML中块级元素和内联元素的区别
1. 下标列出了内联元素和块级元素的主要区别
html中内联元素和块级元素的区别
 块级元素：
- 独占一行，默认情况下，其宽度自动填满其父元素宽度
- 可以设置width,height属性；
- 可以设置margin，padding属性；
- 对应与display：block；
<!-- more -->

行内元素：
- 相邻的行内元素会排列在同一行李，直到一行排不下才会换行，其宽度随元素的内容而变化；
- 行内元素设置width，hight属性无效；
- 行内元素起编剧作用的只有margin-left,margin-right，padding-left，padding-rignt，其他属性不起边距效果；
- 对应于display：inline;


2. 按字母顺序排列块级元素主要有：
-  address        定义地址
-  caption      定义表格标题
-  dd    定义列表中定义条目
-  div        定义文档中的分区或节
-  dl        定义列表
-  dt       定义列表中的项目
-  fieldset      定义一个框架集
-  form     创建表单元素
-  h1,h2,h3,h4,h5,h6        标题元素
-  hr        水平线
-  legend        给fieldset元素定义标题
-  li        定义列表项目
-  noframes        为那些不支持框架的浏览器显示文本，放置于frameset标签内
-  noscript        为那些不支持脚本的浏览器显示文本
-  ol       有序列表
-  ul        无序列表
-  p       定义段落
-  pre        定义预格式化文本
-  table        定义表格
-  tbody        定义表格主体
-  td        表格中的标准单元格
-  tr       表格中的行
-  tfoot        表格中的页脚
-  th        定义表头单元格
-  thead       定义表格的表头
3. 内联元素有
-  a      可定义锚以及超链接
-  abbr       表示一个缩写形式
-  acronym       表示只取title中首字母的缩写形式
-  b        字体加粗
-  bdo       可覆盖默认的文本方向
-  big        大号字体加粗
-  br        换行
-  cite        引用进行定义
-  code        定义计算机代码文本
-  dfn        定义一个定义项目
-  em        定义为强调的内容
-  i        斜体文本效果
-  img        向网页中嵌入一张图像
-  input        输入框
-  kbd        定义键盘文本
-  label        为input进行标记/标注
-  q        定义短的引用
-  s    表示不准确不相关，却不应当给予删除的内容
-  samp        定义样本文本
-  select        定义单选或者多选菜单
-  small        呈现小号字体效果
-  span        组合文档中的行内元素
-  strong        语气更强的强调内容
-  sub        定义下标文本
-  sup        定义上标文本
-  textarea        多行文本输入控件
-  tt        打字机或者等宽的文本效果
-  var       定义变量
-  input ,-  img都是行内元素，但是它们是可以设置宽和高的。这里就涉及到可替换元素和不可替换元素。


4. 替换元素就是浏览器根据元素的标签和属性，来决定元素的具体显示内容
例如浏览器会根据img标签的src属性的值来读取图片信息并显示出来，而如果查看html代码，则看不到图片的实际内容；又列如input标签的type属性来决定是显示输入框还是单选按钮。
html中的img，input，textarea，select，object都是替换元素。这些元素往往没有实际内容，即是一个空元素、

5. 不可替代的元素：html的大多数元素时不可替代元素，其内容直接表现给用户端（例如浏览器）。