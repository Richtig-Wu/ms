## App打包
```
答案：http://jingyan.baidu.com/article/c45ad29c2ffc1e051653e272.html
```
## js基本数据类型
```
String / Number / Boolean / Object/  Undefined / Function / Null
```
## 什么是闭包
```
有权访问另一个函数内部作用域的变量的函数叫闭包
```
## 闭包的作用
```
减少全局变量，使变量私有化！
```
## 字符串的常用方法
```
例如：					
var str = "ABC";
str.charCodeAt(0);
结果：65
将字符串转成ascii码
String.fromCharCode(65,66,112);
结果：ABp
将ascii码转成字符串
str.charAt(1);
获取字符
012345
var str = "ABCDEF";
str.slice(2,4);
结果：CD
截取字符串起始位置到结束位置
012345
var str = "ABCDEF";
str.substr(2,4);
结果：CDEF
截取字符串起始位置到截取的几位
var str = "ABCDEF";
str.concat("ABCDEF","ABC");
结果：ABCDEFABCDEFABC
连接字符串
var str = "AA BB CC DD EE FF";
alert(str.split(" "，3));
结果：
AA,BB,CC
截取字符串
var str = "ABCabc";
str.toLowerCase();
结果：abcabc
将字母转换>>>>>>> 9dbe7db676dd1bba44437e425cb4a5f2b71ec1ae:mst/mianshi_zy.md成小写
var str = "ABCabc";
str.toUpperCase();
结果：ABCABC
将字符转换成大写
```
## 数组的常用方法
```
push：向数组的末尾增加一项 返回值是数组的新长度
unshift：向数组开头增加一项 返回值是数组的新长度
pop:删除数组的末尾项 返回值是删除的数组项
shift:删除数组开头项 返回被删除的开头项目
splice：删除数组中的任意项 返回值是被删除的数组项
slice:复制数组 返回值是复制到的新数组 写上数值之后 不包含被复制的最后一项

拼接：
concat:把一个数组和另一个数组拼接在一起 返回拼接好的数组
join:把数组中的每一项 按照指定的分隔符拼接成字符串

排序：
reverse:倒序数组 返回值倒序数组 原有数组改变
sort:根据匿名函数进行冒泡排序 b-a倒序 a-b升序

indexOf:返回获取项在数组中的索引
lastIndexOf:返回获取项在数组中出现的最后一次索引
forEach: 循环遍历数组 参数是一个匿名函数 默认返回为undefined
map：循环遍历数组 参数是一个匿名函数
```
## js类的使用
```
/***定义类***/
var Class = function(){
  var _self = this;//把本身引用负值到一变量上
  var _Field = "Test Field"; //私有字段
  var privateMethod = function(){ //私有方法
    alert(_self.Property); //调用属性
  }
  this.Property = "Test Property"; //公有属性
  this.Method = function(){ //公有方法
    alert(_Field); //调用私用字段
    privateMethod(); //调用私用方法
  }


实例化类
var c = new Class();
c.Method(); //使用方法
```
## 原型链
```
JavaScrip可以采用构造器(constructor)生成一个新的对象,每个构造器都拥有一个prototype属性,
而每个通过此构造器生成的对象都有一个指向该构造器原型(prototype)的内部私有的链接(proto),
而这个prototype因为是个对象,它也拥有自己的原型,这么一级一级直到原型为null,这就构成了原型链
```
## Object原型指向谁
```
每个构造函数内部均有一个prototype原型指针，指向该类型的原型对象C.prototype。原型对象C.
prototype中包含一个回指向构造函数的指针constructor。这样就实现了构造函数和原型对象间的双向绑定。
每个实例对象内部也包含一个指向原型对象C.prototype的指针。
```
## typeof
```
typeof返回变量的类型
```
## DOM是什么
```
HTML DOM 定义了所有 HTML 元素的对象和属性，以及访问它们的方法。
换言之，HTML DOM 是关于如何获取、修改、添加或删除 HTML 元素的标准
```
## JQuery常用的方法
```
http://www.css88.com/jqapi-1.9/
```

