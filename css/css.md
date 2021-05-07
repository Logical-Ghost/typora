# css

  + 层叠样式

  + 网页实际上是一个多层的结构，通过css可以分别为网页的每一个层来设置样式

    而最终我们能看到的只是网页最上边一层

+ 总之一句话，css用来设置网页中元素的样式

### 内联，内部，外联样式表

#### 内联样式表

<img src="./images./内联，内部，外联样式表./1.png" style="zoom: 50%; margin-left: 0px;" >

<img src="./images./内联，内部，外联样式表./2.png" style="zoom: 50%; margin-left: 0px;" >
css 属性的值 也遵循名值对结构（属性名对应属性值，中间用:隔开 ，结尾用;）
内联样式在开发的时候**尽量不使用**

#### 内部样式表

只对一个页面起作用，不能跨页面使用

<img src="./images./内联，内部，外联样式表./3.png" style="zoom: 50%; margin-left: 0px;" >

#### 外部样式表

<img src="./images./内联，内部，外联样式表./4.png" style="zoom: 50%; margin-left: 0px;" >

<img src="./images./内联，内部，外联样式表./5.png" style="zoom: 50%; margin-left: 0px;" >

在**style标签**里面是一个特殊的区域 遵守的是css的规范 和html不一样
		/* */   css中的注释
<img src="./images./内联，内部，外联样式表./6.png" style="zoom: 50%; margin-left: 0px;" >



### 选择器

#### 元素选择器

<img src="./images./css选择器./1.png" style="zoom: 50%; margin-left: 0px;" >

<img src="./images./css选择器./2.png" style="zoom: 50%; margin-left: 0px;" >

#### id选择器

**（id不能重复）** **虽然id可能可以相同但是 不能写，因为后面可能出现其他问题**

<img src="./images./css选择器./3.png" style="zoom: 50%; margin-left: 0px;" >

<img src="./images./css选择器./4.png" style="zoom: 50%; margin-left: 0px;" >

####   class选择器

**开发的时候大多数都用这个选择器**

<img src="./images./css选择器./5.png" style="zoom: 50%; margin-left: 0px;" >

<img src="./images./css选择器./6.png" style="zoom: 50%; margin-left: 0px;" >

多个class属性的 值之间用空格隔开
<img src="./images./css选择器./7.png" style="zoom: 50%; margin-left: 0px;" >



#### **通配选择器**

所有选择器有一个算一个
<img src="./images./css选择器./8.png" style="zoom: 50%; margin-left: 0px;" >

#### **交集选择器**

<img src="./images./css选择器./9.png" style="zoom: 50%; margin-left: 0px;" >
div#box1{} 不建议这么使用，因为id为box1 本就是唯一的。

#### 选择器分组

<img src="./images/css选择器/10.png " style="zoom:67%;margin-left:0px" >

#### 子元素选择器

<img src="./images/css选择器/11.png " style="zoom:67%;margin-left:0px" >

<img src="./images/css选择器/12.png " style="zoom:67%;margin-left:0px" >
div元素的子元素span（我是div中的span元素）将变成橙色

<img src="./images/css选择器/13.png " style="zoom:67%;margin-left:0px" >
将会把满足 元素为div 和 class为box 的元素的 子元素span变成橙色

#### 后代元素选择器

<img src="./images/css选择器/14.png " style="zoom: 50%; margin-left: 0px;" >
div元素下 的span元素变色

#### 兄弟元素选择器

<img src="./images/css选择器/15.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/16.png " style="zoom: 67%; margin-left: 0px;" >
这个时候下一个兄弟不会变色，因为span没有紧贴p元素





<img src="./images/css选择器/17.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/18.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/19.png " style="zoom: 67%; margin-left: 0px;" >
p元素下面所有的span元素边红色，在p元素上边的span元素不变

#### 属性选择器

<img src="./images/css选择器/20.png " style="zoom: 67%; margin-left: 0px;" >
p[title]{color:orange}  //表示p元素 且含有title属性 的变成橙色
[title]{color:orange}  //表示 含有title属性 的变成橙色

<img src="./images/css选择器/21.png " style="zoom: 67%; margin-left: 0px;" >
p[title="abc"]{color:orange}  //表示p元素 含有title属性 其属性值为abc 的变成橙色

<img src="./images/css选择器/22.png " style="zoom: 67%; margin-left: 0px;" >
p[title^="abc"]{color:orange}  //表示p元素 含有title属性 其属性值**开头**为abc 的变成橙色

<img src="./images/css选择器/23.png " style="zoom: 67%; margin-left: 0px;" >
p[title$="abc"]{color:orange}  //表示p元素 含有title属性 其属性值**结尾**为abc 的变成橙色

<img src="./images/css选择器/24.png " style="zoom: 67%; margin-left: 0px;" >
p[title*="abc"]{color:orange}  //表示p元素 含有title属性 其属性值**含有**abc 的变成橙色

#### 伪类选择器

<img src="./images/css选择器/25.png " style="zoom: 67%; margin-left: 0px;" >
odd 基数
even 偶数

<img src="./images/css选择器/26.png " style="zoom: 67%; margin-left: 0px;" >
以上这些伪类都是根据所有的子元素进行排序，就是ul下所有子元素进行排序

以<img src="./images/css选择器/27.png " style="zoom: 67%; margin-left: 0px;" >为例子，如果ul下第一个子元素不是li 那么这个红色的效果就没有用



<img src="./images/css选择器/28.png " style="zoom: 67%; margin-left: 0px;" ><img src="./images/css选择器/29.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/30.png " style="zoom: 67%; margin-left: 0px;" >
nth-child(4)没有效果，nth-childe(5)有效果（<li>4</li>变色）

