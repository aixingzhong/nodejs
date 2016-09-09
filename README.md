关闭当前窗口页面（适用于用open打开的窗口）
    window.opener = null;
    window.open("", "_self");
    window.close();

word-wrap:break-word;word-break:break-all;  文字处理

a{text-decoration:none}

img{border:0;vertical-align:middle}

table{border-collapse:collapse;border-spacing:0}

onresize 事件会在窗口或框架被调整大小时发生：
<body onresize="alert('You have changed the size of the window')"></body>

返回前一页：history.go(-1);  document.referrer

typeof arr 和 arr instanceof Array 分别输出object和true。

选择绑定事件时采用事件捕获还是事件冒泡，方法就是绑定事件时通过addEventListener函数，它有三个参数，第三个参数若是true，则表示采用事件捕获，若是false，则表示采用事件冒泡。
ele.addEventListener('click',doSomething2,true)
true=捕获
false=冒泡

alert($(window).height()); //浏览器时下窗口可视区域高度
alert($(document).height()); //浏览器时下窗口文档的高度
alert($(document.body).height());//浏览器时下窗口文档body的高度
alert($(document.body).outerHeight(true));//浏览器时下窗口文档body的总高度 包括border padding margin

alert($(window).width()); //浏览器时下窗口可视区域宽度
alert($(document).width());//浏览器时下窗口文档对于象宽度
alert($(document.body).width());//浏览器时下窗口文档body的高度
alert($(document.body).outerWidth(true));//浏览器时下窗口文档body的总宽度 包括border padding margin

alert($(document).scrollTop()); //获取滚动条到顶部的垂直高度
alert($(document).scrollLeft()); //获取滚动条到左边的垂直宽度

.validError {
	color: #F00;
	margin-left: 20px;
	display: block;
	height: 20px;
	width: 50%;
	line-height: 20px;
	display: none;
}
 html{
	height:100%;
	/*  overflow:hidden; */
	/*  border:2px solid red; */
} 
 body{
	height:100%; 
	border:1px solid transparent;
	/* border:2px solid blue; */
}  

Weinre运行
1.命令行键入
weinre -httpPort 8081 -boundHost -all-


Weinre文件加载地址：C:\Users\dell\AppData\Roaming\npm\node_modules\weinre\web


要获取顶端 只需要获取到scrollTop()==0的时候 

要获取底端 只要获取scrollTop()>=$(document).height()-$(window).height() 

