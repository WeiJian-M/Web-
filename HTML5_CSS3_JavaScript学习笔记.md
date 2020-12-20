# web概念概述

* JavaWeb：使用Java语言开发基于互联网的项目

* 软件架构:
	1. C/S：Client/Server 客户端/服务端。在用户本地有一个客户端程序，在远程有一个服务器端程序
		* 优点：用户体验好
		* 缺点：开发、安装、部署、维护比较困难
	2. B/C：Browser/Server 浏览器/服务器端。只需要一个浏览器，用户通过不同的网址（URL），客户访问不同的服务器端程序
		* 优点：开发、安装、部署、维护相对简单
		* 缺点：如果应用过大，用户体验可能会受到影响；对硬件要求过高
* B/S架构详解：
	* 资源分类：
		1. 静态资源
			* 使用静态网页开发技术发布的资源
			* 特点：
				1. 所有用户访问，得到的结果是一样的。如：文本、图片、音频、视频、HTML，CSS，JavaScript
				2. 如果用户请求的是静态资源，那么服务器会直接将静态资源发送给浏览 器。浏览器中内置了静态资源的解析引擎，可以展示静态资源
		2. 动态资源
			* 使用动态网页及时发布的资源
			* 特点:
				1. 所有用户访问,得到的结果不一样.如jsp/servlet，php，asp...
				2. 如果用户请求的是动态资源，那么服务器会执行动态资源，转换为静态资源，在发送给浏览器
* 静态资源：
	* HTML：用于搭建基础页面，展示页面的内容
	* CSS：用于美化页面，布局页面
	* JavaScript：控制页面的元素，让页面有一些动态的效果

# HTML

1. 概念：Hyper Text Markup Language 超文本标记语言，是最基础的网页开发语言

	* 超文本：超文本是用超链接的方法，将各种不同空间的文字信息组织在-起的网状文本.
	* 标记语言：由标签构成的语言。<标签名称>，如HTML，XML。标记语言不是编程语言

2. 快速入门

	* 语法：

		1. html文档后缀名：.html  .htm
		2. 标签分为：
			1. 围堵标签：有开始标签和结束标签。如：`<html> </html>`
			2. 自闭合标签：开始标签和结束标签在一起。如：`<br/>`
		3. 标签可以嵌套：需要正确嵌套，不能你中有我，我中有你
		4. 在开始标签中可以定义属性。属性是由键值对构成，值需要用引号（单双都可以）引起来
		5. HTML的标签不区分大小写，但是建议使用小写

	* 代码示例

		```html
		<html>
		<head>
			<title>title</title>
		</head>
		<body>
			<font color="red">HelloWorld!!!</font>
		</body>
		</html>
		```



## 标签

### 文件标签和文本标签

#### 文件标签

构成HTML最基本的标签

* html：html文档的根标签
* head：头标签。用于指定html文档的一些属性，引入外部资源。
* title：标题标签
* body：体标签
* `<!DOCTYPE html>` ：html5中定义该文档是html文档

#### 文本标签

和文本有关的标签

* 注释：`<!-- 注释内容 -->`
* `<h1> to <h6>`：标题标签
	* `<h1> to <h6>`：字体大小逐渐递减
* `<p>`: 段落标签
* `<br>`：换行标签
* `<hr>`：展示一条水平线
	* 属性：
		* color：颜色
		* width：宽度
		* size：高度
		* align：对齐方式
			* center：居中
			* left：左对齐
			* right：右对齐
* `<b>`：字体加粗
* `<i>`：字体斜体
* `<font>`：字体标签
* `<center>`：文本居中
	* 属性：
		* color：颜色
		* size：大小
		* face：字体
	* 属性的相关定义：
		* color：
			* 英文单词：red、green、blue
			* rgb(值1，值2，值3)：值的范围：0~255，如rgb(0, 0, 255)
			* #值1值2值3：值得范围：00~FF之间。如：#FF00FF
		* width：
			* 数值：width = '20'，数值得单位，默认是px（像素）
			* 数值%：占比相对于父元素得比例

#### 练习

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Title</title>
</head>
<body>
<h1>hahaha</h1>
<hr color="yellow">
lalalala

<hr color="yellow">
<font size="2", color="gray">
    <center>
        
    </center>
</font>