<img src="./images/css选择器/31.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/32.png " style="zoom: 67%; margin-left: 0px;" >
这些伪类是根据ul元素的 子元素li 进行排序，找到第一个li子元素后有红色效果

<img src="./images/css选择器/33.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/34.png " style="zoom: 67%; margin-left: 0px;" >
ul元素下的 第三个子元素 没有使用效果

<img src="./images/css选择器/35.png " style="zoom: 67%; margin-left: 0px;" >
ul元素下 第三个li子元素 没有使用效果

**超链接的伪类**

<img src="./images/css选择器/36.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/37.png " style="zoom: 67%; margin-left: 0px;" >
link和visited是超链接独有的

<img src="./images/css选择器/38.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/39.png " style="zoom: 67%; margin-left: 0px;" >
hover和active其他元素 都有

focus伪类选择器
元素获取焦点时（比如鼠标点击文本框时）

#### 伪元素

伪元素是一个行内元素

<img src="./images/css选择器/40.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/41.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/42.png " style="zoom: 67%; margin-left: 0px;" >
::before和::after在网页中挺常见 content记得带引号

#### 样式的继承，优先级冲突

<img src="./images/css选择器/43.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/44.png " style="zoom: 67%; margin-left: 0px;" >

``` css
//例如：
	background-color:red !important;
```



### 长度，颜色单位

#### 长度单位

**当元素设置了绝对定位以后，脱离的文档流他的width:50% 是根据它的包含块来设定的（height也是一样的）**

<img src="./images/长度，颜色单位/1.png " style="zoom: 67%; margin-left: 0px;" >

效果
<img src="./images/长度，颜色单位/2.png " style="zoom: 33%; margin-left: 0px;" >

**两个长度单位**
默认情况下1em=16px;
				  1rem=16px;

<img src="./images/长度，颜色单位/3.png " style="zoom: 67%; margin-left: 0px;" >
em是参照于自身的字体大小（及当前元素的字体大小)
rem是参照与根元素的字体大小

#### **颜色单位**

<img src="./images/长度，颜色单位/4.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/长度，颜色单位/5.png " style="zoom: 67%; margin-left: 0px;" >

HSL值（调颜色的，用的不是特别多）
<img src="./images/长度，颜色单位/6.png " style="zoom: 67%; margin-left: 0px;" >

#### 文档流中的块元素和行内元素

<img src="./images/文档流，盒子模型/1.png " style="zoom: 67%; margin-left: 0px;" >

### 盒子模型

<img src="./images/文档流，盒子模型/2.png " style="zoom: 67%; margin-left: 0px;" >

#### 内容区

<img src="./images/文档流，盒子模型/3.png " style="zoom: 67%; margin-left: 0px;" >

#### 边框

<img src="./images/文档流，盒子模型/4.png " style="zoom: 50%; margin-left: 0px;" >

##### 边框像素

<img src="./images/文档流，盒子模型/5.png " style="zoom: 67%; margin-left: 0px;" >

边框像素设置 例如： 
<img src="./images/文档流，盒子模型/6.png " style="zoom: 67%; margin-left: 0px;" >

##### 边框颜色

<img src="./images/文档流，盒子模型/7.png " style="zoom: 67%; margin-left: 0px;" >

##### 边框样式

<img src="./images/文档流，盒子模型/8.png " style="zoom: 67%; margin-left: 0px;" >

##### 边框的主要写法

<img src="./images/文档流，盒子模型/9.png " style="zoom: 67%; margin-left: 0px;" >

#### 内边距

<img src="./images/文档流，盒子模型/10.png " style="zoom: 67%; margin-left: 0px;" >

总结一下 ：盒子其实就是把一个元素放进去，然后又这个元素设置css 进行对外的扩充，
延伸出内边距和边框，该元素背景颜色的设置会延伸到内边距上，所以需要给那个元素
增加一个子元素，通过子元素颜色的改变 来体现出内边距和元素内容的区别， 整个盒子
的大小由边框（border） 内边距（padding） 内容（content）决定

我们说的盒子 一般都指的是盒子的可见框

#### 外边距

<img src="./images/文档流，盒子模型/11.png " style="zoom: 67%; margin-left: 0px;" >

简写
<img src="./images/文档流，盒子模型/12.png " style="zoom: 67%; margin-left: 0px;" >

#### **盒子模型水平方向**

<img src="./images/文档流，盒子模型/13.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/文档流，盒子模型/14.png " style="zoom: 50%; margin-left: 0px;" >

**==注意点==**

​	1.<img src="./images/文档流，盒子模型/15.png " style="zoom: 67%; margin-left: 0px;" >

​	2.<img src="./images/文档流，盒子模型/16.png " style="zoom: 67%; margin-left: 0px;" >

​	3.<img src="./images/文档流，盒子模型/17.png " style="zoom: 50%; margin-left: 0px;" >

​	4.**如果width的值没有设置，那么它的值就是auto**
​		

#### **垂直方向上的布局**

<img src="./images/文档流，盒子模型/18.png " style="zoom: 50%; margin-left: 0px;" >

#### 外边距的折叠问题

<img src="./images/文档流，盒子模型/19.png " style="zoom: 50%; margin-left: 0px;" >

解决父子元素间垂直外边距的方法
1.不要用外边距
2.使用外边框，将父子元素的外边距隔开了

#### 行内元素的盒模型

<img src="./images/文档流，盒子模型/20.png " style="zoom: 50%; margin-left: 0px;" >
总结就是行内元素 只能改变水平方向上的布局，垂直方向上的布局不能改变

#### 属性，以及去除默认样式

##### text-decoration

去除下划线
<img src="./images/某些属性，去除默认样式/10.png " style="zoom: 50%; margin-left: 0px;" >

##### font-weight