window.location.assign();  	加载新的文档（能返回）
window.location.reload();	重新加载当前文档(不能返回，传参无效）
window.location.replace()	用新的文档替换当前文档（不能返回）

<base href="http://pic.chinadaily.com.cn/" target="_blank"/>   页面所有的链接都基于url，都新的页面

工厂模式：在函数内创建一个对象，给对象赋予属性及方法再将对象return，把执行函数赋值给定义的变量，相当于把函数的对象赋值给变量。
解决了创建多个相似对象的问题，确无从识别对象的类型，因为全部都是Object（有缺点）


构造函数模式：相对于工厂模式而言，没有显示的创建对象,直接将属性和方法赋值给了this对象，每次创建实例的时候都要重新创建一次方法（有缺点）

原型方式：定义一个空函数，在函数外给函数定义prototype属性，在新建的函数赋值给定义的变量，但构造函数没入参，对象共用会污染（有缺点）

混合的构造函数/原型方式：在函数内直接将属性赋值给了this对象，将方法赋值给函数的prototype，在新建的函数赋值的定义的变量（流行使用）


可以使用prototype修改和创建对象的方法

charAt(index);返回在指定位置的字符

indexOf(str,index);指定字符串中首次出现的位置

document.write(str.link("http://www.jb51.net"))	   link() 方法用于把字符串显示为超链接。

call()和apply(),将第一个参数替换方法中的this，然后后面的参数传入该方法使用

js默认只执行最后一个事件，jQuery的点击事件click()默认添加on,可以触发多个click事件，添加off()或unbind()可以解除绑定，只执行最后一个click事件

事件监听器是被添加到它们的父元素上。事件监听器会分析从子元素冒泡上来的事件，找到是哪个子元素的事件。e.target是被点击的元素

filter() 方法允许您规定一个标准。不匹配这个标准的元素会被从集合中删除，匹配的元素会被返回。

解析JavaScript面向对象概念中的Object类型与作用域	日期:2016-05-10

canvas:
stroke()
通过线条来绘制图形轮廓。需用closePath()闭合
fill()
通过填充路径的内容区域生成实心的图形。


响应式网页
  (1)声明viewport元标签:<meta name="viewport" content="width=device-width, initial-scale=1">
  (2)使用相对单位，代替px
  (3)流式布局
  (4)响应式图片   img { max-width: x%; }
  (5)CSS3 Media Query


在jsp页面上通过${属性名}这样的语法来访问传送到页面上的对象的属性值。

URL中的参数主要是根据后台需要,如果后台需要一个参数作为查询的辅助条件 前端在URL数据请求时就传递参数。参数前面？,几个参数中间&


移动端远程调试问题



{"errormessage":"图形验证码不匹配","strategy":"2","errorcode":"8004"}

struts.xml配置文件路径

node.js中express模块安装的路径：c:\Users\dell\AppData\Roaming\npm\node_modules


Node.js 应用是由三部分组成的：

1.引入 required 模块：我们可以使用 require 指令来载入 Node.js 模块。

2.创建服务器：服务器可以监听客户端的请求，类似于 Apache 、Nginx 等 HTTP 服务器。

3.接收请求与响应请求 服务器很容易创建，客户端可以使用浏览器或终端发送 HTTP 请求，服务器接收请求后返回响应数据。



NPM是随同NodeJS一起安装的包管理工具，能解决NodeJS代码部署上的很多问题，常见的使用场景有以下几种：

允许用户从NPM服务器下载别人编写的第三方包到本地使用。

允许用户从NPM服务器下载并安装别人编写的命令行程序到本地使用。

允许用户将自己编写的包或命令行程序上传到NPM服务器供别人使用。

清除被占用的端口eclipse:d:\workspace\mogosec_jiangsu\SecurityPlatform_jiangsu>mvn eclipse clean

left:698px  35%
center:486  25%
right:726px  40%;

50% =948

http://172.23.12.231/aqb/mogosec/portal/branches/mogosec_jiangsu/SecurityPlatform/


http://localhost:8080/securityplatform/main.do

goActionDo('encryptAppIndex.do','encryptDetailIntroduction.do',false);return false;

encryptDetailIntroduction.do
5518.19



goActionDo('reinforceSdkDetail.do','reinforceSdkDetailIntroduction.do',true);return false;

cd /home 进入 '/ home' 目录' 
cd .. 返回上一级目录 
cd ../.. 返回上两级目录 
cd 进入个人的主目录 
cd ~user1 进入个人的主目录 
cd - 返回上次所在的目录 
pwd 显示工作路径 
ls 查看目录中的文件 
ls -F 查看目录中的文件 
ls -l 显示文件和目录的详细资料 
ls -a 显示隐藏文件 

<form  onkeypress="if(event.keyCode==13||event.which==13){return false;}">  禁用回车键提交表单

button、checkbox、radio、reset、submit等 这些控件都可以使用，不过需要注意在Android和ios的手机上，控件的样式会所有不同，
如果想完全掌控样式，需要reset一下-webkit-appearance:none，之后在设置自己需要的样式。


Allocate exception for servlet omss4:更新servlet
Servlet.service() for servlet omss4 threw exception：改为window是加密

数据库omss_sec_apppackinfo  列表下改支付方式
omss4_sec_orderrelation    删除数据

<meta name="viewport" content="width=device-width,initial-scale=1.0,
 minimum-scale=1.0, maximum-scale=1.0, user-scalable=no"/>

sessionStorage.setItem("num",oVal.num);    	将value存储到key字段

sessionStorage.getItem("num")			获取指定key本地存储的值

ajax拿到success 的状态码时立刻做跳转，用 window.location.href，浏览器会记录这个登录历史,应该使用 window.location.replace


$("#t_file").uploadify("settings", "formData", { 'appName':$("#appName").val(),'version':$("#AppVersion").val() });

$("#t_file").uploadify('upload','SWFUpload_0_'+fileIndex);

fileObjName：Input Type String，后台表单接受的名称，默认Filedata；

<input type="text" unselectable="on" readonly="readonly">	input框禁止编辑,兼容IE

requestAnimationFrame和setTimeout的区别就在于requestAnimationFrame比setTimeout更快执行，因此很多人用requestAnimationFrame来制作动画。

时间秒转时钟指度数：       
hours: transform, rotate(' + s / 120 + 'deg)');
minute: transform, rotate(' + s * 0.1 + 'deg)');
second: transform", 'rotate(' + s * 6 + 'deg)');