</body>
</html>
```

### 图片标签、列表标签、链接标签

#### 图片标签

* img：展示图片

	* 属性：

		* src：指定图片的位置

	* 路径：

		* 相对路径：以.开头的路径

			./：代表当前目录；../：代表上一级目录

* 代码示例：

	```html
	<img src="image/jingxuan 2.jpg" align="right" alt="古镇" width= "500" height="500"/>
	<!-- alt指图片没有加载出来时所显示的文字 -->
	```

	

#### 列表标签

* 有序列表
	* ol
	* li
* 无序列表
	* ul
	* li

#### 链接标签

* 定义一个超链接
	* 属性：
		* href：指定访问资源的url(url是统一资源定位符)
		* target
			* _self：默认值，在当前页面打开
			* _blank：在空白页面打开

### div和span、语义化标签、表格标签

#### div和span

* div：每一个div占满一整行，会计标签
* span：文本信息在一行显示，行内标签 内联标签

#### 语义化标签

html5中为了提高程序的可读性，提供了一些标签

* `<header>`：叶眉
* `<footer>`：页脚

#### 表格标签

* table：定义表格
	* width：宽度
	* border：边框
	* cellpadding：定义内容和单元格的距离
	* cellspacing：定义单元格之间的距离，如果指定为0，则单元格的线会合为一条
	* bgcolor：背景色
	* align：对齐方式
* tr：定义行
	* bgcolor：背景色
	* align：对齐方式
* td：定义单元格
	* colspan：合并列
	* rowspan：行并行
* th：定义表头单元格
* `<caption>`：表格标题
* `<thead>`：表示表格的头部分
* `<tbody>`：表示表格的体部分
* `<tfoot>`：表示表格的脚部分



### 综合案例

旅游网站首页

分析：

1. 在没有使用CSS的情况下，确定使用table来完成布局

2. 如果某一行只有一个单元格，则使用`<tr><td></td></tr>`

3. 如果某一行有多个单元格，则使用如下：

	```
	<tr>
		<td>
			<table></table>
		</td>
	</tr>
	```

代码略

### 表单标签

表单：用于采集用户输入的数据，用于和服务器进行交互

使用的标签：form（用于定义表单的，可以定义一个范围，范围代表采集用户数据的范围）

属性：

* action：用于提交数据的URL
* method：指定提交方式
	* 分类：一共七种，两种比较常用
		* get：
			* 请求参数会在地址栏中显示
			* 请求参数的长度是有限制的
			* 不太安全
		* post：
			* 请求参数不会在地址栏中显示，会封装在请求体中
			* 请求参数的大小没有限制
			* 较为安全
	* 表单项中的数据要想被提交：必须定义其name属性

表单项标签：

* input：可通过type属性值，改变元素展示的样式

	type属性

	* text：文本输入框，默认值

		* placeholder：指定输入框的提示信息，当输入框的内容发生变化，会自动清空提示信息

	* password：密码输入框

	* radio：单选框

		注意：

		1. 要想让多个单选框实现单选的效果，则多个单选框的name属性值必须一样
		2. 一般会给每一个单选框提供value属性，指定其被选后提交的值
		3. checked属性，可以指定默认值

	* checkedbox：复选框：

		注意

		1. 一般会给每一个单选框提供value属性，指定其被选中后提交的值
		2. checked属性，可以指定默认值

	* file：文件选择框

	* hidden：隐藏域，用于提交一些信息

	* 按钮：

		* submit：提交按钮。可以提交表单
		* button：普通按钮
		* image：图片形式的提交按钮
			* src属性指定图片的路径

	label：指定输入项的文字描述信息

	注意：

	1. label的for属性一般回合input的id属性值对应，如果对应了，点击label区域，会让input输入框获取焦点

* select：下拉列表

	* 子元素：option，指定列表项

* textarea：文本域

	* cols：指定列数，每一行有多少个字符
	* rows：默认多少行



# CSS

页面的美化工作和布局

概念：Cascading Style Sheet 层叠样式表

* 层叠：多个样式可以作用在同一个html的元素上，同时生效

好处：

1. 功能强大
2. 将内容展示和样式控制分离
	* 降低耦合度。解耦
	* 让分工协作更容易
	* 提高开发效率

CSS的使用：CSS与html的结合方式

1. 内联样式

	* 在标签内使用style属性指定css代码

		如：`<div style = "color:red;">hello css</div>`

2. 内部样式

	* 在head标签内，定义style标签，style标签的标签体内容就是css代码

		如：

		```html
		<style>
			div{
				color:blue;
			}
		</style>
		<div>hello css</div>
		
		```

3. 外部样式：

	1. 定义css资源文件
	2. 在head标签内，定义link标签，引入外部的资源文件

	如：

	```html
	div{
		color:green;
	}
	<link rel="stylesheet" href="css/a.css">
	<div>hello css</div>
	<div>hello css</div>
	```

* 注意：

	* 1、2、3种方式，css作用的范围越来越大

	* 1方式不常用，后期常用2，3

	* 第3种格式可以在head标签内这样写：

		```html
		<style>
			@import "css/a.css";
		</style>
		
		```

## CSS语法

格式：

```
选择器{
	属性名1:属性值1;
	属性名2:属性值2;
	...
}
```

* 选择器：筛选具有相似特征的元素
* 注意：每一对属性需要使用；隔开，最后一对属性可不加；

### 选择器

筛选具有相似特征的元素

分类：

1. 基本选择器

	1. id选择器：选择具体的id属性值的元素，建议在一个html页面中id值唯一
		* 语法：#id属性值{}
	2. 元素选择器：选择具有相同标签名称的元素
		* 语法：标签名称{}
		* 注意：id选择器优先级高于元素选择器
	3. 类选择器
		* 语法：.class属性值{}
		* 注意：类选择器优先级高于元素选择器

	* 基础选择器优先级比较：

		id选择器 > 类选择器 > 元素选择器

2. 扩展选择器：

	1. 选择所有元素：
		* 语法：*{}
	2. 并集选择器：
		* 选择器1，选择器2{}
	3. 子选择器：筛选选择器1下的选择器2元素
		* 语法：选择器1  选择器2{}
	4. 父选择器：筛选选择器2的父选择器1
		* 语法：选择器1 > 选择器2{}
	5. 属性选择器：选择元素名称，属性名=属性值元素
		* 语法：元素名称[属性名=“属性值”]{}
	6. 伪类选择器：选择一些元素具有的状态
		* 语法：元素：状态{}
		* 如：`<a>`
			* 状态：
				* link：初始化的状态
				* visited：被访问过的状态
				* active：正在访问的状态
				* hover：鼠标悬浮状态

### 属性

1. 字体、文本
	* font-size：字体大小
	* color：文本颜色
	* text-align：对齐方式
	* line-height：行高
2. 背景
	* background：
3. 边框
	* border：设置边框
4. 尺寸
	* width：宽度
	* height：高度
5. 盒子模型：控制布局
	* margin：外边距
	* padding：内边距
		* 默认情况下内边距会影响整个盒子的大小
		* box-sizing：border-box；设置盒子的属性，让width和height就是最终盒子的大小
	* float：浮动
		* left
		* right

## 综合案例

最终效果图：

![](E:\Java学习资料\JavaWeb\day08_HTML&CSS\day08_HTML&CSS\资料\案例\案例2_注册页面(css)\案例效果.png)



代码实现：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>综合案例</title>
    <style>
        .bc{
            background: url("image/register_bg.png") no-repeat center;
        }

        .bc_reg{
            background-color: white;
            border: gray 5px solid;
            width: 900px;
            height: 600px;
            margin: 50px auto auto;
        }
        .bc_left{
            float: left;
            font-size: 22px;
            margin: 20px;
        }
        .bc_center{
            float: left;
            height: 600px;
            width: 450px;
        }

        .bc_rigth{
            float: right;
            margin: 15px;
            padding-left: 50px;
        }

        .form_left{
            height: 50px;
            color: grey;
            text-align: right;
            padding-right: 5px;
            font-size: 14px;
        }
        .form_right{
            height: 50px;
        }

        #username, #password, #email, #your_name, #tel_phone, #date_t, #yan_zheng{
            border-radius: 5px;
            border: 1px darkgrey solid;
            width: 230px;
            height: 32px;
        }

        #yan_zheng{
            width: 115px;
        }

        #img_check{
            vertical-align: middle;
        }

        #submit{
            width: 115px;
            height: 32px;
            background-color: yellow;
            border: yellow 1px;
            border-radius: 5px;
        }

    </style>
</head>
<body class="bc">
<div class="bc_reg">
    <div class="bc_left">
        <p><font color="yellow">新用户注册</font></p>
        <p><font color="#a9a9a9">USER REGISTER</font></p>
    </div>

    <div class="bc_center" align="center">
        <form>
            <table>
                <tr>
                    <td class="form_left">用户名</td>
                    <td class="form_right"><input type = text name="username" id="username" placeholder="请输入用户名"></td>
                </tr>
                <tr>
                    <td class="form_left">密码</td>
                    <td class="form_right"><input type="password" name="password" id="password" placeholder="请输入密码" ></td>
                </tr>
                <tr>
                    <td class="form_left">Emile</td>
                    <td class="form_right"><input type="email" name="email" id="email" placeholder="请输入邮箱"></td>
                </tr>
                <tr>
                    <td class="form_left">姓名</td>
                    <td class="form_right" ><input type="text" name="your_name" id="your_name" placeholder="请输入真实姓名"></td>
                </tr>
                <tr>
                    <td class="form_left"> 手机号</td>
                    <td class="form_right"><input type="tel" name="tel_phone" id="tel_phone" placeholder="请输入您的手机号"></td>
                </tr>
                <tr>
                    <td class="form_left">性别</td>
                    <td class="form_right">
                        <input type="radio" name="sex" value="male">男
                        <input type="radio" name="sex" value="female">女
                    </td>
                </tr>
                <tr>
                    <td class="form_left">出生日期</td>
                    <td class="form_right"><input type="date" name="date_t" id="date_t" placeholder="请输入您的出生日期"></td>
                </tr>
                <tr>
                    <td class="form_left">验证码</td>
                    <td class="form_right"><input type="text" name="yan_zheng" id="yan_zheng" placeholder="请输入右侧验证码"> <img id="img_check" src="image/verify_code.jpg" alt="验证码"></td>
                </tr>
                <tr>
                    <td colspan="2" align="center" class="submit"><input type="submit" id="submit" value="注册"></td>
                </tr>
            </table>
        </form>
    </div>

    <div class="bc_rigth">
        已有帐号？
        <a href="">立即注册</a>
    </div>
</div>

</body>
</html>
```

