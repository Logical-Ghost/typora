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

#### 伪元素

<img src="./images/css选择器/40.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/41.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/42.png " style="zoom: 67%; margin-left: 0px;" >
::before和::after在网页中挺常见 content记得带引号

#### 样式的继承，优先级冲突

<img src="./images/css选择器/43.png " style="zoom: 67%; margin-left: 0px;" >

<img src="./images/css选择器/44.png " style="zoom: 67%; margin-left: 0px;" >

### 长度，颜色单位

#### 长度单位

**当元素设置了绝对定位以后，脱离的文档流他的width:50% 是根据它的包含块来设定的（height也是一样的）**

<img src="./images/长度，颜色单位/1.png " style="zoom: 67%; margin-left: 0px;" >

效果
<img src="./images/长度，颜色单位/2.png " style="zoom: 33%; margin-left: 0px;" >

**两个长度单位**
<img src="./images/长度，颜色单位/3.png " style="zoom: 67%; margin-left: 0px;" >

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

### 属性，以及去除默认样式