文字加粗
<img src="./images/某些属性，去除默认样式/11.png " style="zoom: 50%; margin-left: 0px;" >

##### background-color 
**属性的有效范围只在盒子的可见框内，****可见框外（margin）不会有颜色的**

##### line-height 

若要想把一个文字在父元素中设置垂直居中，需要将父元素的line-height设置为一个和父元素的height相同的高度

<img src="./images/某些属性，去除默认样式/9.png " style="zoom: 50%; margin-left: 0px;" >

##### border-radius 

设置边框的圆角半径

<img src="./images/某些属性，去除默认样式/8.png " style="zoom: 50%; margin-left: 0px;" >

##### box-shadow

不会影响到布局，该属性最好4个值都写出来

<img src="./images/某些属性，去除默认样式/7.png " style="zoom: 50%; margin-left: 0px;" >

##### outline

outline属性不会影响到页面布局

<img src="./images/某些属性，去除默认样式/6.png " style="zoom: 50%; margin-left: 0px;" >

##### box-sizing

​		属性值：content-box 高度和宽度为内容区大小
​					   border-box  高度和宽度为盒子可见框大小	

<img src="./images/某些属性，去除默认样式/5.png " style="zoom: 50%; margin-left: 0px;" >

##### display，visibility

display 可以将行内元素显示成块元素
			 将块元素显示成行内元素(一般不这么做)

inline-block属性值   行内块元素
因为存在换行
<img src="./images/某些属性，去除默认样式/12.png " style="zoom: 50%; margin-left: 0px;" >
所以会导致元素之间会存在间隙
<img src="./images/某些属性，去除默认样式/13.png " style="zoom: 50%; margin-left: 0px;" >

将换行删掉就可以 使间隙消失了
<img src="./images/某些属性，去除默认样式/14.png " style="zoom: 50%; margin-left: 0px;" >

但还是尽量不要使用inline-block

none 属性值
使得元素消失 不占据原先的位置

visibility 设置元素的可见性

hidden 属性值
使得元素消失 但占据原先的位置

<img src="./images/某些属性，去除默认样式/2.png " style="zoom: 50%; margin-left: 0px;" >



##### 去除默认样式

通常在PC端会去除掉 浏览器的默认样式
<img src="./images/某些属性，去除默认样式/1.png " style="zoom: 50%; margin-left: 0px;" >

使用<img src="./images/某些属性，去除默认样式/3.png " style="zoom: 50%; margin-left: 0px;" >或者<img src="./images/某些属性，去除默认样式/4.png " style="zoom: 50%; margin-left: 0px;" >
去除默认样式，使用reset.css 比较多一些

使用 list-style:none;去除项目符号



### 浮动

#### 浮动

<img src="./images/浮动以及浮动塌陷/1.png " style="zoom: 50%; margin-left: 0px;" >
元素浮动以后虽然该元素的水平布局等式不会成立了，但是它的子元素（块元素)水平布局的等式还是会成立的

<img src="./images/浮动以及浮动塌陷/2.png " style="zoom: 50%; margin-left: 0px;" >
第六点 1，2，3是兄弟元素，所以即使3上面有空间，它也不会超过“2”兄弟元素

<img src="./images/浮动以及浮动塌陷/3.png " style="zoom: 50%; margin-left: 0px;" >
使用 float属性设置浮动 属性值right或left，会移动到父元素的右边或者左边，但不会移出父元素

<img src="./images/浮动以及浮动塌陷/4.png " style="zoom: 50%; margin-left: 0px;" >
浮动元素不会盖住文字，文字会自动环绕在浮动元素周围

#### 元素脱离文档流的特点

<img src="./images/浮动以及浮动塌陷/5.png " style="zoom: 50%; margin-left: 0px;" >



#### 高度塌陷

高度塌陷
<img src="./images/浮动以及浮动塌陷/6.png " style="zoom: 50%; margin-left: 0px;" >

解决办法：

①开启BFC
**使用overflow属性的 auto或hidden值可以解决（副作用比较小）**从而开启BFC
<img src="./images/浮动以及浮动塌陷/7.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/浮动以及浮动塌陷/8.png " style="zoom: 50%; margin-left: 0px;" >

②最终版本解决高度塌陷和外边距重叠

<img src="./images/浮动以及浮动塌陷/10.png " style="zoom: 50%; margin-left: 0px;" >

clear属性
<img src="./images/浮动以及浮动塌陷/9.png " style="zoom: 50%; margin-left: 0px;" >



### 定位

#### 定位 

<img src="./images/定位/1.png " style="zoom: 50%; margin-left: 0px;" >

#### 相对定位

``` css
position:relative;
```

定位位置指的是其本来的所在的位置

<img src="./images/定位/2.png " style="zoom: 50%; margin-left: 0px;" >

#### 绝对定位

``` css
position:absolute;
```

绝对定位元素是相对于其包含块进行定位的 
<img src="./images/定位/3.png " style="zoom: 50%; margin-left: 0px;" >

#### 固定定位

**position:fixed**

其他特点都和绝对定位相同，固定定位永远参照于视口定位，就是滚动条拉动 它也固定在哪个位置不动

<img src="./images/定位/4.png " style="zoom: 50%; margin-left: 0px;" >

#### 粘滞定位

**position:sticky**

<img src="./images/定位/5.png " style="zoom: 50%; margin-left: 0px;" > 
粘滞定位是相对于包含块而言的
兼容性不好

#### 水平布局等式的改变

开启绝对定位以后
<img src="./images/定位/6.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/定位/7.png " style="zoom: 50%; margin-left: 0px;" >

#### 垂直方向上的等式

<img src="./images/定位/8.png " style="zoom: 50%; margin-left: 0px;" >

#### 定位元素的层级设定