## JQuery中的find方法是干嘛的
```
方法获得当前元素集合中每个元素的后代、通过选择器、jQuery 对象或元素来筛选
返回 <ul> 后代中所有的 <span> 元素：
$(document).ready(function(){
$("ul").find("span").css({"color":"red","border":"2px solid red"});
});
```
## 事件冒泡
```
当你使用事件冒泡时，子级元素先触发，父级元素后触发
```
## 事件捕获
```
当你使用事件捕获时，父级元素先触发，子级元素后触发
```
## CSS3
```
移动 translate3d(value,value,value) 可以改变元素的位置.
缩放 scale3d(x, y, z), scaleX(x) .
旋转 rotate3d(x,y,z,deg), rotateX(deg) 可以对元素进行旋转.
倾斜 skew(deg, deg),skewX(deg) ,skewY(deg)可以使元素按一定的角度进行倾斜
以上四个还有2D
------------------------------------------------------------------
border-radius 边框圆角化
rotate（angle）  定义 2D 旋转
text-shadow  阴影 可分别设置偏移量、模糊度、颜色（可设透明度）
background: linear-gradient(to bottom , red, white); 线性渐变
background-image: radial-gradient(100px at center,yellow 50%  , blue, red); 径向渐变
transition-property 设置过渡属性
transition-duration 设置过渡时间
transition-timing-function 设置过渡速度
transition-delay 设置过渡延时】

animation-name 设置动画序列名称
animation-duration 动画持续时间
animation-delay 动画延时时间
animation-timing-function 动画执行速度，linear、ease等
animation-play-state 动画播放状态，play、paused等
animation-direction 动画逆播，alternate等
animation-fill-mode 动画执行完毕后状态，forwards、backwards等
animation-iteration-count 动画执行次数，inifinate等

flex-grow 设置的flex子项的扩展比例
flex-shrink 设置的flex子项的收缩比例
flex-basis 设置的flex子项的基准宽度
flex-flow 设置flex-direction 和flex-wrap
flex-direction 设置子元素排列的方向
flex-wrap 设置子元素是否允许换行
justify-content 横轴的对齐方式
align-items 纵轴对齐
align-content 设置的横向有换行的盒子的纵轴对齐
align-self 子元素自身的纵轴对齐
order 设置子元素的排列顺序
```
##canvas (绘画)
```
https://nts.newbieol.com/classroom/study/327?lid=4238
```
## 如何实现Socket.io
```
socket.io 的核心就是这两个函数了，通过 emit 和 on 可以轻松地实现服务器与客户端之间的双向通信
emit ：用来发射一个事件或者说触发一个事件，第一个参数为事件名，第二个参数为要发送的数据，第三个参数为回调函数（一般省略，如需对方接受到信息后立即得到确认时，则需要用到回调函数）。
on ：用来监听一个 emit 发射的事件，第一个参数为要监听的事件名，第二个参数为一个匿名函数用来接收对方发来的数据，该匿名函数的第一个参数为接收的数据，若有第二个参数，则为要返回的函数
connect 事件，当收到对方发来的数据后触发 message 事件（通常为 socket.send() 触发），当对方关闭连接后触发 disconnect 事件
```

## Ajax和jsonp干什么用的，有什么区别？
```
1.ajax和jsonp的调用方式很像，目的一样，都是请求url，然后把服务器返回的数据进行处理，因此jquery和ext等框架都把jsonp作为ajax的一种形式进行了封装；
2.实质不同
　　　ajax的核心是通过xmlHttpRequest获取非本页内容
　　　jsonp的核心是动态添加script标签调用服务器提供的js脚本
3.区别联系
　　 不在于是否跨域
　　 ajax通过服务端代理一样跨域
　　 jsonp也不并不排斥同域的数据的获取
4.jsonp是一种方式或者说非强制性的协议
    ajax也不一定非要用json格式来传递数据
```

