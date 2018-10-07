# css
css2 css3学习

# 概述

## 文档流
CSS世界构建的基石是HTML，而HTML最具代表的两个基石<div>和<span>正好是CSS世界中块级元素和内联级元素的代表，它们对应的正是图1-3 所示的盛水容器中的水和木头，其特性表现也正如现实世界的水和木头。

# 流、元素与基本尺寸

两类：块级元素和内联元素

## 块级元素
常见的有：<div> 、<li>、<table>

li: display: list-item
table: display : table

均为块级元素，因为他们都符合块级元素的基本特征：即是一个水平流上只能单独显示一个元素，多个块级元素则换行显示
注意：块级元素和display为block的元素不是一个概念

正是由于“块级元素”具有换行特性，因此理论上它都可以配合clear 属性来清除浮动带来的影响

### 为什么list-item 元素会出现项目符号

display: block 的元素的盒子实际由外在的“块级盒子”和内在的“块级容器盒子”组成，值为inline-block的元素则由外在的“内联盒子”和内在的“块级容器盒子”组成；值为inline 的元素则内外均是“内联盒子”。

外部尺寸与流体特性

包裹性：
button: 极具代表性的inline-block元素，可谓展示“包裹性”最好的例
子，具体表现为：按钮文字越多宽度越宽（内部尺寸特性），但如果文字足够多，则会在容器的宽度处自动换行（自适应特性）

button标签会自动换行,input标签按钮，默认white-space: pre是不会换行的，需要将pre 值重置为默认的normal。

“包裹性”开发作用？

（2）首选最小宽度
所谓“首选最小宽度”，指的是元素最适合的最小宽度; 
利用连续英文单词不换行的特性，我们就可以控制什么地方“凹”，什么地方“凸”啦

（3）最大宽度 

内联盒子：可以简单理解为display: inline、inline-block、inline-table等元素；连续内联盒子指的全部都是内联级别的一个元素或一堆元素，中间没有任何的换行标签<br>或其他块级元素；

开发中的作用

3.2.2 width值作用的细节

前面讲width: auto

下面将说设置具体宽度

这种宽度设定和表现并不合理。我总结为以下两点。

3.2.3 CSS 流体布局下的宽度分离原则

3.替换元素的尺寸计算规则