开启了定位的元素 可以通过 **z-index** 设置元素的层级 
<img src="./images/定位/9.png " style="zoom: 50%; margin-left: 0px;" >

### 字体

#### 字体族

<img src="./images/字体/1.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/字体/2.png " style="zoom: 50%; margin-left: 0px;" >
最后一个字体兜底

提供服务器里的字体直接给用户使用 （注意版权问题）
<img src="./images/字体/3.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/字体/4.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/字体/5.png " style="zoom: 50%; margin-left: 0px;" >

使用@font-face可能会有三个问题

①加载速度
②版权
③字体格式

#### 图标字体

​	字体库
​	<img src="./images/字体/6.png " style="zoom: 50%; margin-left: 0px;" >

​	图标字体

​	<img src="./images/字体/7.png " style="zoom: 50%; margin-left: 0px;" >

​	<img src="./images/字体/8.png " style="zoom: 50%; margin-left: 0px;" >

​	将all.css引入到网页
​	<img src="./images/字体/9.png " style="zoom: 50%; margin-left: 0px;" >
​	使用方法
​	①内联样式
​	<img src="./images/字体/10.png " style="zoom: 50%; margin-left: 0px;" >
​	class="fas ???"
​	class="fab ???" 
​	???里面的需要到文档里面找

​	②伪元素设置图标字体
​	<img src="./images/字体/11.png " style="zoom: 50%; margin-left: 0px;" >
​	content:'\???'
​	???中的内容去这里面找
​	<img src="./images/字体/12.png " style="zoom: 33%; margin-left: 0px;" >
​	
​	③通过实体来设置图标字体
​	<img src="./images/字体/13.png " style="zoom: 50%; margin-left: 0px;" >
​	class="fas"或"fab
​	然后&#???x; ???中的内容去下图中找
​	<img src="./images/字体/14.png " style="zoom: 50%; margin-left: 0px;" >

​	④百度 [Iconfont](http://www.baidu.com/link?url=o756F3IJ2w2znv4cT6GGHRBmRr2yxUVxg0vLMYLxtCtWpAXcDzd7phAUUEKbcFYE) 有功能更全的图标字体

#### 行高，字体框

行高指的文字占有的实际高度，可以使单行文字在一个元素中垂直居中
字体框 指的是字体存在的格子高度，就是font-size的值 
<img src="./images/字体/15.png " style="zoom: 50%; margin-left: 0px;" >

#### 字体相关属性

<img src="./images/字体/16.png " style="zoom: 50%; margin-left: 0px;" >

简写
<img src="./images/字体/17.png " style="zoom: 50%; margin-left: 0px;" >

还可以在前面加上 字重 和风格
<img src="./images/字体/18.png " style="zoom: 50%; margin-left: 0px;" >

font:normal normal 50px/normal serif;
不写 相当于写了默认值;

单独设置字重 以及风格
<img src="./images/字体/19.png " style="zoom: 50%; margin-left: 0px;" >

#### 文本相关的样式

##### text-align(水平对齐)

text-align ：left，right，center，justify

<img src="./images/字体/20.png " style="zoom: 50%; margin-left: 0px;" >

##### vertical-align(垂直对齐)  

不同元素之间的垂直对齐

<img src="./images/字体/21.png " style="zoom: 50%; margin-left: 0px;" >

当插入图片的时候
外边框和图片之间有一条缝隙，因为图片是按照基线对齐的，为解决
这个问题
<img src="./images/字体/22.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/字体/23.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/字体/24.png " style="zoom: 50%; margin-left: 0px;" >

##### text-decoration(文本修饰)

<img src="./images/字体/25.png " style="zoom: 50%; margin-left: 0px;" >
红色，下划线，虚线 （但是ie 不兼容 这么写）
<img src="./images/字体/26.png " style="zoom: 50%; margin-left: 0px;" >

##### white-space(处理空白)

属性值：pre 保留元素内文字原有的格式（换行，空格等)

<img src="./images/字体/27.png " style="zoom: 50%; margin-left: 0px;" >

##### 设置省略号

<img src="./images/字体/28.png " style="zoom: 50%; margin-left: 0px;" >
出现省略号的<img src="./images/字体/29.png " style="zoom: 50%; margin-left: 0px;" >效果
四个条件缺一不可

##### 隐藏文字

text-indent:-99999px;   

### 背景属性

#### background-color（背景色）

<img src="./images/背景/1.png " style="zoom: 50%; margin-left: 0px;" >

#### **background-repeat**（背景重复方式）

<img src="./images/背景/2.png " style="zoom: 50%; margin-left: 0px;" >

#### background-position（背景图片位置）

设置背景图片在背景元素中的位置

①通过方位词设置图片位置
<img src="./images/背景/3.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/背景/4.png " style="zoom: 50%; margin-left: 0px;" >

②通过偏移量来设置图片的位置
<img src="./images/背景/5.png " style="zoom: 50%; margin-left: 0px;" >

#### background-clip（背景占盒子模型的范围）

#### background-origin(背景图片偏移量计算的原点)

<img src="./images/背景/6.png " style="zoom: 50%; margin-left: 0px;" >

#### background-size（设置背景图片的大小）

<img src="./images/背景/7.png " style="zoom: 50%; margin-left: 0px;" >

#### 滚动条问题

子元素比父元素大，设置滚动条后

<img src="./images/背景/8.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/背景/9.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/背景/10.png " style="zoom: 50%; margin-left: 0px;" >
box1 的背景图片不会移动
但是box2 的背景图片会跟着滚动条移动（就是滚动条往下拉，猫会往上走 然后消失）

#### background-attachment（固定背景图片）

<img src="./images/背景/11.png " style="zoom: 50%; margin-left: 0px;" >
当给box2设置 background-attachment:fixed;  后上图的猫就不会跟着滚动条移动了

