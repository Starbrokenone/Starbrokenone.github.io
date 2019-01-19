---
layout:     post
title:      JavaScript快速入门
subtitle:   html css JavaScript
date:       2019-01-18
author:     Starbroken
header-img: img/post-bg-ios9-web.jpg
catalog: true
tags:
    - web前端
---
# 简介
JavaScript 是世界上最流行的编程语言。

这门语言可用于 HTML 和 web，更可广泛用于服务器、PC、笔记本电脑、平板电脑和智能手机等设备。
# 变量
变量是数据的代号，如同人的名字一样。
```
var num;//在JavaScript中使用关键字var声明一个变量
```
与代数一样，JavaScript 变量可用于存放值（比如 x=2）和表达式（比如 z=x+y）。

1. 变量可以使用短名称（比如 x 和 y），也可以使用描述性更好的名称（比如 age, sum, totalvolume）。

2. 变量必须以字母开头
3. 变量也能以 $ 和 _ 符号开头（不过我们不推荐这么做）
4. 变量名称对大小写敏感（y 和 Y 是不同的变量）
提示：JavaScript 语句和 JavaScript 变量都对大小写敏感
## 变量定义
```
var dog;
    dog="狗";//字符串，它们总被包含在双引号(或单号)中
    var num;
    num=1;//数字，它们裸露的出现了
    var strNum;
    strNum="1";//但是现在strNum所引用的是一个字符串,因为它被包含在引号中了
    var badNum;
    badNum=3.345;//一个小数，因为它带有一个小数点
    badNum=.2;//仍然是一个小数，这句代码与badNum=0.2是一样的!
    badNum = 0.4.5;//当然，这句代码是错的，一个非法数字
```    
事实上这种风格才是最常见的
```
  var dog="小虎子"; var num=1; var str="some string",strNum="123";
```
数字（只能有整数或小数），字符串可能最常用的了，还有另一种类型：布尔值(Boolean).不像数字或字符串，有无限种可能的值，Boolean值只有两种可能：真，假
```
var bool=true;//用true表示真值
    bool=false;//用false表示假值
```
JavaScript是动态类型语言，在声明变量时无需指明其类型，在运行时刻变量的值可以有不同的类型。
```
 var s="Hello,World!!!";//无需指明为字符串类型
    s=1.61803;//在运行时将变量值指定为另一个类型
```
##变量类型
1. JavaScript的变量类型不止字符串，数字，布尔值这三种，然而这三种确是最常用的了。其它数据类型（参考）：
复合（引用）数据类型是：
    - 对象
    - 数组

2. 特殊数据类型是：
Undefined
 ```
 //事实上,我们接触的第一个数据类型是Undefined,它的含义是"未定义值"
       var a;//声明一个变量,但没有对其赋值
       alert(a);//但它仍然有值的,它的值为undefined
       alert(b);//但注意,输出一个未定义的变量将出现错误,而不是输出undefined 
```
3. 字符串
字符串相连
```
 var s1="Hello,";
    s1=s1+"World!";
    alert(s1);
    s1+="!!!!";
    alert(s1);
```
## 比较操作符:
<,>,<=,>=,==,!=,!;比较操作符返回布尔值
```
//小于 <
    //大于 >
    //小于或等于 <=
    //大于或等于 >=
    //相等 ==
    //不相等 !=
    alert(2<4);//返回true
    alert(2>4);//返回false
    alert(2<=4);//返回true
    alert(2>=2);//返回true
    alert(2==2);//返回true
    alert(2!=2);//返回true
```    
表达式的组合
```
    alert((2<4)==(5>3)==(3<=3)==(2>=2)==(2!=2)==(2==2)==true );
``` 
## 逻辑运算符
逻辑运算符用于对布尔值进行比较
```
 // &&逻辑与,当两边的值都为true时返回true,否则返回false
    // || 逻辑或,当两边值都为false时返回false,否则返回true
    // ! 逻辑非
    alert(true && false);//输出false
    alert(true && true);//输出true
    alert(true || false);//输出true
    alert(false || false);//输出false
    alert(!true);//输出false
```
# 分支结构
- 单一选择结构（if）
- 二路选择结构（if/else）
- 内联三元运算符 ?:
- 多路选择结构（switch）
```
 var condition = true; if (condition) {
        alert("我将出现！");
    }
    condition = false; if (condition) {
        alert("我不会出现！");
    } else {
        alert("我会出现！");
    }
    condition ="some string"; if (condition) {
        alert("可以直接对任何数据类型进行if判断,在判断时计算会自动将其转换成布尔值!");
    } var val = condition?"当为true时我将被返回":"当为false时我将被返回";
    alert(val);//将输出"当为true时我将被返回"
```
对于if..else语句，如果要执行的语句只有一条，可以不使用“｛｝”，但这种写法并不推荐.但确实这样可以简化代码:
```
 var str ="one"; if (str=="one") alert("str的值为字符串'one' !"); else alert("not one");
```
虽然JavaScript中没有if .... elseif 结构,但可以使用if...else的简写方式得到
```
 //为了判断用户输入的成绩的范围,我们使用了多重嵌套的if .. else语句
    var num = window.prompt("请输入XXX的成绩!","");
    num *=1;//window.prompt方法始终只返回字符串,用这样的方法将其转换成数字
    // if (...) {...}这算是一句
    if (isNaN(num)) {
        alert("您输入的不是一个数字!");
    } else if (num<=100 && num>=90) {
        alert("Excellent!");
    } else if (num =80) {
        alert("Good!");
    } else if (num < 80 && num >= 70) {
        alert("So so!");
    } else if (num < 70 && num >=60) {
        alert("Be careful !!!");
    } else if (num < 60 && num >= 0) {
        alert("Oh, NO!");
    } else {
        alert("USB!");
    } //看上去清晰多了,但要注意的是,JavaScript中没有elseif 这样的语法,所以上的else if之间是有空格的
```
用于进行多次判断的switch语句
```
 switch(condition) { //switch本来就是跳转的意思（又称为“开关”），所以switch语句就是判断情况，跳到符合的情况开始执行
        case 4:alert("c的值是4"); 
        case 3:alert("c的值肯定大于等于3"); 
        case 2:alert("c的值肯定大于等于2"); 
        case 1:alert("c的值肯定大于等于1");
    } //可以使用 break来只执行符合一个条件的语句
 switch(condition) { 
        case 4:alert("c的值是4"); break; 
        case 3:alert("c的值是3"); break; 
        case 2:alert("c的值是2"); break; 
        case 1:alert("c的值是1"); break;
    } 
var condition="one"; switch(condition) {//switch不但可以用来判断数字,还可以判断字符串，甚至是不定的变量
        case "one":
            alert("condition的值是字符串'one' !"); break;
        case "three":
            alert("condition的值是字符串'three' !"); break; 
        case "four":
            alert("condition的值是字符串'four' !"); break; 
        case "five":
            alert("condition的值是字符串'five' !"); break;
        default://当所有情况都不匹配时，将执行default语句后的
            alert("我们要万无一失!condition什么都不是!");
    }
```
# 循环
循环用来指明当某些条件保持为真时要重复的动作。当条件得到满足时，就跳出循环语句。在 JavScript 中有四种循环结构可用。
- 由计数器控制的循环（for）
- 在循环的开头测试表达式（while）
- 在循环的末尾测试表达式（do/while）
- 对对象的每个属性都进行操作（for/in）