## 对jquery的ajax进行二次封装
** ajax封装 **
封装时用到的参数：
```
$(function(){
        /**
         * ajax封装
         * url 发送请求的地址
         * data 发送到服务器的数据，数组存储，如：{"username": "张三", "password": 123456}
         * succCallback 成功回调函数
         * errorCallback 失败回调函数
         * type 请求方式("POST" 或 "GET")， 默认已经设置为 "POST"
         * dataType 预期服务器返回的数据类型，常用的如：xml、html、json、text
         * reference jquery-1.7.1.js
         */

        //插入loading
        var html = "";
            html += '<div class="js_loading">';
            html +=     '<div class="mask"></div>';
            html +=     '<div class="loading">';
            html +=         '<span><img src="loading.gif"></span>';
            html +=     '</div>';
            html += '</div>';
        $("body").append(html);

        function $ajax(url, postData, succCallback, errorCallback, type, dataType){
            var type = type || "post";
            var dataType = dataType || "json";

            $.ajax({
                type: type,
                url: url,
                data: postData,
                dataType: dataType,

                beforeSend: function(){  //开始loading
                    $(".js_loading").show();                    
                },

                success: function(res){
                    if(res.success){
                        if(succCallback){
                            succCallback(res);
                        }                       
                    }else{
                        if(errorCallback){
                            errorCallback(res);
                        }
                    }                   
                },

                complete: function(){   //结束loading
                    //$(".js_loading").remove();
                    $(".js_loading").hide();
                }
            });
        }
    });
------------------------------------------------------------------------------------
页面调用：

<!DOCTYPE html>
<html>
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0, maximum-scale=1.0, user-scalable=no">
<title>ajax再封装</title>
<style>
.js_loading{display:none;}
.mask{background:rgba(255, 255, 255, 0);position:fixed;left:0;top:0;width:100%;height:100%;z-index:1;}
.loading{position:fixed;left:0;top:0;width:100%;height:100%;z-index:2;display:box;box-pack:center;box-align:center;display:-webkit-box;-webkit-box-pack:center;-webkit-box-align:center;}
.loading span{display:block;background:#333;width:40px;height:40px;border-radius:3px;text-align:center;}
.loading img{width:26px;margin-top:7px;}
</style>
<script src="jquery-1.7.1.js"></script>
</head>
<body>
<button type="button" class="btn">获取</button>
<div class="box"></div>
<script>
    $(function(){
        $(".btn").click(function(){
            var postData = {
                username: '张三',
                password: 123456
            };
            $ajax(
                'test.asp',
                postData,
                function(res){  //成功
                    $(".box").html(res.firstName);
                },
                function(res){  //失败
                    $(".box").html(res.fail);
                }
            );
        });
    });
</script>       
</body>
</html>
--------------------------------------------------------------------------
请求页面test.asp

{
    "success":true,
    "firstName":"获取成功！！！",
    "lastName":"哈哈...",
    "fail":"获取失败！！！"
}

```
## 怎么实现分页
```
1.首先在页面放两个隐藏域，一个是当前页码，一个是总页码，总页码是页面加载完，从后台查询出来后直接附上值的，当前页码是每操作一个，就要对当前页码赋值
2.写一个页面加载完的function，给总页码和当前页码赋值
3.抽取的ajax方法，此页面会用到好几次这个方法，所有把它收取了出来，因为页面的数据时通过ajax从后台获取到的，后台返回的是一个List集合
```

## call 方法和 apply方法的区别?

```
共同功能：绑定this值
区别：apply和call的功能是一样的，只是传入的参数列表形式不同。
apply ：可以接收数组，返回的结果是将数组进行拆分
call : 可以接收多个单个参数
```
## 公司总共js脚本总共在多少行代码？
```
在5000  ~  8000 行左右
```

## js脚本是每个页面多写一个吗？
```
可以每一个页面写一个js脚本。也可以写一个JS脚本文件直接引用。
```

## 你为什么要投我这个公司？
```
先是了解岗位的需求，去公司的官网查看 公司做什么的。在总结一下……
```
## 你为什么离开上一家公司？
```
我之前公司工作做实习生，我做了有半年多一直没有转正，我跟老板提过这样的问题，老板说因为现在不缺正式员工，所以暂时还不能转正。我一直想要转正所有才会跳槽！
```
## 你工作中遇到困难是怎么解决的？
```
首先去看它的官方文档，英文看不懂，就去找中文的官方文档解决。解决不了就去Google搜索找答案。如果找不到答案我们就去论坛找比如stack overflow,我经常上这个论坛，基本有80%可以找到答案。如果还找不到就去问同事或者我跟我同行的人去寻求帮助！！！
```
## 你最近遇到最大的阻碍是什么，让你觉的很困难。然后你是怎么解决它克服它的？
```
？？？？？？？？？？？？？？？？？？？？？？？？
```