#### 背景属性简写

 <img src="./images/背景/12.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/背景/13.png " style="zoom: 50%; margin-left: 0px;" >

#### 雪碧图

**雪碧图**（也叫精灵图 css-sprite）
解决图片闪烁的问题
<img src="./images/背景/14.png " style="zoom: 50%; margin-left: 0px;" >

#### 渐变

①
linear-gradient()属性值

渐变是背景图片不是颜色
使用 background-image 属性来设置
属性值 linear-gradient（) 和 repeating-linear-gradient（）
<img src="./images/背景/15.png " style="zoom: 50%; margin-left: 0px;" >
repeating-linear-gradient属性值 的意思是 重复开始渐变 到结束渐变 中间这一段过程

background-image:linear-gradient(to right,red,yellow);
background-repeat:no-repeat;	//对渐变没有作用

②radial-gradient()

<img src="./images/背景/16.png " style="zoom: 50%; margin-left: 0px;" >

### 表格

table是块元素

#### rowspan,colspan属性

rowspan属性 用来纵向合并单元格 （前提是被合并的那个得是 没有的）
colspan属性  横向合并单元格 （前提是被合并的那个得是 没有的）

<img src="./images/表格/1.png " style="zoom: 50%; margin-left: 0px;" >

#### thead，tbody，tfoot

然后再在thead，tbody，tfoot 标签内写<tr><td></td></tr>
<img src="./images/表格/2.png " style="zoom: 50%; margin-left: 0px;" >

#### 小问题

如果表格中没有使用tbody而是直接使用tr  
那么浏览器会自动创建一个tbody，并且将tr全都放到tbody  
所以tr不是table的子元素了

#### 表格的样式

##### border-spacing（指定边框的距离）

<img src="./images/表格/3.png " style="zoom: 50%; margin-left: 0px;" >

##### border-collapse（合并边框）

<img src="./images/表格/4.png " style="zoom: 50%; margin-left: 0px;" >

#### td标签的特性

默认情况下元素在td中是垂直居中的
可以通过vertical-align(垂直) 和 text-align(水平)去调文元素（文字，图片，等等）在td中的位置
其他标签下只能控制文字  td有些特殊

#### 元素垂直居中

可以在父元素中设置
display:table-cell 
vertical-align:middle
使元素设置成单元格然后 从而使得子元素在父元素中垂直居中
<img src="./images/表格/5.png " style="zoom: 50%; margin-left: 0px;" >

### 表单

#### form标签(创建表单)

<img src="./images/表单/1.png " style="zoom: 50%; margin-left: 0px;" >

form标签的 action 属性
<img src="./images/表单/2.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/表单/3.png " style="zoom: 50%; margin-left: 0px;" >

#### form表单内的表单项

##### 文本框

**标签input  属性type="text"**
注意数据如果要**提交到服务器**，必须要为元素指定一个==name==属性值
<img src="./images/表单/4.png " style="zoom: 50%; margin-left: 0px;" >

##### 密码框

**标签input 属性type="password"**
<img src="./images/表单/5.png " style="zoom: 50%; margin-left: 0px;" >

##### 单选按钮

必须要指定一个value属性，属性值最终会作为用户填写的值传递给服务器
单选框的name属性值要写 一样的不然两个单选框就都能亮了
checked属性 将改单选按钮设置为默认选项
<img src="./images/表单/6.png " style="zoom: 50%; margin-left: 0px;" >

##### 多选框

<img src="./images/表单/7.png " style="zoom: 50%; margin-left: 0px;" >

##### 下拉列表

select标签
<img src="./images/表单/8.png " style="zoom: 50%; margin-left: 0px;" >

##### 提交按钮

标签input 属性type="submit"
<img src="./images/表单/9.png " style="zoom: 50%; margin-left: 0px;" >

##### 重置按钮，普通按钮

普通按钮(这个按钮用的比较多，因为这个按钮按下去没有任何效果
所以后期可以通过js添加很多东西)

<img src="./images/表单/10.png " style="zoom: 50%; margin-left: 0px;" >

##### 提交,重置,普通按钮

**好像用成对出现的标签比较多，因为可以添加图片之类的**
<img src="./images/表单/11.png " style="zoom: 50%; margin-left: 0px;" >

##### 标签内的属性

###### autocomplete自动补全

autocomplete="off" 关闭自动补全
autocomplete="on" 打开自动补全，有点类似于历史记录，打开的时候会显示以前写过的
<img src="./images/表单/12.png " style="zoom: 50%; margin-left: 0px;" >
整个表单都会取消自动补全

###### readonly只读

<img src="./images/表单/13.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/表单/14.png " style="zoom: 50%; margin-left: 0px;" >

###### disabled禁用

<img src="./images/表单/15.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/表单/16.png " style="zoom: 50%; margin-left: 0px;" >

###### autofocus焦点

<img src="./images/表单/17.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/表单/18.png " style="zoom: 50%; margin-left: 0px;" >

### 三角形的制作

<img src="./images/三角形/1.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/三角形/2.png " style="zoom: 50%; margin-left: 0px;" >

### 网站图标的设置

设置网站的图标（在标题栏和收藏栏）

​		网站图标一般都存储在网站的根目录下，名字一般都叫做favicon.ico

<img src="./images/网站的图标/1.png " style="zoom: 50%; margin-left: 0px;" >

``` html
<link rel="icon" href="./favicon.ico">  //引入图标
```



### 过渡，动画，变形

#### 过渡（**transition**）

<img src="./images/过渡，动画，变形/1.png " style="zoom: 50%; margin-left: 0px;" >

##### **transition-property**

属性值：left，right，all等等
<img src="./images/过渡，动画，变形/2.png " style="zoom: 50%; margin-left: 0px;" >