for 语句指定了一个计数器变量，一个测试条件，以及更新该计数器的操作。在每次循环的重复之前，都将测试该条件。如果测试成功，将运行循环中的代码。如果测试不成功，不运行循环中的代码，程序继续运行紧跟在循环后的第一行代码。在执行该循环后，计算机变量将在下一次循环之前被更新。
```
 for (var i=0;i<10;i++) {//for循环的圆括号里面须放三个句子,分别是1.初使化计数器 2.判断条件 3.更新计数器
        alert("i当前的值为"+i);
    }
```
一个死循环最能说明while的工作方式了（但这样的错误我们绝不能在实际编程中出现）
```
 while (true) {
        alert("你关不掉我的！");//这就是网上那些所谓的高手写的“关不上的窗(周传雄新歌,力荐)”代码
    }
```
do..while循环与while循环不同之处在于它至少将代码块中的代码执行一次
```
 do {
        alert("我肯定会出现一次的");
    } while (false);
```
而对于for ... in循环，我们将在讲解数组和对象时使用
# javascript实现回到顶部效果
## <script>标签解析

属性 | 解释
---|---
charset| src指定字符集
scr | 包含要执行代码的外部文件
type|type="text/javascript" 
## 使用（类似于css）：
1. 在html文件中写入```<script></script>```直接在script标签中写javascript
2. 新建js脚本文件```<script type="text/javascript" src="index.js"></script>```

## 测试
```
//index.js
alert('javascript')
```
## 页面加载后完成
```
window.onload = function () {
    alert('javascript')
}
```
## 获取元素
```
var obtn = document.getElementById('btn');
```
## 为btn添加点击事件
```
obtn.onclick = function(){
    alert('javascript')
}
```
## 获取滚动条到顶部的距离
```
var osTop = document.documentElement.scrollTop;
//alert(osTop)
```
## 改写滚动条到顶部的距离
```
document.documentElement.scrollTop = 200;
//点击一次向上移动200    -=200
```
## 动画效果
```
//设置定时器
var timer = null;
timer = setInterval(function(){
    var osTop = document.documentElement.scrollTop;
    document.documentElement.scrollTop -= 200;
    if(osTop == 0 ){//解决回到顶部后无法下拉
			clearInterval(timer);
	} 
},30);//此动画隔30毫秒执行一次

```
## 减速向上滚动
```
var ispeed = osTop/7;
document.documentElement.scrollTop = osTop - ispeed;
```
## 向上滚动时无法暂停
没到顶部，所以不清除计时器
```
window.onscroll = function(){//滚动条滚动时触发
        //停止滚动时，清除计时器
    	if(!isTop){
    		clearInterval(timer);	
    	}
    	isTop = false;
//此时会暂停，应在计时器函数中加isTop = true;
```
## 多次点击bug
onclick后清除计时器
## 按钮的显示与隐藏
不做解释，请自行练习
