# 个人网站开发报告

标签（空格分隔）：作者：张日安 学号：16058329

---

>##1.策划思路
  本人喜欢旅游，家乡那边有许多好玩的，著名的景点我也去过，所以想把期末要求的个人网站主题设计为**桂平旅游**，通过这个网站给大家介绍家乡的一些著名的景点，给家乡招点人气；内容来源于**百度旅游**，**欣欣旅游**等旅游网站;
期望达到的效果是基本框架和**百度旅游**网站的页面差不多，以及关于一个目的地的著名景点的列表页差不多  
!()[https://lvyou.baidu.com/guigang/jingdian]

---
>##2.页面结构说明
网站由4个页面组成，包括：

* [首页](首页.html)既导航页
* [著名景点](著名景点.html) 列表页，简单介绍一些著名景点
* [桂平西山](桂平西山.html) 详细页，详细介绍**桂平西山**这个景点
* [个人信息](个人信息.html) 表单页，作用是提供有兴趣者报名前往旅游

---
>##3.技术指标
* 兼容主流浏览器，IE8+
* 使用HTML4,CSS2,Javascript,
* 开发工具：Chrome,Sublime Text及其插件。

---
>##4.技术难点说明
>>####4.1首页头部使用jQuery轮播图
该动态效果需要引入jquery和xSlider.js文件：
```
<script type="text/javascript"src="http://cdn.bootcss.com/jquery/1.11.0/jquery.min.js"></script>
<script type="text/javascript"src="http://demo.htmleaf.com/1704/201704251459/js/xSlider.js"></script>
```
>>而且后面还要对该轮播图插件进行初始化，需使用 xSlider()方法来初始化该轮播图插件。
xSlider()方法运用以及一些参数配置如下：
```
 <script type="text/javascript">
        $('.slider').xSlider({
      // slider width
      w: 1200,
      // current slide
      current: 0,
      // animation speed
      speed: 500,
      // autoplay interval
      intervalTime: 5000
    });
    </script>
```
 可以根据具体效果来改变参数值。
>>####4.2列表页对图片的处理
难点：如何对图片进行横向排列，既左边以一张图片为单位，而右边的则以一列图为单位。
解决方法：主要利用到**div**盒子和浮动**float**
步骤一：首先对左边的每一张图片都设置一个div，然后向左浮动，但是一行需要放多少张图片就得在第几张图的下一张图消除浮动{style="clear:both;"},比如我的是一行三张图片，所以在第四张图片就要消除浮动，然后再对两边的图片分别加一个div在浮动一下就好，**补充一点**：对于图片的间距可以使用“margin”；
主要代码如下
左边图片：
```
float:left;
margin: auto 20px;
```
右边图片：
```
float:right;
 	border:2px solid lightgrey;
 	padding:auto 5px;
 	margin-left: 10px;
 	margin: auto 20px; 
``` 	

>>####4.3详细页关于图片五角星的效果
原图是![](ico_jd_top.png),我们只需要10号的五个五角星的4个半，难点：1.如何定位到五颗五角星，2.如何截取五颗五角星中的四颗半。解决方法如下：
引入一个css样式，首先需要定位，然后设计那部分图片隐藏，具体代码如下：
```
position: absolute;
background-image: url(https://gss0.bdstatic.com/8KIPcyv9KgQIm2_p8IuM_a/static/destination/widget/public/star/img/star-2x_e79e4de.png);
background-origin: padding-box;
background-position: 0px -17px;	background-size: 100px;
height: 16px;
width: 92px;
```
 具体参数需要根据效果来不断调试。
>##5.开发心得
>>####5.1开发过程的总结
整个网站大约耗时7个星期，在制作过程中就是对老师的教的知识运用，还有自学过程，最重要的一点是要动手去尝试，而且要学会思考，对老师讲的内容不仅要会吸收，还要会运用，在制作网站时，应该一、先有一个明确的主题；二、要有一个基本框架，三就是基本内容；最后四、就是加特效。
>>####5.2对本课程的展望与感想
这门课和老师教给我很多很多实用的东西，让我对计算机以及web前端开发有了更深刻的理解，这门课也是我最上心的一门课，这门课和老师真的很棒。希望以后老师能教我更多的东西。


 
 