##### transition-duration

**它的值 为s 或者ms（单位） 指的是过渡的时间**
<img src="./images/过渡，动画，变形/3.png " style="zoom: 50%; margin-left: 0px;" >

##### **transition-timing-function**

属性值 ease(默认)，linear，ease-in，ease-out，ease-in-out，cubic-bezier()，steps
cubic-bezier() 值得获取需要看**[https://cubic-bezier.com/](https://cubic-bezier.com/#.17,.67,.83,.67) **网站
<img src="./images/过渡，动画，变形/4.png " style="zoom: 50%; margin-left: 0px;" >

##### **transition-delay**

<img src="./images/过渡，动画，变形/5.png " style="zoom: 50%; margin-left: 0px;" >

##### transition

可以设置过渡相关的所有属性，只有一个要求，如果要写延迟的话
则两个时间中 **持续时间**先写前面**延迟时间**写在后面。
<img src="./images/过渡，动画，变形/6.png " style="zoom: 50%; margin-left: 0px;" >

#### 动画（animation）

与过渡的区别，自触发的
<img src="./images/过渡，动画，变形/7.png " style="zoom: 50%; margin-left: 0px;" >

##### @keyframes

**需要在style里面设置（不在元素的css类里面） @keyframes+名字**
<img src="./images/过渡，动画，变形/8.png " style="zoom: 50%; margin-left: 0px;" >

关键帧内的位置还可以使用%来表示

``` html
<stytle>
@keyframes ball{
	0%{
    	animation-timing-function: ease-in; //指的时从0%到50% 这一段内使用ease-in时序函数
		}
    50%{
    
    	}
    100%{
    
    	}
}
 </stytle>
```



##### **animation-name**

这个一定要设置，不然无效的
<img src="./images/过渡，动画，变形/9.png " style="zoom: 50%; margin-left: 0px;" >

##### **animation-duration**

动画执行的时间，也要设置
<img src="./images/过渡，动画，变形/10.png " style="zoom: 50%; margin-left: 0px;" >

##### **animation-delay**，**animation-timing-function**

动画延迟和时序函数
<img src="./images/过渡，动画，变形/11.png " style="zoom: 50%; margin-left: 0px;" >

##### **animation-interation-count**

动画执行次数
<img src="./images/过渡，动画，变形/12.png " style="zoom: 50%; margin-left: 0px;" >

##### **animation-direction**

指定动画运行的方向
<img src="./images/过渡，动画，变形/13.png " style="zoom: 50%; margin-left: 0px;" >

##### **animation-play-state**

设置动画的执行状态（paused好像和伪类hover连用的）
<img src="./images/过渡，动画，变形/14.png " style="zoom: 50%; margin-left: 0px;" >

##### **animation-fill-mode**

动画的填充模式
<img src="./images/过渡，动画，变形/15.png " style="zoom: 50%; margin-left: 0px;" >
backwards值 指的是元素在一开始就处于from所显示 的状态

##### animation

<img src="./images/过渡，动画，变形/16.png " style="zoom: 50%; margin-left: 0px;" >
简写值时 两个时间的顺序： 执行时间  延迟时间

#### 变形（transform）

==**一个元素只会有一个transform生效，后面一个transform属性会把前面那个覆盖掉**==

##### translate(平移函数)

变形 **transform,**变形不会改变页面布局
样式值:translateX()；translateY()；translateZ()；
<img src="./images/过渡，动画，变形/17.png " style="zoom: 50%; margin-left: 0px;" >

##### perspective

**transform:translateZ() ** 需要设置视距才能体现
网页不支持透视，所以需要设置视距(网页到人眼的距离)

body大小需要设置边框才能看见，设置背景色会延伸到html根标签上面
<img src="./images/过渡，动画，变形/21.png " style="zoom: 50%; margin-left: 0px;" >

##### 元素居中(大小不确定)		

用绝对定位后 它的水平垂直居中 只能适用于元素大小确定的
元素大小没有设置时 width 和 height 默认值时auto 为了满足等式会扩大 而不会进行移动
<img src="./images/过渡，动画，变形/18.png " style="zoom: 50%; margin-left: 0px;" >

**可以使用transform:translateX() translateY() 去实现元素大小不确定的 在页面中居中**
<img src="./images/过渡，动画，变形/19.png " style="zoom: 50%; margin-left: 0px;" >

##### 鼠标经过后 浮出效果

<img src="./images/过渡，动画，变形/20.png " style="zoom: 50%; margin-left: 0px;" >

##### rotate(旋转函数)

**transform:rotateZ(），rotateY()，rotateZ() 旋转角度**
backface-visibility:hidden; 设置元素背面可见
<img src="./images/过渡，动画，变形/22.png " style="zoom: 50%; margin-left: 0px;" >

``` html
transform:rotateY(180deg) translateZ(400px);//先旋转，再平移， 离我们远了
transform:translateZ(400px) rotateY(180deg);//先平移，再在旋转， 离我们近了
```

改变旋转的原点
transform-origin属性 改变变形的原点
transform-origin:left center;

##### 立方体效果

opacity样式 设置元素的透明效果
<img src="./images/过渡，动画，变形/23.png " style="zoom: 50%; margin-left: 0px;" >
opacity无法兼容ie8
兼容ie8的透明
filter:alpha(opacity=50)

给元素设置3D效果

``` html
transform-style: preserve-3d;
```

立方体旋转
<img src="./images/过渡，动画，变形/24.jpg " style="zoom: 50%; margin-left: 0px;" >

##### 元素的缩放

实现图片再固定大小内的放大缩小
<img src="./images/gif/3.gif " style="zoom: 50%; margin-left: 0px;" >

``` html
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <style>
        .img-wrapper {
            width: 100px;
            height: 100px;
            margin: 100px auto;
            overflow: hidden;
            border: 1px solid black;

        }
        .img-wrapper:hover img{
            transform: scale(1.1);
        }
        .img-wrapper img{
            width: 100px;
            transition: .1s;

        }
    </style>
</head>

<body>
    <div class="img-wrapper">
        <img src="./images/dahuangmao-11.png" alt="">
    </div>
</body>

</html>
```

对元素进行缩放
transform:scale()
scaleX()
scaleY()
scaleZ() //如果想要体现出这个效果必须 实现3D的效果
scale()
<img src="./images/过渡，动画，变形/25.png " style="zoom: 50%; margin-left: 0px;" >

#### 思维导图
<img src="./images/过渡，动画，变形/26.png " style="zoom: 50%; margin-left: 0px;" >

### 代码的压缩

代码是要压缩的 目前使用下面的插件来实现 ，但是以后有更方便的。
使用按F1然后点击<img src="./images/css压缩/1.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/css压缩/2.png " style="zoom: 50%; margin-left: 0px;" >

### less

less 是css预处理语言
**需要下载插件 easy less 将less转换为css（在vs code中是这样的 在其他软件中不清楚）**
<img src="./images/less/1.png " style="zoom: 50%; margin-left: 0px;" >

#### 注释

less中的注释：
						// 单行注释不会被解析到css文件中
						/* */ 多行注释，会被解析到css文件中

#### 变量

##### 变量的声明

@变量名:变量值;
<img src="./images/less/2.png " style="zoom: 50%; margin-left: 0px;" >

##### 变量的使用

**使用变量时，如果直接使用变量则 @变量名的 形式就可以使用了**
<img src="./images/less/3.png " style="zoom: 50%; margin-left: 0px;" >

**作为类名，或者一部分值使用时必须以 @{变量名} 的形式使用**
<img src="./images/less/4.png " style="zoom: 50%; margin-left: 0px;" >
<img src="./images/less/5.png " style="zoom: 50%; margin-left: 0px;" >

**变量重名时，会优先使用比较近的变量**
可以在变量声明前使用变量//但不建议这么做
<img src="./images/less/6.png " style="zoom: 50%; margin-left: 0px;" >

height样式 引用width样式的值
<img src="./images/less/7.png " style="zoom: 50%; margin-left: 0px;" >

#### &符号的使用

<img src="./images/less/8.png " style="zoom: 50%; margin-left: 0px;" >

#### extend()的使用

<img src="./images/less/9.png " style="zoom: 50%; margin-left: 0px;" >

``` html
在css显示为
.p1,
.p2{
	width:100px;
	height:200px;
}
.p2{
	color:red;
}
```

#### mixins的使用

**创建mixins， mixins不会产生在css里面** 
<img src="./images/less/10.png " style="zoom: 50%; margin-left: 0px;" >

``` html
在css中显示
.p5{
	width:100px;
	height:100px;
	background-color:#bfa;
}
//此时相当于是对.p4样式的一个复制，会造成浪费
```

在mixins中可以直接设置变量

①按固定顺序传递参数

<img src="./images/less/11.png " style="zoom: 50%; margin-left: 0px;" >

②按指定顺序传递参数
<img src="./images/less/12.png " style="zoom: 50%; margin-left: 0px;" >

③使用默认值，传递值后使用该值
<img src="./images/less/13.png " style="zoom: 50%; margin-left: 0px;" >

#### 函数

color:average()    //取颜色得平均值
<img src="./images/less/14.png " style="zoom: 50%; margin-left: 0px;" >

darken(颜色,百分比) //加深当前颜色，变得更浓
<img src="./images/less/15.png " style="zoom: 50%; margin-left: 0px;" >

#### @import

<img src="./images/less/16.png " style="zoom: 50%; margin-left: 0px;" >
通过@import可以将其他的less引入到当前less中
从而实现 模块化管理

#### 检查网页代码→less代码

①

<img src="./images/less/17.png " style="zoom: 50%; margin-left: 0px;" >

②<img src="./images/less/18.png " style="zoom: 50%; margin-left: 0px;" >

③

<img src="./images/less/19.png " style="zoom: 50%; margin-left: 0px;" >

### 弹性盒

移动端用的比较多，pc端兼容性有些不好

<img src="./images/弹性盒/1.png " style="zoom: 50%; margin-left: 0px;" >

#### 弹性容器

 <img src="./images/弹性盒/2.png " style="zoom: 50%; margin-left: 0px;" >

#### 弹性元素

<img src="./images/弹性盒/3.png " style="zoom: 50%; margin-left: 0px;" >

#### 弹性容器的属性

##### 主轴与侧轴

主轴：弹性元素排列方向称为主轴
侧轴：与主轴垂直的称为侧轴

##### **flex-direction **（元素排列方式)

指定容器中弹性元素的排列方式
可选值：
            row ==默认值==，弹性元素在容器中水平排列（左向右）
                    —主轴 自左向右
            row-reverse 弹性元素在容器中反向水平排列(右向左）
                    —主轴 自右向左
            column 弹性元素在容器中纵向排列（上向下）
                    —主轴 自上向下
            column-reverse 弹性元素在容器中纵向排列(下向上）
                    —主轴 自下向上

##### **flex-wrap**(元素换行)

**设置是否自动换行**  // 例如当flex-shrink:0；的时候弹性元素超出盒子便会换行 
<img src="./images/弹性盒/5.png " style="zoom: 0%; margin-left: 0px;" >

##### **flex-flow**（flex-direction和flex-wrap结合）

例如：flex-flow:row nowrap; 

##### **justify-content**（主轴方向上空白分布)

可选值 flex-star,flex-end,center,space-around,space-evenly,space-between

###### felx-start 

元素沿主轴起边排列
<img src="./images/弹性盒/6.png " style="zoom: 50%; margin-left: 0px;" >

###### flex-end

元素沿主轴终边排列
<img src="./images/弹性盒/7.png " style="zoom: 50%; margin-left: 0px;" >

###### center

元素居中排列
<img src="./images/弹性盒/8.png " style="zoom: 50%; margin-left: 0px;" >

###### space-around

空白分布到元素两侧
<img src="./images/弹性盒/9.png " style="zoom: 50%; margin-left: 0px;" >

###### space-evenly

空白分布到元素一侧
<img src="./images/弹性盒/10.png " style="zoom: 50%; margin-left: 0px;" >

###### space-between

空白分布到元素间
<img src="./images/弹性盒/11.png " style="zoom: 50%; margin-left: 0px;" >

##### align-items(辅轴上的元素对齐)

左右元素间的关系

###### stretch

默认值，将元素的长度设置为相同的值
<img src="./images/弹性盒/12.png " style="zoom: 50%; margin-left: 0px;" >

###### flex-start

元素不会拉伸，沿着辅轴起边对齐
<img src="./images/弹性盒/13.png " style="zoom: 50%; margin-left: 0px;" >

###### flex-end 

沿着辅轴终边对齐
<img src="./images/弹性盒/14.png " style="zoom: 50%; margin-left: 0px;" >

###### center

居中对齐
<img src="./images/弹性盒/15.png " style="zoom: 50%; margin-left: 0px;" >

###### baseline基线对齐

##### align-content(辅轴上的空白分布)

align-content属性 的属性值和justify-content: 的属性值相对应，只不过从主轴变成了辅轴

##### 弹性元素在弹性盒内的居中对齐

align-content:center;
justify-content:center;

#### 弹性元素的属性

##### align-self(单独覆盖align-items)

<img src="./images/弹性盒/16.png " style="zoom: 80%; margin-left: 0px;" >

##### flex-grow与flex-shrink 

flex-grow 
指定弹性元素的伸展的系数   //默认值为0

flex-shrink 
指定弹性元素的收缩系数     //默认值为1

<img src="./images/弹性盒/4.png " style="zoom: 50%; margin-left: 0px;" >

##### flex-basis(元素的基础长度)

指定元素在主轴上的基础长度
<img src="./images/弹性盒/17.png " style="zoom: 80%; margin-left: 0px;" >

##### flex(增长+缩减+基础)

flex-grow,flex-shrink,flex-basis三个属性的结合
<img src="./images/弹性盒/18.png " style="zoom: 80%; margin-left: 0px;" >

##### order(元素的排列顺序)

属性值:数字
数字越小越排列在前

#### 思维导图

<img src="./images/弹性盒/flex思维导图.jpg " style="zoom: 80%; margin-left: 0px;" >

### 像素的问题

#### 物理像素和css像素

​	网页中的像素分为css像素和物理像素
​	css像素指的就是 我们编写网页的时候所说的像素
​	物理像素 就是屏幕上发光的小点点 然后用截图工具 量出来的都是物理像素

​	打开网页 它的视口宽度就是：html标签的盒模型 的宽度（css 像素）
 （在正常情况下，win10没有缩放，浏览器没有缩放的情况下 css像素个数=物理像素个数）	

​	<img src="./images/像素的问题/1.png " style="zoom: 50%; margin-left: 0px;" >

​	在不同的屏幕，单位像素的大小是不同的，像素越小（寸/物理像素)越清晰
​	这里的24寸指的是 屏幕对角线的长度
​	<img src="./images/像素的问题/2.png " style="zoom: 50%; margin-left: 0px;" >	

#### 完美视口	

在写移动端网页的时候，需要将网页视口设置为完美视口

``` html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
将这个写上就好了
```

​	<img src="./images/像素的问题/3.png " style="zoom: 50%; margin-left: 0px;" >

​	完美视口 指的是根据官方的像素比自动设置 视口大小 从而达到更好的显示效果

#### vw适配	

**移动端开发的时，不能再使用px来进行布局了**
	vw 视口的宽度单位
	1vw=1%视口宽度
	<img src="./images/像素的问题/4.png " style="zoom: 50%; margin-left: 0px;" >

​	网页中字体大小最小为12px，如果设置小于12px，那么浏览器会自动将字体设置为12px
​	<img src="./images/像素的问题/5.png " style="zoom: 50%; margin-left: 0px;" >

​	

### 响应式布局（css3新特性）

<img src="./images/响应式布局/1.png " style="zoom: 50%; margin-left: 0px;" >

#### 媒介查询规则

<img src="./images/响应式布局/2.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/响应式布局/4.png " style="zoom: 50%; margin-left: 0px;" >

<img src="./images/响应式布局/3.png " style="zoom: 50%; margin-left: 0px;" >
一般 all，print，speech都不用的，用的screen比较多

only加不加都可以 只是为了解决兼容性问题
<img src="./images/响应式布局/5.png " style="zoom: 50%; margin-left: 0px;" >

#### 断点

样式切换的分界点，我们称其为段点，也就是网页的样式会在这个点时发生变化，一般比较常用的段点
<img src="./images/响应式布局/6.png " style="zoom: 50%; margin-left: 0px;" >

#### 最长用的写法

<img src="./images/响应式布局/7.png " style="zoom: 50%; margin-left: 0px;" >
整体的意思就是 500<= ___<=700
and表示 “与” 的意思

<img src="./images/响应式布局/8.png " style="zoom: 50%; margin-left: 0px;" >
,  表示 “或” 的意思
整体的意思就是 <=500  或  700<=

#### 在less可以这样写

``` html
@media only screen{
    @media (min-width: 768px){
       
        }
}
```