# JavaScript

## JavaScript基础

概念：JavaScript是一门客户端脚本语言

* 运行在客户端浏览器中的。每一个浏览器都有JavaScript的解析引擎
* 脚本语言：不需要编译，直接就可以被浏览器解析执行了

功能：可以来增强用户和html页面的交互过程，可以来控制html元素，让页面有一些动态的效果，增强用户的体验

JavaScript发展史：

1. 1992年，Nombase公司， 开发出第1门客户端脚本语言，专门用于表单的校验。命名为：C--，后来更名为: ScriptEase
2. 1995年，Netscape(网景)公司，开发了一门客户端脚本语言：LiveScript。后来，请来SUN公司的专家，修改LiveScript，命名为JavaScript
3. 1996年，微软抄袭JavaScript开发出JScript语言
4. 1997年，ECMA(欧洲计算机制造商协会)，ECMAScript，就是所有客户端脚本语言的标准。

JavaScript = ECMAScript + JavaScript自己特有的东西(BOM+DOM）

### ECMAScript ：客户端脚本语言的标准

#### 1. 基本语法

1. 与html结合方式

	1. 内部JS：定义`<script>`，标签体容就是JS代码
	2. 外部JS：定义`<script>`，通过src属性引入外部的JS文件

	* 注意：
		* `<script>`可以定义在html页面的任何地方。但是定义位置会影响执行顺序
		* `<script>`可以定义多个

2. 注释

	1. 单行注释：//注释内容
	2. 多行注释：/* 注释内容 */

3. 数据类型

	1. 原始数据      类型（基本数据类型）
		1. number：数字。整数/小数/NaN(not a number 一个不是数字的数字类型)
		2. string：字符串。字符串 "abc" "a" 'abc'
		3. boolean：true和false
		4. null：一个对象为空的占位符
		5. undefined：未定义。如果一个变量没有初始化值，则会被默认赋值为undefined
	2. 引用数据类型：对象

4. 变量

	* 变量：一小块存储数据的内存空间
	* JavaScript语言是弱类型的语言，而Java是强类型的语言
		* 强类型：在开辟变量存储空间是，定义了空间将来存放的数据的类型。只能存储固定类型的数据
		* 弱类型：在开辟变量存储空间 时，不定义空间将来的存储数据类型，可以存放任意类型的数据
	* 语法：
		* `var 变量名 = 初始化值;`
	* typeof运算符：获取变量的类型
		* 注：null运算后的到的是object

5. 运算符

	1. 一元运算符：只有一个运算数的运算符

		++，--， +（正号），-（负号）

		* 注意：在JS中，如果运算数不是运算符所要求的类型，那么JS引擎会自动将运算数进行数据类型转换

			* 其他类型转number：

				string转number：按照字面值转。如果字面值不是数字，则转为NaN（不是数字的数字）

				boolean转number：true转为1，false转为0

	2. 赋值运算符

		`=, +=, -=`

	3. 算数运算符：

		`+, -, *, /, %`

	4. 比较运算符

		`>, <, >=, <=, ==, ===(全等于)`、

		* 比较方式：
			1. 类型相同：直接比较
				* 字符串：按照字典顺序比较。按位逐一比较，直到得出大小为止
			2. 类型不同：先进行类型转换，再比较
				* `===`：全等于。在比较之前，先判断类型，如果类型不一样，则直接返回false

	5. 逻辑运算符

		`&&, ||, !`

		`!`:非

		* 其他类型转boolean：
			1. number：0或NaN为假，其他为真
			2. string：除了空字符串("")，其他都是true
			3. null&undefined：都是false
			4. 对象：所有对象都是true

	6. 三元运算符

		`? :`

	7. JS特殊语法

		1. 语句以;结尾，如果一行只有一条语句则;可以省略（不建议）
		2. 变量的定义使用var关键字，也可以不使用
			* 用：定义的变量是局部变量
			* 不用：定义的变量是全局变量（不建议）

6. 流程控制语句

	1. `if...else...`
	2. `switch`
		* 在Java中，switch语句可以接受的数据类型：`byte int short char 枚举 String`
		* 在JS中，switch语句可以接受任意的原始数据类型
	3. `while`
	4. `do...while`
	5. `for`

7. 练习：99乘法表

	最终效果：

	![](E:\Java学习资料\Java进阶笔记\图片\007.png)

	代码实现：

	```html
	<!DOCTYPE html>
	<html lang="en">
	<head>
	    <meta charset="UTF-8">
	    <title>99乘法表</title>
	    <style>
	        td{
	            border: 1px solid;
	        }
	    </style>
	
	    <script>
	        document.write("<table>");
	        for (var i = 1; i <= 9; i++) {
	            document.write("<tr>");
	            for(var j = 1; j <= i; j++){
	                document.write("<td>");
	                document.write(i + " * " + j + " = " +  i * j);
	                document.write("</td>");
	            }
	            document.write("</tr>");
	        }
	        document.write("</table>");
	    </script>
	</head>
	<body>
	
	</body>
	</html>
	```

	

#### 2. 基本对象

##### `Function`：函数（方法）对象

1. 创建：

	1. `var fun = new Function(形式参数列表, 方法体)`

	2. ```javascript
		function 方法名称(形式参数列表){
			//方法体
		}
		```

	3. ```javascript
		var 方法名 = function(形参列表){
			 //方法体
		}
		```

		

2. 方法

3. 属性

	length：代表形参个数

4. 特点

	1. 方法定义时，形参的类不用写，返回值类型也不写。
	2. 方法是一个对象，如果定义名称相同的方法，会覆盖
	3. 在JS中，方法的调用只与方法的名称有关，和参数列表无关
	4. 在方法声明中有一个隐藏的内置对象（数组），`arguments`，封装所有的实际参数。

5. 调用：

	`方法名称(实际参数列表);`

##### `Array`数组对象

1. 创建
	1. `var arr = new Array(元素列表);`
	2. `var arr = new Array(默认长度);`
	3. `var arr = [元素列表];`
2. 方法
	1. `join(参数)`：将数组中的元素按照指定的分隔符拼接为字符串
	2. `push()`：向数组中的末尾添加一个或更多元素，并返回新的长度  
3. 属性
	1. length：数组的长度
4. 特点：
	1. JS中，数组元素的类型是可变的。
	2. JS中，数组的长度是可变的

##### `Boolean`对象

##### `Date` 日期对象

1. 创建

	`var date = new Date();`

2. 方法

	1. `toLocaleString()`：返回当前date对象对应的时间本地字符串格式
	2. `getTime()`：获取毫秒值。返回当前日期对象描述的时间到1970年1月1日零点的毫秒值差



##### `Math` 数学对象

1. 创建：

	特点：Math对象不用创建，直接使用。`Math.方法名()`

2. 方法：

	1. `random()`：返回0~1之间的随机数。含0不含1
	2. `ceil(x)`：对数进行上舍入（向上取整）
	3. `floor(x)`：对数进行下舍入（向下取整）
	4. `ruond(x)`：把数四舍五入为最接近的整数

3. 属性：

	1. PI（圆周率）

##### `Number`对象

##### `String`对象

##### `RegExp` 正则表达式对象

1. 正则表达式：定义字符串的组成规则
	1. 单个字符
		* \d：单个数字字符[0-9]
		* \w：单个单词字符
	2. 量词符号：
		* `?`：表示出现0次或一次
		* `*`：表示出现0次或多次
		* `+`：表示出现1次或多次
		* `{m, n}`：表示`m<= 数量 <=n`
			* m如果缺省：`{ , n}`：最多n次
			* n如果缺省：`{m, }`：最少m次
	3. 开始结束符号
		1. `^`：开始符号
		2. `$`：结束符号
2. 正则对象
	1. 创建
		1. `var reg = new RegExp("正则表达式");` （有时候需要转义）
		2. `var reg = /正则表达式/;`
	2. 方法
		1. `test(参数)`：验证指定的字符串是否正则定义的规范

##### `Global`对象

1. 特点：全局对象，这个Global中封装的方法不需要对此昂就可以直接调用。`方法名();`
2. 方法
	1. `encodeURI`：url编码
	2. `decodeURI`：url解码
	3. `encodeURIComponent`：url编码，编码的字符更多
	4. `decodeURIComponent`：url解码
	5. `parseInt()`：将字符串转为数字
		* 逐一判断每一个字符是否是数字，直到不是数字为止，将前边数字部分转为number
	6. `isNaN(参数)`：判断一个值是否是NaN
		* NaN参与的==比较全部为false
	7. `eval()`：将JavaScript字符串解析，并把它作为脚本代码来执行
3. URL编码：将字符转换为指定格式的编码（略）

## JavaScript高级

### DOM的简单学习

功能：控制html文档的内容

获取页面标签（元素）对象：Element

* `document.getElementById("id值")`：通过元素的id获取元素对象

操作Element对象：

1. 修改属性值：

	1. 明确获取的对象是哪一个？
	2. 查看API文档，找其中有哪些属性可以设置。

2. 修改标签体内容：

	* 属性：`innerHTML`

	1. 获取元素对象
	2. 使用`innerHTML`属性修改标签体内容

### 事件的简单学习

功能：某些组件被执行了某些操作后，触发某些代码的执行。

如何绑定事件

1. 直接在html标签上，指定事件的属性（操作），属性值就是js代码
	1. 事件：`onclick` --- 单击事件
2. 通过js获取元素对象，指定事件属性，设置一个函数

代码示例：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>点击事件</title>
</head>
<body>
<img id="click" src="../image/register_bg.png">

<script>
    var elementById = document.getElementById("click");

    function fun() {
        alert("我被点击了");
    }

    elementById.onclick = fun;
</script>

</body>
</html>
```

### 案例：电灯开关案例

代码实现：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>电灯开关案例</title>
</head>
<body>

<img id="light" src="image/off.gif">

<script>
    var flag = false;

    var elementById = document.getElementById("light");

    elementById.onclick = function () {
        if(flag){
            elementById.src = "image/off.gif";
            flag = false;
        }else{
            elementById.src = "image/on.gif";
            flag = true;
        }
    }
</script>
</body>
</html>
```

### BOM

1. 概念：Browser Object Model 浏览器对象模型
	* 将浏览器的各个组成部分封装成对象

#### `Window`：窗口对象

##### 创建

##### 方法

1. 与弹出框有关的方法
	* `alert()`：显示带有一段消息和一个确认按钮的警告框。
	* `confirm()`：显示带有一段消息以及确认按钮和取消按钮的对话框
		* 如果用户点击确定按钮，则方法返回true
		* 如果用户点击取消按钮，则方法返回false
	* `prompt()`：显示可提示用户输入的对话框
		* 返回值：获取用户输入的值
2. 与打开关闭有关的方法
	1. `close()`：关闭浏览器窗口
		* 哪个window对象调用，就关哪个对象所对应的窗口
	2. `open()`：打开一个新的浏览器窗口。参数可以传递网址，返回值是新的window对象
3. 与定时器有关的方法
	1. `setTimeout()`：在指定的毫秒数后调用函数或计算表达式
		* 参数：
			1. js代码或者方法对象
			2. 毫秒值
		* 返回值：唯一标识，用于取消定时器
	2. `clearTimeout()`：取消由`setTimeout()`方法设置的timeout
		* 参数为`setTimeout()`的返回值
	3. `setInterval`：按照指定分周期（以毫秒计）来调用函数或计算表达式（参数和返回值同`setTimeout()`）
	4. `clearInterval()`：取消由`setInterval()`设置的timeout

##### 属性

1. 获取其他BOM对象
	1. `history`
	2. `location`
	3. `Navigator`
	4. `Screen`
2. 获取DOM对象
	1. `document`

##### 特点

* Window对象不需要创建可以直接使用：`window.方法名();`
* `window`引用可以省略，使用时直接写方法名：`方法名();`

##### 案例

轮播图，每3秒更换一张图片。

代码实现：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>轮播图</title>
</head>
<body>
<img id="image" src="../image/banner_1.jpg" width="100%">

<script>
    var num = 0;
    function fun(){
        var n = num % 3 + 1;
        var image = document.getElementById("image");
        image.src = "../image/banner_" + n + ".jpg";
        num++;
    }
    
    //每3秒更换一张图片
    setInterval(fun, 3000);
</script>
</body>
</html>
```

#### `Location` 地址栏对象

##### 创建（获取）

1. `window.location`
2. `location`

##### 方法

`reload()`：重新加载当前文档

##### 属性

`href`：设置或返回完整的URL

##### 案例

五秒后跳转到首页。

代码实现：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>跳转首页</title>
    <style>
        p{
            text-align: center;
        }

        span{
            color: red;
        }
    </style>
</head>
<body>
<p>
    <span id="num">5</span>秒后跳转到首页...
</p>

<script>
    var number = 5;
    var elementById = document.getElementById("num");
    function fun() {
        if(number <= 0){
            location.href = "https://www.baidu.com"
        }
        elementById.innerText = number--;
    }

    setInterval(fun, 1000);
</script>

</body>
</html>
```

#### `History` 历史记录对象

##### 创建（获取）

1. `window.history`
2. `history`

##### 方法

1. `back()`：加载`history`列表中的前一个URL
2. `forward()`：加载`history`列表中的下一个URL
3. `go(参数)`：加载`history`列表中的某个具体页面
	* 参数：
		* 正数：前进几个历史记录
		* 负数：后退几个历史记录

##### 属性

1. `length`：返回当前窗口历史列表中的URL数量



### DOM

概念：Document Object Model 文档对象模型

* 将标记语言文档的各个组成部分，封装为对象。可以使用这些对象，对标记语言文档进行CURD的动态操作。

W3C DOM 标准被分为3个不同的部分

* 核心 DOM：针对任何结构化文档的标准模型
	* Document：文档对象
	* Element：元素对象
	* Attribute：属性对象
	* Text：文本对象
	* Comment：注释对象
	* Node：节点对象，上面五个对象的父对象
* XML DOM：针对XML文档的标准模型
* HTML DOM：针对HTML文档的标准模型

#### 核心DOM模型

##### Document 文档对象

1. 创建（获取）:在html dom模型中可以使用window对象来获取

	1. `window.document`
	2. `document`

2. 方法：

	1. 获取Element对象

		`getElementById()`：根据id属性值获取元素对象。id属性值一般唯一

		`getElementsByTagName()`：根据元素名称获取元素对象们。返回值是一个数组

		`getElementsByClassName()`：根据Class属性值获取元素对象们。返回值是一个数组

		`getElementByName()`：根据name属性值获取元素对象们。返回值是一个数组

	2. 创建其他DOM对象

		`createAttribute(name)`

		`createComment()`

		`createElement()`

		`createTextNode()`

3. 属性

##### `Element` 元素对象

1. 获取 / 创建：通过document来获取和创建
2. 方法：
	1. `removeAttribute()`：删除属性
	2. `setAttribute()`：设置属性

##### `Node` 节点对象

其他5个对象的父对象。

1. 特点：所有dom对象都可以被认为是一个节点

2. 方法：

	1. CURD dom树：

		`appendChild()`：向节点的子节点列表的结尾添加新的子节点

		`removeChild()`：删除（并返回）当前节点得指定子节点

		`replaceChild()`：用新节点替换一个子节点

3. 属性：

	`parentNode`：返回节点的父节点

##### 案例：动态表格

可对表格进行添加和删除操作。

效果图：

![image-20200513174216384](E:\Java学习资料\Java进阶笔记\图片\008.png)

步骤：

1. 添加
	1. 给添加按钮绑定单机事件
	2. 获取文本框内容
	3. 创建td，设置td的文本为文本框的内容
	4. 创建tr
	5. 将td添加到tr中
	6. 获取table，将tr添加到table中
2. 删除
	1. 确定点击的是哪一个超链接
		* `<a href = "javascript:void(0);" onclick = "delTr(this);">删除</a>`
	2. 怎么删除？
		* `removeChild()`：通过父节点删除子节点

代码实现：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>动态添加表项</title>
    <style>
        table{
            margin: auto;
            border: black 1px solid;
            width: 500px;
        }

        td, th{
            text-align: center;
            border: black 1px solid;
        }

        div{
            text-align: center;
            margin: 50px;
        }
    </style>
</head>
<body>

<div>
    编号：
    <input type="text" id = "id">
    姓名：
    <input type="text" id = "name">
    性别：
    <input type="text" id = "sex">
    <input type="button" id = "add" value="添加">
</div>
<table>
    <caption>名单信息</caption>
    <tr>
        <th>编号</th>
        <th>姓名</th>
        <th>性别</th>
        <th>操作</th>
    </tr>

    <tr>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td><a href="javascript:void(0);" onclick="delTr(this);">删除</a></td>
    </tr>
</table>

<script>
    //给添加按钮绑定单机事件
    document.getElementById("add").onclick = function () {
        var id = document.getElementById("id").value;
        var name = document.getElementById("name").value;
        var sex = document.getElementById("sex").value;

        var id_text = document.createTextNode(id);
        var name_text = document.createTextNode(name);
        var sex_text = document.createTextNode(sex);

        //创建td
        var td_id = document.createElement("td");
        var td_name = document.createElement("td");
        var td_sex = document.createElement("td");
        var del = document.createElement("td");

        td_id.appendChild(id_text);
        td_name.appendChild(name_text);
        td_sex.appendChild(sex_text);

        //创建一个超链接
        var a = document.createElement("a");
        a.setAttribute("href", "javascript:void(0)");
        a.setAttribute("onclick", "delTr(this)");
        var text = document.createTextNode("删除");
        a.appendChild(text);
        //添加到表项中
        del.appendChild(a);
        //创建表格的一行
        var tr = document.createElement("tr");
        tr.appendChild(td_id);
        tr.appendChild(td_name);
        tr.appendChild(td_sex);
        tr.appendChild(del);

        document.getElementsByTagName("table")[0].appendChild(tr);
    }

    function delTr(e) {
        var table = e.parentNode.parentNode.parentNode;
        var tr = e.parentNode.parentNode;

        table.removeChild(tr);
    }
</script>
</body>
</html>
```

### HTML DOM

1. 标签体的设置和获取：`innerHTML`

2. 使用`html`元素对象的属性（用到时查看文档）

3. 控制元素样式

	1. 使用元素的style属性来设置

		如：

		```html
		div1.style.border = "1px solid red";
		div1.style.width = "200px";
		div1.style.fontSize = "20px";
		```

	2. 提前定义好类选择器的样式，通过元素的`className`属性来设置其class属性值

利用`innerHTML`对上一节案例的优化：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>动态添加表项</title>
    <style>
        table{
            margin: auto;
            border: black 1px solid;
            width: 500px;
        }

        td, th{
            text-align: center;
            border: black 1px solid;
        }

        div{
            text-align: center;
            margin: 50px;
        }
    </style>
</head>
<body>

<div>
    编号：
    <input type="text" id = "id">
    姓名：
    <input type="text" id = "name">
    性别：
    <input type="text" id = "sex">
    <input type="button" id = "add" value="添加">
</div>
<table>
    <caption>名单信息</caption>
    <tr>
        <th>编号</th>
        <th>姓名</th>
        <th>性别</th>
        <th>操作</th>
    </tr>

    <tr>
        <td>1</td>
        <td>1</td>
        <td>1</td>
        <td><a href="javascript:void(0);" onclick="delTr(this);">删除</a></td>
    </tr>
</table>

<script>
    //给添加按钮绑定单机事件
    document.getElementById("add").onclick = function () {
        var id = document.getElementById("id").value;
        var name = document.getElementById("name").value;
        var sex = document.getElementById("sex").value;

        //获取table
        var table = document.getElementsByTagName("table")[0];

        table.innerHTML += "<tr>\n" +
            "        <td>"+ id +"</td>\n" +
            "        <td>"+ name +"</td>\n" +
            "        <td>"+ sex +"</td>\n" +
            "        <td><a href=\"javascript:void(0);\" onclick=\"delTr(this);\">删除</a></td>\n" +
            "    </tr>";
    }

    function delTr(e) {
        var table = e.parentNode.parentNode.parentNode;
        var tr = e.parentNode.parentNode;

        table.removeChild(tr);
    }
</script>
</body>
</html>
```

### 事件

概念：某些组件被执行了某些操作后，触发某些代码的执行

* 事件：某些操作。如单机，双击，键盘按下了，鼠标移动了
* 事件源：组件。如：按钮，文本输入框...
* 监听器：代码
* 注册监听：将事件，事件源，监听器结合在一起。当事件源上发生了某个事件，则触发执行某个监听器代码。

常见的事件：

1. 点击事件：
	1. onclick	点击事件。
	2. ondblclick	双击事件。
2. 焦点事件
	1. onblur	元素失去焦点。
	2. onfocus	元素获得焦点。
3. 加载事件
	1. onload：一张页面或一副图像完成加载，onload 事件会在页面或图像加载完成后立即发生。
4. 鼠标事件
	1. onmousedown 鼠标按钮被按下
	2. onmouseup 鼠标按键被松开。
	3. onmousemove 鼠标被移动。
	4. onmouseover 鼠标移到某元素之上。
	5. onmouseout 鼠标从某元素移开。
5. 键盘事件
	1. onkeydown 某个键盘按键被按下。
	2. onkeyup 某个键盘按键被松开。
	3. onkeypress 某个键盘按键被按下并松开。
6. 选择和改变
	1. onchange 域的内容被改变。
	2. onselect 文本被选中。
7. 表单事件
	1. onsubmit 确认按钮被点击。
	2. onreset 重置按钮被点击。

#### 案例：表格全选

代码实现：

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>动态添加表项</title>
    <style>
        table{
            margin: auto;
            border: black 1px solid;
            width: 500px;
        }

        td, th{
            text-align: center;
            border: black 1px solid;
        }

        div{
            text-align: center;
            margin: 50px;
        }

        .setN{
            text-align: center;
        }
    </style>

    <script>
        window.onload = function () {
            //全选
            document.getElementById("selAll").onclick = function () {
                var elementsByName = document.getElementsByName("cb");
                for (var i = 0; i < elementsByName.length; i++) {
                    elementsByName[i].checked = true;
                }
            }
            
            //全不选
            document.getElementById("selNone").onclick = function () {
                var elementsByName = document.getElementsByName("cb");
                for (var i = 0; i < elementsByName.length; i++) {
                    elementsByName[i].checked = false;
                }
            }
            //反选
            document.getElementById("selOther").onclick = function () {
                var elementsByName = document.getElementsByName("cb");
                for (var i = 0; i < elementsByName.length; i++) {
                    elementsByName[i].checked = !elementsByName[i].checked;
                }
            }
            
            //跟随第一行操作
            document.getElementById("cbfirst").onclick = function () {
                var elementsByName = document.getElementsByName("cb");
                for (var i = 0; i < elementsByName.length; i++) {
                    elementsByName[i].checked = this.checked;
                }
            }
        }
    </script>
</head>
<body>

<div>
    编号：
    <input type="text" id = "id">
    姓名：
    <input type="text" id = "name">
    性别：
    <input type="text" id = "sex">
    <input type="button" id = "add" value="添加">
</div>
<table>
    <caption>名单信息</caption>
    <tr>
        <th> <input type="checkbox" name="cb" id="cbfirst"></th>
        <th>编号</th>
        <th>姓名</th>
        <th>性别</th>
        <th>操作</th>
    </tr>
</table>

<script>
    //给添加按钮绑定单机事件
    document.getElementById("add").onclick = function () {
        var id = document.getElementById("id").value;
        var name = document.getElementById("name").value;
        var sex = document.getElementById("sex").value;

        var id_text = document.createTextNode(id);
        var name_text = document.createTextNode(name);
        var sex_text = document.createTextNode(sex);

        //创建td
        var td_cb = document.createElement("td");
        var td_id = document.createElement("td");
        var td_name = document.createElement("td");
        var td_sex = document.createElement("td");
        var del = document.createElement("td");

        var cb = document.createElement("input");
        cb.setAttribute("type", "checkbox");
        cb.setAttribute("name", "cb");

        td_cb.appendChild(cb);
        td_id.appendChild(id_text);
        td_name.appendChild(name_text);
        td_sex.appendChild(sex_text);

        //创建一个超链接
        var a = document.createElement("a");
        a.setAttribute("href", "javascript:void(0)");
        a.setAttribute("onclick", "delTr(this)");
        var text = document.createTextNode("删除");
        a.appendChild(text);
        //添加到表项中
        del.appendChild(a);
        //创建表格的一行
        var tr = document.createElement("tr");
        tr.appendChild(td_cb);
        tr.appendChild(td_id);
        tr.appendChild(td_name);
        tr.appendChild(td_sex);
        tr.appendChild(del);

        document.getElementsByTagName("table")[0].appendChild(tr);
    }

    function delTr(e) {
        var table = e.parentNode.parentNode.parentNode;
        var tr = e.parentNode.parentNode;

        table.removeChild(tr);
    }
</script>
<div class="setN">
    <input type="button" id="selAll" value="全选">
    <input type="button" id="selNone" value="全不选">
    <input type="button" id="selOther" value="反选">
</div>

</body>
</html>
```