## 你还有什么想了解我们公司的吗？
```
你们公司最近在做什么项目，主要用到些什么技术? 如果我上班 主要是负责那一块？ 你们公司最近有去探索什么新技术吗？
```
## 你们公司有哪些部门 多少人？
```
部门有：售电部门，财务部，综合部，人事部，DT事业部（包括-硬件组，软件组，工程组，商务组）
我们公司总共30人左右，我们部门12人，软件组6人，3人前端3人后端，3人硬件组，1人工程组，2人商务组。
```

# ---------------------------------------------------------------------------------------------------------------

## 相对定位和绝对定位的区别
```
relative： 相对定位，相对于自己在文档流中的位置进行偏移，并且原来在文档流中占有的位置得以保留。
absolute：绝对定位，相当于自己向父级元素查找出的第一个带有position属性的元素进行定位，并且脱离文档流，原来在文档流中所占用的位置不保留。
```
## z-index有什么用？
```
z-index有一个层级的关系，设的值越大，层级也就越高！
```
## 在没有设置z-index属性时，文档层级中有哪些上下文的关系，哪些元素会高于其它元素
```
浮动会比普通元素层级高，绝对定位会比相对层级高。元素是从左到右从上到下。
```
## 什么是事件委托，jquery 举例一个
```
利用事件冒泡的原理，让自己的所触发的事件，让他的父元素代替执行！
1  <ul id = "lists">
2          <li>列表1</li>
3          <li>列表2</li>
4          <li>列表3</li>
5          <li>列表4</li>
6          <li>列表5</li>
7          <li>列表6</li>
8  </ul>
===============================================================
1  $(function(){
2             $("#lists").on("click","li",function(event){
3                 var target = $(event.target);
4                 target.css("background-color","red");
5             })
6         })
```
## 什么是闭包，什么时候会用到闭包
```
在一个函数A中,返回一个函数,并且返回函数中引用了A中的变量.那么这个返回函数就是一个闭包
在封装函数时可能会用到闭包，闭包可以减少全局变量的定义,实现变量私有化
```
## 深拷贝和浅拷贝的区别，深拷贝有什么方法
```
浅拷贝只是对指针的拷贝，拷贝后两个指针指向同一个内存空间，深拷贝不但对指针进行拷贝，而且对指针指向的内容进行拷贝，深拷贝后的指针是指向两个不同的地址
深拷贝的方法：比如一个数组，深拷贝我需要在创建一个新的数组，然后通过for循环一个一个赋值到另外一个数组，这样就形成了深拷贝
```
## 说出ES6的新特性
```
箭头函数，模板字符串，拓展运算符，let和const关键字
```
## 箭头函数this的指向谁
```
定义时所在的对象
```
## 假设我在Constructor的一个函数中，去执行一个super函数，这时候这个super函数作用是什么？
```
1、用在子类的构造方法里，主要是调用父类的默认构造方法。
2、在子类里调用隐藏或重写的属性或行为
总结：是调用父类的无参构造方法,创建一个父类(这是因为创建子类对象之前都要先创建父类对象,以便他继承父类的属性和方法),只有先创建了父类,类才能正确初始化
```
## 类中的静态和非静态的区别
```
静态成员：静态类中的成员加入static修饰符,即是静态成员.可以直接使用类名+静态成员名访问此静态成员,因为静态成员存在于内存,非静态成员需要实例化才会分配内存,所以静态成员不能访问非静态的成员..因为静态成员存在于内存,所以非静态成员可以直接访问类中静态的成员.

 非成静态员：所有没有加Static的成员都是非静态成员,当类被实例化之后,可以通过实例化的类名进行访问..非静态成员的生存期决定于该类的生存期..而静态成员则不存在生存期的概念,因为静态成员始终驻留在内容中..
```
## 什么是跨域，有什么方法可以实现跨域
```
跨域就是不同源，如：协议，端口，域名。可以用jsonp，添加script标签来调用服务器的JS脚本（代码），来实现跨域
```
## Fetch的优点
```
实现一个异步刷新
注：Fetch跟ajax本质上没有什么区别，多是实现一个异步刷新，但是他比ajax语法简洁，更加语义化。基于标准 Promise 实现，支持 async/await
```
